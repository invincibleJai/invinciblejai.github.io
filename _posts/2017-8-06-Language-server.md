---
layout: post
title: Language Server Protocol (LSP)- Introduction
---

Today am gonna talk about language server protocol as the name suggest , it's an open JSON-RPC based protocol for communication between IDE's 
(Integrated Development Environment like JBoss Dev Studio , VScode , Eclipse-Che) and server.

![_config.yml]({{ site.baseurl }}/images/lsp-ide.png)


**Now the Question is , why de we even need it?**


Let me try to explain the need , as a developer almost all of us would have used IDE's and each one of us have their favourite IDE for some it 
could be JBoss , Eclipse , VScode etc. The question here is why are we so used to IDE's ? yes , they make our life easier. These IDE's support 
rich editing feature like syntax highlighting, code completion, flagging Errors, Go-to definition etc. So the point here is among all the rich 
editors out there , these features are common. Now supporting such complex features in IDE's is not an easy task , it's even time consuming and 
moreover it has to be developed specific to each IDE's i.e separately for eclipse, separately for VScode and list goes on. LSP is needed to 
address this pain point, it helps in decoupling language services from editors and calling it as server which can be utilised by any client(IDE's) 
via LS Protocol. So in simple term we can say it's increasing the reusability.

**Next Question which comes in mind would be , How to use it?**


![_config.yml]({{ site.baseurl }}/images/lsp-flow.png)

Language server works on it's own process and tools like VScode , Eclipse-che communicates with server via JSON-RPC. Above diagram shows how client
i.e IDE's and server communicates. Nice example for LSP can be seen [here](https://code.visualstudio.com/docs/extensions/example-language-server)

**Now we would be wondering who is doing all these great stuff?**

The Language Server Protocol was originally developed for Microsoft's Visual Studio Code. Later Microsoft announced along with Red Hat and Codenvy that the protocol is being adopted and supported by the three companies. At the same time, Microsoft made the Language Server Protocol specification an open standard, hosted on GitHub.

That's enough for introduction i guess, will be posting couple of more articles on LSP soon. In case of any queries do drop your comments.