# Community list of Mermaid diagrams [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
### You wish to add or change something? Please send me an [email](mailto:mvarga1989@gmail.com), create a [pull request](https://github.com/mvarga1989/Mermaid_notebook/pulls) or an [issue](https://github.com/mvarga1989/Mermaid_notebook/issues).

## Sources
-[Mermaid cheat sheet](https://jojozhuang.github.io/tutorial/mermaid-cheat-sheet/)
-[Mermaid demo](https://mvarga1989.github.io/Mermaid_notebook/)

## Examples
### Click functionality

```mermaid
graph LR;
A-->Google;
click Google "http://www.google.com"
```

### Flowchart:
```mermaid
graph LR
    subgraph Input
        A[Start] --> B[Read user input]
    end
    subgraph Process
        B --> C[Process user input]
    end
    subgraph Output
        C --> D[Display output]
    end
    subgraph Condition
        A --> E[Is user input valid?]
        E --> F[Yes] --> B
        E --> G[No] --> D
    end
    A --> E
```


### Sequence diagram:
```mermaid
sequenceDiagram
    participant Alice
    participant Bob

    Alice->>Bob: Hello
    Bob->>Alice: Hi
    Alice->>Bob: How are you doing?
    Bob->>Alice: I'm doing well, thanks for asking.
    Alice->>Bob: That's good to hear.
    Bob->>Alice: What's up?
    Alice->>Bob: Not much. Just wanted to say hi.
    Bob->>Alice: It's good to hear from you.
    Alice->>Bob: Talk to you later.
    Bob->>Alice: Bye.
```
	
```mermaid
  graph TD;
      A-->B;
      A-->C;
      B-->D;
      C-->D;
```

### Gantt chart:
```mermaid
gantt
    title Project Plan
    dateFormat  YYYY-MM-DD
    section Requirements
        Requirements gathering    :start=2023-10-17, end=2023-10-21
        Requirements analysis     :start=2023-10-21, end=2023-10-28
    section Design
        System design              :start=2023-10-28, end=2023-11-04
        Database design           :start=2023-11-04, end=2023-11-11
        User interface design   :start=2023-11-11, end=2023-11-18
    section Development
        Backend development     :start=2023-11-18, end=2023-12-05
        Frontend development   :start=2023-11-25, end=2023-12-12
    section Testing
        Unit testing              :start=2023-12-05, end=2023-12-12
        Integration testing     :start=2023-12-12, end=2023-12-19
        System testing           :start=2023-12-19, end=2023-12-26
    section Deployment
        Deploy to production  :start=2023-12-26, end=2023-12-31
```

### Source: [martinwoodward](https://gist.github.com/martinwoodward/8ad6296118c975510766d80310db71fd?permalink_comment_id=4065246)
```mermaid
sequenceDiagram
    participant user
    participant [example](example.com)
    participant iframe
    participant ![viewscreen](./.tiny-icon.png)
    user->>dotcom: Go to the [example](example.com) page
    dotcom->>iframe: loads html w/ iframe url
    iframe->>viewscreen: request template
    viewscreen->>iframe: html & javascript
    iframe->>dotcom: iframe ready
    dotcom->>iframe: set mermaid data on iframe
    iframe->>iframe: render mermaid
```


### Source: [LozanoMatheus](https://gist.github.com/martinwoodward/8ad6296118c975510766d80310db71fd?permalink_comment_id=4065246#gistcomment-4065246)
```mermaid
flowchart LR;
    A-->B;
    B-->C;
    C-->D;
    click A callback "Tooltip for a callback"
    click B "http://www.github.com" "This is a tooltip for a link"
    click A call callback() "Tooltip for a callback"
    click B href "http://www.github.com" "This is a tooltip for a link"
```
	

### Source: [Datamweb](https://gist.github.com/martinwoodward/8ad6296118c975510766d80310db71fd?permalink_comment_id=4067229#gistcomment-4067229)
```mermaid
  flowchart LR;
      A[CI MULTI CHAPTCHA]-->B{Select captcha service by developer?};
      classDef green color:#022e1f,fill:#00f500;
      classDef red color:#022e1f,fill:#f11111;
      classDef white color:#022e1f,fill:#fff;
      classDef black color:#fff,fill:#000;
      B--YES-->C[How to use?]:::green;
      
      C-->U[I choose recaptcha.]:::green;
      U--Views-->Q["echo CIMC_JS('recaptcha');\n echo CIMC_HTML(['captcha_name'=>'recaptcha']);"]:::green;
      U--Controller-->W["CIMC_RULE('recaptcha');"]:::green;
      
      C-->I[I choose arcaptcha.]:::white;
      I--Views-->O["echo CIMC_JS('arcaptcha');\n echo CIMC_HTML(['captcha_name'=>'arcaptcha']);"]:::white;
      I--Controller-->P["CIMC_RULE('arcaptcha');"]:::white;
      
      C-->X[I choose bibot.]:::red;
      X--Views-->V["echo CIMC_JS('bibot');\n echo CIMC_HTML(['captcha_name'=>'bibot']);"]:::red;
      X--Controller-->N["CIMC_RULE('bibot');"]:::red;
      
      B--NO-->D[How to use?]:::black;
      D---Views:::black-->F["echo CIMC_JS('randomcaptcha');\n echo CIMC_HTML(['captcha_name'=>'randomcaptcha']);"]:::black; 
      D---Controller:::black-->T["CIMC_RULE('archaptcha,recaptcha,bibot');"]:::black;
```

### Source: [mathdatasimplified.com](https://mathdatasimplified.com/2022/04/29/mermaid-create-flow-chart-using-code/)
```mermaid
graph TD
    A[Should you go to work today?] --> B(Do you like working?)
    B --Yes--> C{Go to work}
    B --No--> D(Are you feeling sick?)
    D --Yes--> E{Go to the doctor}
    D --No--> F(Do you have a lot of work to do?)
    F --Yes--> H(And you don't want to go?)
    F --No--> H  
    H --Yes, I don't want to-->I(You signed up for this. Get dressed and go to work!) 
```