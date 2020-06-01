# Gf-Patterns V 1.9

## [GF](https://github.com/tomnomnom/gf) By [![Twitter](https://img.shields.io/badge/twitter-@TomNomNom-blue.svg)](https://twitter.com/TomNomNom) 

A wrapper around grep, to help you grep for things 

# installation

[Go Path Setup](https://github.com/golang/go/wiki/SettingGOPATH)

If you've got Go installed and configured you can install `waybackurls & Gf` with:

```bash 

▶ go get -u github.com/tomnomnom/waybackurls
```
```bash
▶ go get -u github.com/tomnomnom/gf
```

If you've installed using `go get`, you can enable auto-completion to your `.bashrc` like this:

```bash
▶ echo 'source $GOPATH/src/github.com/tomnomnom/gf/gf-completion.bash' >> ~/.bashrc
```

Note that you'll have to restart your terminal, or run `source ~/.bashrc` for the changes to
take effect.

To get started quickly, you can copy the example pattern files to `~/.gf` like this:
```bash
▶ mkdir .gf
```
```bash
▶ cp -r $GOPATH/src/github.com/tomnomnom/gf/examples ~/.gf
```
**MY Gf Patterns installation**
```bash
▶ git clone https://github.com/1ndianl33t/Gf-Patterns
```

To get started quickly, you can copy the example pattern files to `~/.gf` like this:
```bash
▶ mkdir .gf
```
```bash
▶ mv ~/Gf-Patterns/*.json ~/.gf
```
**Use example**
```bash

▶ cat subdomains.txt | waybackurls | sort -u >> waybackdata | gf ssrf | tee -a ssfrparams.txt

▶ cat waybackdata | gf redirect | tee -a redirect.txt
```
### Pattern Files

The pattern definitions are stored in `~/.gf` as little JSON files that can be kept under version control:

**gf ssrf**

```bash
▶ cat ~/.gf/ssrf.json

{
    "flags": "-iE",
     "patterns": [

        "access",
        "admin",
        "dbg",
        "debug",
        "edit",
        "grant",
        "test",
        "alter",
        "clone",
        "create",
        "delete",
        "disable",
        "enable",
        "exec",
        "execute",
        "load",
        "make",
        "modify",
        "rename",
        "reset",
        "shell",
        "toggle",
        "adm",
        "root",
        "cfg",
        "dest",
        "redirect",
        "uri",
        "path",
        "continue",
        "url",
        "window",
        "next",
        "data",
        "reference",
        "site",
        "html",
        "val",
        "validate",
        "domain",
        "callback",
        "return",
        "page",
        "feed",
        "host",
        "port",
        "to",
        "out",
        "view",
        "dir",
        "show",
        "navigation",
        "open"
        
      ]
}

```

**gf redirect**

```bash
▶ cat ~/.gf/redirect

{
    "flags": "-iE",
     "patterns": [
"forward=",
"dest=",
"redirect=",
"uri=",
"path=",
"continue=",
"url=",
"window=",
"to=",
"out=",
"view=",
"dir=",
"show=",
"navigation=",
"Open=",
"file=",
"val=",
"validate=",
"domain=",
"callback=",
"return=",
"page=",
"feed=",
"host=",
"port=",
"next=",
"data=",
"reference=",
"site=",
"html="
]
}

```
***gf rce***
```bash
▶ cat ~/.gf/rce.json
{
    "flags": "-iE",
     "patterns": [
 
        "daemon",
        "upload",
        "dir",
        "execute",
        "download",
        "log",
        "ip",
        "cli",
        "cmd"
]
}
```
***Gf idor***

```bash
▶ cat ~/.gf/idor.json
{
    "flags": "-iE",
     "patterns": [

 "id",
 "user",
 "account",
 "number",
 "order",
 "no",
 "doc",
 "key",
 "email",
 "group",
 "profile",
 "edit",
 "report"
 
 ]
}

```






***Gf Sqli***
```bash
▶ cat ~/.gf/sqli.json
{
    "flags": "-iE",
     "patterns": [

         "id",
        "select",
        "report",
        "role",
        "update",
        "query",
        "user",
        "name",
        "sort",
        "where",
        "search",
        "params",
        "process",
        "row",
        "view",
        "table",
        "from",
        "sel",
        "results",
        "sleep",
        "fetch",
        "order",
        "keyword",
        "column",
        "field",
        "delete",
        "string",
        "number",
        "filter"
]
}
```
***Gf LFI***
```bash
▶ cat ~/.gf/lfi.json
{
    "flags": "-iE",
     "patterns": [

        "file",
        "document",
        "folder",
        "root",
        "path",
        "pg",
        "style",
        "pdf",
        "template",
        "php_path",
        "doc"
]
}
```

***Gf ssti***
```bash
▶ cat ~/.gf/ssti.json


{
    "flags": "-iE",
     "patterns": [
        
        "template",
        "preview",
        "id",
        "view",
        "activity",
        "name",
        "content",
        "redirect"
]
}
```

***Gf debug_logic***
```bash
▶ cat ~/.gf/debug_logic.json
{
    "flags": "-iE",
     "patterns": [

        "access",
        "admin",
        "dbg",
        "debug",
        "edit",
        "grant",
        "test",
        "alter",
        "clone",
        "create",
        "delete",
        "disable",
        "enable",
        "exec",
        "execute",
        "load",
        "make",
        "modify",
        "rename",
        "reset",
        "shell",
        "toggle",
        "adm",
        "root",
        "cfg",
        "config"
]
}
```

### Donations
You can encourage me to contribute more to the open source with donations.

- Paypal - [https://www.paypal.me/1ndianl33t](https://www.paypal.me/1ndianl33t)

- GooglePay,Paytm -

`8085778875`


# Credit

[![Twitter](https://img.shields.io/badge/twitter-@TomNomNom-blue.svg)](https://twitter.com/TomNomNom)
[Bugcrowd HUNT](https://github.com/bugcrowd/HUNT)
[![Twitter](https://img.shields.io/badge/twitter-@1ndianl33t-blue.svg)](https://twitter.com/1ndianl33t)

# Contributers
@victoni `added more redirect parameters`

@s0meguy1 `redirect & ssrf pattern Added additional filters`

# Contact
[![Twitter](https://img.shields.io/badge/twitter-@1ndianl33t-blue.svg)](https://twitter.com/1ndianl33t)
