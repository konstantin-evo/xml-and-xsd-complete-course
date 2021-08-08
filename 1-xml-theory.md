# XML Theory 
## What is XML ?
**XML** (Extensible Markup Language) is a markup language that defines a set of rules for encoding documents in a format that is both human-readable and machine-readable.

The design goals of XML emphasize simplicity, generality, and usability across the Internet. It is a textual data format with strong support via Unicode for different human languages. Although the design of XML focuses on documents, the language is widely used for the representation of arbitrary data structures such as those used in web services.

Several schema systems exist to aid in the definition of XML-based languages, while programmers have developed many application programming interfaces (APIs) to aid the processing of XML data.

**Characteristics:**
* Self-descriptive tags, representing only the structure and info of the data, not anything about its displaying or processing.

XML separates data from presentation, or from the view.

When the view is necessary (final-user systems), XML is generally used along with HTML and CSS, these who care about which part of data to show, how to organize it along the web page and which style to use, but not with the data itself (XML cares about the data!).
* There are no predefined tags, but all custom created tags are extensible and reusable. In practice, tags are defined at XSD files and imported to XML files, in order to be used.
* XML stores data in plain text format. A software- and hardware independent way of storing, transporting, and sharing data with no data losing or compatibility issues.

Either at the back-end or at the front-end, XML can be consumed (read/processed) or produced – using any programming language – and the data sent to the view for displaying (to the final user) or for being consumed by another server (e.g., via SOAP or REST web services).
* Can be read easily by humans, programming APIs, voice synthesizers and all sorts of algorithms, both at front-end as well as at back-end development layers.
* Can be used to represent and transfer any human-machine understandable data, within any field of human knowledge, using many different programming languages.

**A tree-based structure:**
Its syntax has a tree-based structure of elements (tags) similar to HTML.

![XML tree-based structure](/img/1-xml-tree.png)
```xml
<konstantin-evo:dog konstantin-evo:animalId="1">
		<konstantin-evo:name>DogA</konstantin-evo:name>
		<konstantin-evo:species>Canis familiaris</konstantin-evo:species>
		<konstantin-evo:color>Brown</konstantin-evo:color>
		<konstantin-evo:birthDate>2005-01-01</konstantin-evo:birthDate>
		<konstantin-evo:owner>OwnerDEF</konstantin-evo:owner>
</konstantin-evo:dog>
<konstantin-evo:cat konstantin-evo:animalId="2">
		<konstantin-evo:name>CatA</konstantin-evo:name>
		<konstantin-evo:species>Felis catus</konstantin-evo:species>
		<konstantin-evo:color>white</konstantin-evo:color>
		<konstantin-evo:birthDate>2000-01-01</konstantin-evo:birthDate>
		<konstantin-evo:owner>OwnerABC</konstantin-evo:owner>
</konstantin-evo:cat>
  ```
## XML Syntax
In this chapter, we will discuss the simple syntax rules to write an XML document. XML documents that bind to the syntax rules are said to be “well formed”.

* **One root element**

There must be one and only root element, on each XML document (XSD instances), into which other elements may be nested

```xml
 <?xml version="1.0" encoding="UTF-8"?>
 <!DOCTYPE example [<!ENTITY copy "&#xA9;">]>
   
 <rootElement attribute="xyz">
   <contentElement/>
 </rootElement>
```
* **The prolog line is optional and always at first on**
```xml
<?xml version="1.0" encoding="UTF-8"?>
```
* **Closing tag**

All element tags must have a closing tag, except the prolog that is not part of the document

Incorrect:
```xml
<body>See Spot run.<body>See Spot catch the ball.
```
Correct:
```xml
<body>See Spot run.</body><body>See Spot catch the ball.</body>
```
* **XML tags are case sensitive**

When you createXML documents the tag <Body> is different from the tag <body>.

Incorrect:
```xml
<Body>See Spot run.</body>
```
Correct:
```xml
<body>See Spot run.</body>
```
* **All XML elements must be properly nested**
	
Impropernesting of tags makes no sense to XML.

Incorrect:
```xml
<b><i>This text is bold and italic.</b></i>
```
Correct:
```xml
<b><i>This text is bold and italic.</i></b>
```
* **Attribute values must always be quoted**
	
Itis illegal to omit quotation marks around attribute values. XML elementscan have attributes in name/value pairs; however the attribute valuemust always be quoted.
	
Incorrect:
```xml
<?xml version= "1.0" encoding="ISO-8859-1"?><note date=05/05/05><to>Dick</to><from>Jane</from></note>
```
Correct:
```xml
<?xml version= ?1.0? encoding="ISO-8859-1"?><note date="05/05/05"><to>Dick</to><from>Jane</from></note>
```



