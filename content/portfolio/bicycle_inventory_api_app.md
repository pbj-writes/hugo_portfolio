---
paige:
  style: |
    #paige-breadcrumbs
---
# Bicycle Inventory API App
> **NOTE**  
> In progress. I'm working on developing some sweet mermaid skillz to create design and data model diagrams. Also, I'm intending to embed a demo video.

## Introduction

I wanted to gain a deeper understanding of APIs and demonstrate my API doc skills, so I set out to create a data-driven API application. I started with an idea to track all of my current and former bicycles. I knew that I could easily (but sloppily) design a bicycle data table. And from this point, I did a lot of searching.

## Tools
### Database
I can write SQL but I needed a solution to host my db online in the cloud. I came across [https://elephantsql.com](https://elephantsql.com). They offer to host a limited, but free, Postgres database instance.

### API server and code platform for APIs
I'm not a developer so finding how to write some basic APIs was intimidating, but after some [next-level](../../resume/#syracuse-university-) internet searching, I found a [step-by-step guide](https://dev.to/fredabod/a-step-by-step-guide-to-using-elephantsql-with-nodejs-and-express-2e9f) for using ElephantSQL with Node.js and Express. 

### IDE
[Visual Studio Code](https://code.visualstudio.com).

### API Platform
[Postman](https://www.postman.com)

## Design
> **TODO**  
> Learn mermaid and create a design artifact.

## Data Model
### SQL
{{< paige/code
    lang="sql" >}}
-- create the bicycles table with a few bicycle attributes.
CREATE TABLE bicycles (
    bicycle_id	SERIAL PRIMARY KEY,
    make varchar(50),
    model varchar(50),
    groupset varchar(50),
    frame_type varchar(50),
    frame_size varchar(50),
    prime_color varchar(50),
    model_year int,
    crank_length varchar(50)
);

-- add the four road bikes that I've ever owned.
INSERT INTO bicycles (make, model, groupset, frame_type, frame_size, prime_color, model_year, crank_length)
VALUES
('Specialized', 'Sequoia Sport', 'Shimano Sora', 'aluminum', '60cm', 'silver', '2003', '175mm'),
('Cannondale', 'CAAD8', 'Shimano Tiagra', 'aluminum', '58cm', 'white', '2014', '172.5mm'),
('Cannondale', 'CAAD13 Disc Rival AXS', 'Rival eTAP', 'aluminum', '58cm', 'purple', '2021', '175mm'),
('Cannondale', 'Topstone 4', 'microSHIFT Advent 10', 'aluminum', 'large', 'alpine', '2021', '175mm');
{{< /paige/code >}}

> **TODO**  
> Learn mermaid and create a data model artifact.

## Demo
> **TODO**  
> Record, post, and embed a demo.
