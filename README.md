# Resolver

Delete this link at the end of the specification process:

- [Roadmap to Specification](../../issues/1)

## Location

The Resolver is part of the DomainInterface.

## Description

Mapping between information models is a complicated and laborious function. In case of
very different information structures, it might even fail. Also creating an interface between
the Telefonica information model inside x:akta and the MW SDN controller has been cancelled during
the Transport SDN Pilot project. (An interface between the Enghouse information model inside x:akta
and the MW SDN controller has been created instead, but later discontinued.) The Resolver represents
a workaround, which allows to address single attributes in the MW SDN controller from within x:akta
or other legacy tools in a very generic way. The consuming tool must formulate the path to
the targeted attribute according to the ONF information structure but is free to substitute segments
of the path by placeholders. The Resolver parses through the paths, identifies the placeholders and
replaces them by concrete address components. The Resolver does the bare and generic parsing.
It depends on further applications to provide the information for replacing the placeholders.

## Relevance

The Resolver is supporting legacy applications in addressing live network resources.

## Resources

- [Specification](./spec/)
- [TestSuite](./testing/)
- [Implementation](./server/)

## Dependencies

### [Accesport2LtpTranslator](https://github.com/openBackhaul/Accessport2LtpTranslator)

- [Create ServiceList](openBackhaul/Accessport2LtpTranslator#18)
- [Create ProfileList](openBackhaul/Accessport2LtpTranslator#19)
- [Create ProfileInstanceList](openBackhaul/Accessport2LtpTranslator#20)
- [Create ForwardingList](openBackhaul/Accessport2LtpTranslator#37)
- [Create CONFIGfile](openBackhaul/Accessport2LtpTranslator#38)

### [Linkid2LtpTranslator](https://github.com/openBackhaul/Linkid2LtpTranslator)

- [Create ServiceList](openBackhaul/Linkid2LtpTranslator#7)
- [Create ProfileList](openBackhaul/Linkid2LtpTranslator#8)
- [Create ProfileInstanceList](openBackhaul/Linkid2LtpTranslator#9)
- [Create ForwardingList](openBackhaul/Linkid2LtpTranslator#15)
- [Create CONFIGfile](openBackhaul/Linkid2LtpTranslator#17)

## Comments

This application will be specified during [training for ApplicationOwners](https://gist.github.com/openBackhaul/5aabdbc90257b83b9fe7fc4da059d3cd).
