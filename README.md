# project-ingestor
A Small tool to ingest source code repos and abstract the obvios and keep the meaningful 

## How it Works?
It runs a lot of conditional tests over a repo to guess its changes and its relation to what got changed and why. We use a Expensive KI model to make sense out of the Data. You Should not run this unless you got access to a OpenStack API connected to some real clusters the ingestor by default is not designed to take single repos. It takes repo lists which get created by project-repo-finder which is a multi protocol crawler that finds repositorys. Via Extensiv Web Crawling.

When you run the ingestor for example on a small open source platform like a GitLab Enterprise instance this can take up on a single machine some ages.

- Look if it is a repo via file listing and matching conditions
- starts parsing relevant files into unified datastructure
- above mentioned datastructure gets piped into dspeed cloud 
- KI Model DIREKTSPEED-Exodia gets executed via your dspeed cloud access
- after that Exodia can use the results to build what ever was in that and can tell you what was in that repos.
  - abstraction level call stacks deassembler arguments and parameters. 
  - used code and who created it and why. 
  
  
a example nodejs project that consist of a express server containing server.js and a package.json that returns hello world would end up in meta like
```
NODEJS OLD
EXPRESS HTTP
"hello world!"
LISTEN PORT
```

It works a bit like copilot from github but in the invers direction as also it does not link the data to complet code it links the data always to the most lowest system level that got abstracted. Copilot creates code blocks via matchin and we interpret code blocks via matching and then create total new code out of it. 

## DIREKTSPEED Exodia KI Model
Is a Model Invented for Stealify with the aim to generate codeModification applications that can take existing code and refactor it into current use able code as also reduce bugs and use only the meaningful parts.
