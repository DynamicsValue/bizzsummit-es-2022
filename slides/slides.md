---
marp: true
theme: bizzsummit
paginate: true
footer: '![image](./images/BizzSummitLogoBig.png)'
---

<style>
@import 'https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css';
</style>

![bg](./images/BizzSummitBackGroundTitle.png)

<style scoped>
img {
    margin-top: -30px;
    height: 300px;
    margin-left: 360px;
    text-align: center;
}
h1 {
  font-size: 70px;
  color: #fff;
  text-align: center;
  vertical-align: middle;
  margin-top: 5px;
}
h3 {
  font-family: 'Roboto';
  text-align: center;
  vertical-align: middle;
  margin-top: 30px;
}

</style>

![image](./images/BizzSummitLogoBig.png)

# Azure Functions, FakeXrmEasy, Dataverse
### Jordi Montaña

---

![bg](./images/Sponsors.svg)

---






<hr/>

![bg](./images/BizzSummitBackGround.png)

# ABOUT ME

## Jordi Montaña


- Coding at **10 yrs old**
- **.Net** in 2006
- Master's Degree in Computer Science, **Universitat Politècnica Catalunya (UPC)**, 2007
- Started with **CRM 4** in 2011
- Author of **FakeXrmEasy** since 2014
- Founded **DynamicsValue** in 2015
 


---
![bg](./images/BizzSummitBackGround.png)

<hr/>

# SOCIAL MEDIA

- Twitter: [https://twitter.com/jordimontana](https://twitter.com/jordimontana)

- LinkedIn: [https://es.linkedin.com/in/jordimontana](https://es.linkedin.com/in/jordimontana)

- Email: [jordi@dynamicsvalue.com](jordi@dynamicsvalue.com)


---

![bg](./images/BizzSummitBackGround.png)

<hr/>

# TALK LINKS

- Slides: [https://github.com/DynamicsValue/bizzsummit-es-2022](https://github.com/DynamicsValue/bizzsummit-es-2022)

- Sample code: [https://github.com/DynamicsValue/fake-xrm-easy-samples](https://github.com/DynamicsValue/fake-xrm-easy-samples)

- FakeXrmEasy Docs: [https://dynamicsvalue.github.io/fake-xrm-easy-docs/quickstart/](https://dynamicsvalue.github.io/fake-xrm-easy-docs/quickstart/)


---

![bg](./images/BizzSummitBackGround.png)

<hr/>

# AGENDA

- The Journey of **FakeXrmEasy (FXE)**
- Why?
- Evolution of Unit Testing in Dynamics / Dataverse
- The new Dataverse Client SDK, and new FXE versions
- Demo
- OSS Licensing Considerations
- Q & A


---

![bg](./images/BizzSummitBackGround.png)

<hr/>

# Journey of FakeXrmEasy (FXE)

In 2013 I was told...

- "Unit testing is **too complex**, **too time consuming**"
- "It's xRM man, **no one cares** about **quality** of the software"
- "Not **worth** it"


---

![bg](./images/BizzSummitBackGround.png)

<hr/>

# Journey of FakeXrmEasy (FXE)

... but what if it's **complex BECAUSE** ... 

- you're **mocking every single request, every time?**
- and mocks don't actually **mimic Dataverse / Dynamics behavior?**
- and the code for mocking is actually **bigger** than, say, **plugin** code?
- and **maybe thay's WHY is not worth it?**...

---

![bg](./images/BizzSummitBackGround.png)

<hr/>

# Journey of FakeXrmEasy (FXE)

... and so ... **what IF** ... 

- you **didn't** have to mock anything (and it was **done for you?**)
- you could just use the **IOrganizationService** (something you're already **familiar** with?)
- it could **mimic Dataverse / Dynamics** behavior?
- more like **data-driven**, like when you doing **normal development?**


---
![bg](./images/BizzSummitBackGround.png)

<hr/>

# Journey of FakeXrmEasy (FXE)

... and **SO** we could...  

- **reduce costs** because we could spot **issues** much **earlier**?
- run **thousands** of tests **at scale**? (because they run **In-Memory**)
- **speed-up the dev process** because **no need to deploy** in-between changes?

---
![bg](./images/BizzSummitBackGround.png)

<hr/>

# Journey of FakeXrmEasy (FXE)

... and **so** In 2014 I **started working on FakeXrmEasy**...  

**YET**, **for a couple of YEARS** I was....

- working pretty much alone as a single contributor, **and**
- repeatedly told...  ..... guess what??

---
![bg](./images/BizzSummitBackGround.png)

<hr/>

# Journey of FakeXrmEasy (FXE)

... the **SAME** :)  

- "It's xRM man, **no one cares** about **quality** of the software"
- "Not **worth** it"
- "You're **wasting your time** man..."

---
![bg](./images/BizzSummitBackGround.png)

<hr/>

# Journey of FakeXrmEasy (FXE)

**BUT**, things started to change...  

- Met Raz and delivered (my first) **CRM Saturday** talk in Manchester, 2016
- There **were 4 people** attending
- Yes, you read that right :)

---
![bg](./images/BizzSummitBackGround.png)

<hr/>

# Journey of FakeXrmEasy (FXE)

**Next CRM Saturday in London**:   

- Over **100 attendees**...

---
![bg](./images/BizzSummitBackGround.png)

<hr/>

# Journey of FakeXrmEasy (FXE)

**Following CRM Saturday events**:   

- Zurich (Switzerland)
- Dubai (UAE)
- Manchester (UK)
- Madrid and Barcelona (Spain)
- Dallas, Texas (US)
- Kyiv (Ukraine)
- ...


---
![bg](./images/BizzSummitBackGround.png)

<hr/>

# Journey of FakeXrmEasy (FXE)

I'm very **proud**, that **TODAY**, more than **7 YEARS** later...   

### FakeXrmEasy Use 
- **2 M+ downloads**: [https://www.nuget.org/packages?q=FakeXrmEasy](https://www.nuget.org/packages?q=FakeXrmEasy)

- ~ 20% of **Microsoft Crm Sdk** downloads
- Used in **multi-million** dollar projects (many Fortune 100s included)

---
![bg](./images/BizzSummitBackGround.png)

<hr/>

# Journey of FakeXrmEasy (FXE)

I'm very proud, that **TODAY**, more than **7 YEARS** later...   

### FakeXrmEasy in books

(PHOTOS)

---
![bg](./images/BizzSummitBackGround.png)

<hr/>

# Journey of FakeXrmEasy (FXE)

I'm very proud, that **TODAY**, more than **7 YEARS** later...   

### FakeXrmEasy in MS Docs

(PHOTOS)

---
![bg](./images/BizzSummitBackGround.png)

<hr/>

# Journey of FakeXrmEasy (FXE)

I'm very proud, that **TODAY**, more than **7 YEARS** later...   

### FakeXrmEasy as a LinkedIn skill

(PHOTOS)

---
![bg](./images/BizzSummitBackGround.png)

<hr/>

# Journey of FakeXrmEasy (FXE)

I'm very proud, that **TODAY**, more than **7 YEARS** later...   

### Even JOBS asking for FakeXrmEasy exp...

(PHOTOS)


---
![bg](./images/BizzSummitBackGround.png)

<hr/>

# Journey of FakeXrmEasy (FXE)

I'm very proud, that **TODAY**, more than **7 YEARS** later...   

### And, finally, happy customers ... 

(PHOTOS)

- [https://dynamicsvalue.com/customer-stories](https://dynamicsvalue.com/customer-stories)


---
![bg](./images/BizzSummitBackGround.png)

<hr/>

# Moral of the Story ...

- **Don't listen** to naysayers...
- Be **consistent**   

---
![bg](./images/BizzSummitBackGround.png)

<hr/>

# Why?

## Increased developer efficiency

https://dynamicsvalue.com/white-paper


---
![bg](./images/BizzSummitBackGround.png)

<hr/>

# Evolution of Unit Testing in Dataverse

- **Level 0**: No mocks / unit tests (many companies, surprisingly, still here)
- **Level 1**: Manual mocks / fakse
- **Level 2**: In-Memory data-driven unit testing with FakeXrmEasy
- **Level 3**: Simulation: Azure functions + plugins firing In-Memory 

---
![bg](./images/BizzSummitBackGround.png)

<hr/>

# DEMO

## Scenario
- 

---
![bg](./images/BizzSummitBackGround.png)

<hr/>

# Code snippet ...



``` csharp
// Some code here
public class FakeXrmEasyTestsBase
{
    private readonly IXrmFakedContext _context;
    private readonly IOrganizationService _service;

    public FakeXrmEasyTestsBase() 
    {
        _context = MiddlwareBuilder.New();
        _service = _context.GetOrganizationService();
    }
}
``` 

---
![bg](./images/BizzSummitBackGround.png)

# Code snippet (II)

``` csharp
public class FollowupPlugin : IPlugin
{
    //Omitted for simplicity, please see the full source code above
}
```
# Quote styles

Some paragragraph with a `quote text here`. 
>Some quoted text here 

> Another Quote here

    Some indented text here
    Which continues

---
![bg](./images/BizzSummitBackGround.png)

# Other

###### heading 6

<!-- _class: swipe -->
###### Swipe


Some other text

---
![bg](./images/BizzSummitBackGround.png)
# Notes


<!-- Some presenter notes -->

