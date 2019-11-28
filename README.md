# wsdl_inner_schemas_xjb_usage
very simple WSDL, schemas inside (schema sections), java package name rewrite with XJB file

There are 3 namespaces in the wsdl: my_name_space, a, b.

If you generate classes with the command "wsimport aservice.wsdl" then you will get 4 java packages: wsdl_name_space, a, b, c.
wsdl_name_space contains the port and service, c contains the request and response, a and b contains inner types used in request / response.

If you generate classes with the command "wsimport -b packagedef.xjb aservice.wsdl" then you will get 4 java packages: wsdl_name_space, schema1, schema2, schema3.
wsdl_name_space contains the port and service, schema1 contains the request and response, schema2 contains the A type from namespace a,
schema3 contains the B type from namespace b.

I don't know, how to change the "wsdl_name_space" package via xjb. But that's not needed usually.
