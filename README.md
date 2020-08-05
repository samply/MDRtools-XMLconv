# MDR Tools XML Converter
Convert [model](https://github.com/samply/mdr-tools-model) objects to an mdr XML file.

xsd/common.xsd is Copyright (C) 2015 Working Group on Joint Research, University Medical Center Mainz and licensed under GNU GPL 3 (see file header for details).

Example Usage:

```java
Namespace namespace = new Namespace();
/*
    Add groups, data elements... (see: https://github.com/samply/mdr-tools-model)
*/
String filename = "Your/Output/Path/mymdrfile.xml"
BufferedWriter writer = new BufferedWriter(new FileWriter(filename));
ModelToXSDObjects converter = new ModelToXSDObjects();
Export export = converter.convert(namespace);
JAXB.marshal(export,writer);
```