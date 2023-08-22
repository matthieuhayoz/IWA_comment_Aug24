---
title: "Comment on IWA MRV Version for Public Comment June 2023"
author: "Christiaan Pauw, Alex Howard"
date: "2023-08-22"
output: 
  html_document: 
    keep_md: yes
---
\clearpage

```{=tex}
\pagenumbering{roman}
\tableofcontents
%\listoffigures 
%\listoftables
\newpage
\pagenumbering{arabic}
\clearpage
```

\clearpage

<!--

# General

Underlying premise: Agents engage in activities that impact environments.

Hyperledger Climate Action and Accounting SIG

Hedera Vocabulary Group

Not description of the system as it is, but what it could become ...

As long as the specification as a mere description of the current state of affairs, ...

-->


# Suggested changes

## Differentiate between agents and activities

### Problem

The term *EP* confounds three elements: the coordination of a series of activities, the implementation of an activity, and a legal entity implementing/conducting an activity.

There is an ambiguous element in the definition of an *EP* because *EP* is used to refer to a project, a programme, or the entity coordinating the programme / executing the activity:

> "...an EP can represent a single farm that will want to have a project that makes carbon removal claims and another that will make water claims. Each claim type is associated with a different Quality Standard and will result in different credit types being issued, but are managed by a single organization."

> "Or an EP can represent an organization that will host multiple MBPs in different geographic locations, like solar deployments in different countries or states."

In impact accounting in general, there is a clear difference between *project* and *programme*. This can be seen in the CDM Glossary (see e.g., version 11.0 p3, footnote 1). A *programme* is a series of coordinated activities that share a defined goal. The project activities thus coordinated are sometimes referred to as component project activities. The scope of a programme is larger (in time, space and impact objective) than that of a single component project activity. 

Environmental impacts emanate from an activities. 

### Suggested solution

**Differentiate the project as an agent (i.e., a natural or legal person) from the project as an activity:** Following the GHG Protocol, CDM and others, explicitly refer to the *project activity* when the activity is meant and to the *project implementer* or equivalent when the natural or legal person who carries out the project activity is referred to (during the design and approval phase; prior to execution of the project activity, the term  *project proponent* may be used). 

**Differentiate a programme from a project activity:**
A programme is different from a project activity by virtue of a programme being a coordinated series of project activities who share in the objective of the programme. The activity of a programme is coordination and facilitation of the component project activities. A programme may have an indeterminate duration, whereas a project is per definition of limited duration. 

We propose that, following the CDM and GHG Protocol, the term *project activity* (*PA*) is used where that is meant. 

We propose that a *programme* is defined as separate from a *project*. The definition for a *programme of activities* (PoA) in the CDM Glossary may be a helpful starting point: 

> "A voluntary coordinated action by a private or public entity which coordinates and implements any policy/measure or stated goal (i.e. incentive schemes and voluntary programmes) that leads to GHG emission reductions or net anthropogenic GHG removals by sinks that are additional to any that would occur in the absence of the PoA, via an unlimited number of CPAs."

### Implications of proposed solution

Consistently using the term *project activity* where that is meant (e.g., as it is done in the CDM) will lead to greater clarity. How an EP is tokenised may have to be reworked. E.g., one has to think if an activity is burnable, divisible and transferable. 

A separate specification of the legal entity who implements a project activity must be provided.

The properties of a *project activity* are at least:



The properties of a *project implementer* are the same as that of a natural or legal person, with additional reference to the project activity. A *project implementer* is divisible and transferable in the same way as shares are held and sold in other businesses. 







## Replace term 'MBP' with 'Activity' and replace 'Ecological Claim' with 'Impact Claim' 

### Problem

The concept of an MBP can be further refined to avoid any possible confusion. From its intended use, it is clear that an MBP is a *claim* about about the relationship between a *project activity* and a resulting *environmental state change* that follows a *calculation method* and is subject to one or more *quality standards*. 

<!-- An MBP is a structure linking an activity and an environmental state change, by packaging one or more claims that the activity caused the state change, along with data supporting those claims, and results of verification performed on those claims and their data. -->



The current definition is somewhat ambiguous as far as the relationship between the project activity and the  resulting environmental state change is concerned. 

>  "A Modular Benefit Project, is a ‘child’ of an Ecological Project, and serves as the system of record for the actual type of project work that generates a benefit being measured."

If the phrase *'the actual type of project work that generates a benefit* refers to the project activity, it would establish a one-to-one relationship between activities and the quantified benefits. <!-- That is exactly what they are trying to do --> In reality, the relationship between an activity and its effects is one-to-many: a single activity can  bring about changes in multiple environments or effect multiple parameters of a single environment. If the phrase was meant to refer to the act of quantification (although that does not seem to be the grammatical sense), it is an unfortunate formulation which leads to confounding the act of bringing about an environmental state change with the act of gathering and presenting evidence for the relationship between an activity and an environment state change. In both interpretations the P in MBP is misplaced.  

In addition, there is every reason not to limit environmental accounting only to benefits. The B can therefore be replaced by a I (for impact). In fact, many activities are trade-offs between benefits in one dimension and negative impact in another.  

 <!-- "An Ecological Project/Program (EP) can have multiple MBPs, where each MBP represents the type of ecological claim being issued. This is where the evidence is provided for issuing one or more claims about beneficial impact such as a claim of carbon removal.For example, an EP may want to create claims for carbon removal and water, thus having an MBP for each. An MBP must be validated before it can begin submitting claims for verification." -->

### Solution 
 
Clearly delineate **Activity** as a separate core class not confounded with *Agents* (natural or legal persons) or environmental state changes (impact). The idea of a *project activity* is central to project accounting and should be clearly defined. The GHG Project Protocol or the CDM Glossary provides helpful reference material for defining a project activity. Within the context of a programme of activities, a term similar to *component project activity* can be considered.  Within an organisational accounting context, an onging activity can be referred to as an *operation*. 
<!-- "Operation" may be problematic. -->

Make it clear that impacts are connected to activities and that *impact claims* connect environmental state changes to activities following a quantification method subject to one or more quality standards. 

An implementation of our proposed changes to the definition of an MBP on p.8 of the original document is given below.

Current:
**Modular Benefit Project (MBP)** 

>  An Ecological Project/Program (EP) can have multiple MBPs, where each MBP represents the type of ecological claim being issued. This is where the evidence is provided for issuing one or more claims about beneficial impact such as a claim of carbon removal.
For example, an EP may want to create claims for carbon removal and water, thus having an MBP for each. An MBP must be validated before it can begin submitting claims for verification.

Proposed:
**Activity Impact Module (AIM)** 

>  An ecological Project Activity (PA) be associated with multiple impacts. Each quantifiable impact is represented by an AIM, which is a claim about the impact of the PA on the state of particular environment made according to a particular quantification method.  
For example, an project operator may want to create claims for carbon removal and water benefits related to a particular project activity, and will thus have an AIM for each. An AIM must be validated before the project operator can begin submitting claims for verification.


<!-- 
Replace 
      "Ecological Project",   "Modular Benefit Project"  and "Ecological Claim"
with
      "Project Operator",       "Project Activity"         and "Impact Claim"

Show how this works for both the project scenario and the PoA scenario.
-->


### Implications of proposed solution

The proposed change will allow for a more realistic one-to-many relationship between activities and their impact and disambiguate the relationship between and activity and the owner of an activity (i.e., the natural or legal person to whom the digital assets to be issued will belong). 






## Make framework usable outside of the project environment 

In the context where environmental benefits will be used to offset negative environmental impacts, it is crucial that the accounting for environmental assets and environmental liabilities be done in the same way. With fairly minor reworking, following the changes proposed, the specification can be made useful for corporate accounting and then further for offset accounting. 







## Refine the definitions of the verification process 

### Potential 

Validation & Verification Body (VVB) can be described in such as way as to make use of possibilities created by digital technologies that was not in use before. This means that the focus must be on the validation & verification function and not on the V&V body. Defining the V&V function as part of the specification will enable solutions like specialisation, V&V micro-services and even the use of algorithmic V&V.

### Proposal 


**Change terminology of VVB to VVE**

**Change "organization" to "person or organization" or "natural or legal person"**


<!--


#### Differentiate the validation and verification process  

VVB vs VVP

VV as activity 


#### There is no reason why a VVB cannot also be a natural person

### Implications of proposed solution

Validation and Verification is, in our opinion, one of the least efficient components of the voluntary carbon market, not least because it is an oligopoly. A specification making it atomise the validation and verification process may enable a new paradigm from validation and verification (e.g, V&V micro services)
-->

## Dissolve the concept of co-benefits

