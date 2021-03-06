-----------------------------------------------------------------------

Usage: 

    Xsd2Code.exe <XSD File> [Namespace] [Output file name] [Options]

Where:
    <XSD File>                          - Path to an XSD file. Required
    [Namespace]                         - Generated code namespace. Optional. File name without extension if no value is specified
    [Output file name]                  - Name of the output (generated) file. Optional. 
    [Options]                           - Optional. See below for description

Options:
    
    
    /o[utput] <FileName>                - Name of the output (generated) file. 
                                          By default, name of the source file with extension .Designer.cs 
                                          (.Designer.vb or .Designer.cpp for VisualVasic and Visual C++ respectively)
    /n[s] <Namespace>                   - Generated code CLR namespace. Default: file name without extension
    /l[anguage] <Language>              - Generated code language (CS|VB|CPP). Default: CS
    /pl[atform] <Platform>              - Generated code target platform (Net20|Net30|Net35|Silverlight20). Default: Net20
    /c[ollection] <Collection Base>     - Collection base (Array|BindingList|List|ObservableCollection|DefinedType). Default: List
    /cu[ustomusings] <Custom Usings>    - Comma-separated of custom usings definition (E.g "Xsd2Code.Library,System.Xml.Linq")
    /sm <Serialize>                     - Serialize method name. Default: Serialize
    /dm <Deserialize>                   - Deserialize method name. Default: Deserialize
    /lf[m] <LoadFromFile>               - LoadFromFile method name. Default: LoadFromFile
    /sf[m] <SaveToFile>                 - SaveToFile methodname. Default: SaveToFile
    
    /is[+]                              - Include Serialize method
    /is-                                - Do not include Serialize method (default)
    
    /cl[+]                              - Include Clone method
    /cl-                                - Do not include Clone method (default)
    
    /dbg[+]                             - Enable debug step through
    /dbg-                               - Disable debug step through (default)
    
    /db[+]                              - Enable data bindings 
    /db-                                - Disable data bindings (default)
    
    /dc[+]                              - Generate WCF data contract attributes 
    /dc-                                - Do not generate WCF data contract attributes (default)
    
    /cl[+]                              - Generate Clone method (shallow copy) 
    /cl-                                - Do not generate Clone method (default)
    
    /ap[+]                              - Enable automatic properties
    /ap[-]                              - Disable automatic properties (default)  
    
    /sc[+]                              - Enable summary comment
    /sc-                                - Disable summary comment (default)
    
    /xa[+]                              - Generate xml attributes
    /xa-                                - Do not generate xml attributes (default)
    
    /if[+]                              - Enable initialization of fields (default)
    /if-                                - Disable all field initialization constructor or lazy
    
    /eit[+]                             - Exclude types from included Schemas in generation
    /eit-                               - Generate types from included schemas (default)
    
    /gbc[+]                             - Use Generic Base Class 
    /gbc-                               - Do not use Generic Base Class (default)
    
    /hp[+]                              - Hide private fields in IDE
    /hp-                                - Show private fields in IDE (default)

    /lic[ense]                          - Show license information
    
    /?, /h[elp]                         - Show this help
    
Example:

	Xsd2Code.exe Employee.xsd CompanyXYZ.Entities.HumanResources Employee.cs /c ObservableCollection /sc /dbg /cl /hp- /cu System.Xml.Linq,System.IO

