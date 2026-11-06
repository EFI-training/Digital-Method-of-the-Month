# Digital Method of the Month
![DMM Data Visualisation](./Images/DMM%20Data%20Vis.png)# Data Visualisation

# 06-11-2026

## Authors: Dr. Somya Iqbal (siqbal5@ed.ac.uk)

##  Schedule
- 14:00 : 14:15 - (**Talk**) Welcome and introduction
- 14:15 : 14:30 - (**Discussion**) Break down and evaluate some visualisations
- 14:30 : 14:45 - (**Talk**) Starting with data types & familiarising with visual variables
- 14:45 : 14:55 - (**Discussion**) what would you like to visualise and why?
- 14:55 : 15:00 - (**Q & A**) + complete the attendance & feedback form

 > Note: Questions welcome at any point

## Table of contents
- [Introduction & core concepts](#introduction--core-concepts)
  - [Why visualise your data?](#why-visualise-your-data)
  - [Guiding principles and associated works](#guiding-principles-and-associated-works)
  - [Visual variables, encodings and design choices](#visual-variables-encodings-and-design-choices)
- [Interactivity and embedding interactions into visualisations](#interactivity-and-embedding-interactions-into-visualisations)
- [Pitfalls and misrepresentations/misinterpretations](#pitfalls-and-misrepresentationsmisinterpretations)
  - [Common pitfalls](#common-pitfalls)
  - [Some playful examples](#some-playful-examples)
- [Best practices](#best-practices)
- [Programming tools for data visualisation](#programming-tools-for-data-visualisation)
- [Software tools with GUI (graphical user interface) - no-code options](#software-tools-with-gui-graphical-user-interface---no-code-options)
- [Community initiatives for data viz](#community-initiatives-for-data-viz)
- [Getting started with your own applied data visualisation](#getting-started-with-your-own-applied-data-visualisation)
- [Full reading list for theory and depth](#full-reading-list-for-theory-and-depth)
- [Other resources and links](#other-resources-and-links)


## Introduction & core concepts

**Note:** For those of you who want to focus on applied tools, jump to
[Programming tools for data visualisation](#programming-tools-for-data-visualisation)  or  [Software tools with GUI (graphical user interface) - no-code options](#software-tools-with-gui-graphical-user-interface---no-code-options)
If you are only interested in interactive visualisations jump to
[Interactivity and embedding interactions into visualisations](###interactivity-and-embedding-interactions-into-visualisations)

Visualisation is wide ranging domain, which can only be covered in brief overview. Each document section leads to further reading and principles for those interested in exploring the field at depth. 

### *Why visualise your data?*
When visualising data or information, what you are doing in essence is transferring knowledge that you have generated or engaged with to an audience of some kind. Typically one wants to tell a story about the data, the questions they asked of it, and what is revealed in the outcomes through exploration/analysis. Information in general can be used in the same way, for important messaging, to engage an audience, have them interact with a given reality associated with said information or to simply absorb the story. Knowledge transfer with added graphics can enhance communication with layers of data/information encoded into the design and can be tailored to best reflect the contents.

Core reading and video lectures on data visualisation for an introduction:
1. [Professor Tamara Munzner's work](https://www.cs.ubc.ca/~tmm/).

### Guiding principles and associated works
1. Understanding and best characterising your domain
- Domain characterisation refers to understanding your domain, the end viewers, and communicating in visual formats suitable to the domain (i.e. science or humanities, and further specifics). For instance in some fields certain colours carry meaning or denote context like down (green) and up (red) or the inverse for domains where red=bad/danger these details matter later when presenting visualisations. The wider premise of domain characterisation is to design *for* a given disciplinary context and audience you wish to communicate to.

2. Data abstraction

Data abstraction involves breaking down a few things:
- What are your data types: quantitative, ordinal or nominal?
- Does data require pre-processing, sub-setting, aggregating or formatting first?
- Can new composite values be formed for a clearer picture?
- Have data been transformed to the same scale and format? Is it understandable from the outset?
- Which questions were asked of the data?
- What is the main knowledge we want to transfer with the given data?
> *Quantitative*, *Ordinal* & *Nominal* data types.

3. Task abstraction

- What is your goal and the specified task for the visualisation, which related question have the data answered? Is the audience general or domain specific?

4. Encodings

Visual variables include features like, shape, hue (colour), size, and other dimensions. Have a look at how visual encodings relate to data types & charts here [Visual vocabulary](https://ft-interactive.github.io/visual-vocabulary/)
-> Credit: [Financial Times](https://github.com/Financial-Times/chart-doctor/blob/main/visual-vocabulary/). 
More details on visual variables in this section [Visual variables, encodings and design choices](###visual-variables,-encodings-and-design-choices) 

- Knowing the data types and task, bridges to the application of assigning visual encodings to these which best suit the goal. This section was drawn from work cited above (See [Professor Tamara Munzner](#professor-tamara-munzner) for the original reference on their nested model of visualisation design and steps.)

Note: Legends! Appropriate legends for simple or complex visualisations will convey details of your visual encodings to the viewer, these have similar criteria for clarity, conciseness, position, layer, and hue. 

### Visual variables, encodings and design choices

Mapping data types to visual encodings which best fit for graphical presentation:

Back to - quantitative, ordinal or nominal data types

**Bertin's ***visual variables*** & semiology of graphics:**

![Bertin's Visual Variables](./Images/BertinsVisualVariables.png)

[Read more about the visual variables](https://towardsdatascience.com/data-visualization-explained-part-2-an-introduction-to-visual-variables/)
[Semiology of graphics](https://countersubject.biz/wp-content/uploads/2024/08/Semiology-of-Graphics-Diagrams-Networks-Maps-Jacques-Bertin-Z-Library.pdf) PDF book
> Credit: Bertin, J., 1983. Semiology of graphics. University of Wisconsin press. Original: Bertin, Jacques. 1967. Sémiologie graphique: Les diagrammes, les réseaux, les cartes. Paris: Editions Gauthier-Villars.
Jacques Bertin was a cartographer and developed the foundational ideas around visual variables, read more here [Jacques Bertin](https://www.mappingasprocess.net/blog/2021/8/20/some-thoughts-on-jacques-bertins-cartographic-semiology)

**Mackinlays visual rankings:**

![Mackinlay’s Rankings](./Images/Mackinlays%20rankings.png)
> Credit: Mackinlay, J., 1986. Automating the design of graphical presentations of relational information. Acm Transactions On Graphics (Tog), 5(2), pp.110-141.

Mackinlay built on Bertin's early work and created ranking of items, where users can choose the most effective encodings by data type. 


**The Grammar of Graphics - Foundational work and core ideas**.
> Wilkinson, L., 2011. The grammar of graphics. In Handbook of computational statistics: Concepts and methods (pp. 375-414). Berlin, Heidelberg: Springer Berlin Heidelberg.

### **Interactivity and embedding interactions into visualisations**
Some people wish to use interactivity in their data visualisation design. Most common tools for interactive visualisation require some programming skills. Some of the features that can be incorporated into custom setups for dashboards or interactive exploration of data include (non-exhaustive):

- Click - where you can click an item to get more descriptives.
- Hover - an interaction where you hover over a point and often get a readout window to see more information (adds some details without adding clutter).
- Highlight - Selecting a portion of a visualisation to focus on an area, adds an element like changing colour, opacity, or an outline when you use this interaction.
- Containment - Creating a contained area on a visualisation to focus on that section, this creates boundaries and groups items.
- Zoom/Pan - This function allows for wider pan and closer looks at large or detailed visualisations, increases granularity. 
- Brushing and linking - connects datasets and their features.
- Overview + detail - allows you see the wider visualisation, and to focus  on specific details.

These interactions are all dependent on how one designs them into a visualisation and multiple possibilities are available. Notably, it is sensible to consider which of these ADD to the visualisation by offering further insight, therefore there needs to be a task and goal for such design. 

## Interactivity in visualisation

Interactivity allows viewers to explore a visualisation rather than only look at a fixed image.

Common interactions include:

| Interaction | What it does | Example using map via Leaflet |
|---|---|---|
| **Click** | Select an item or open details | Click a map marker to show a popup |
| **Hover** | Show lightweight information | Hover over a chart point to see year/count |
| **Zoom and pan** | Move around a large view | Navigate the Leaflet map |
| **Filter** | Show a subset of the data | Filter by date, category, or location |
| **Highlight** | Emphasise selected items | Highlight records from a chosen year |
| **Brushing and linking** | Connect selections across views | Select a timeline range and update the map |
| **Overview and detail** | Show the whole dataset and local detail | Map overview plus popup detail |

Interactivity should have a purpose.

It is most useful when it helps the viewer:

- inspect details without cluttering the whole page;
- move between overview and detail;
- compare subsets;
- follow their own research question.

It is less useful when it adds complexity without improving understanding.

Interactive data visualisation is becoming increasingly adopted where data use requires ranges and scope beyond single use, includes exploration of data, and can be used for teams, presentations, national intitives across fields.

The below examples show two types of interactive visualisation designs to explore and dig into data, take a look and explore the features:

- > [Plotly Python example - Bubble map](https://plotly.com/python/bubble-maps/) 

- >  [Kindred Britain](http://kindred.stanford.edu/#) – an interactive historical network visualising relationships among 30,000 notable British figures, blending biography, culture, and data design. Give it a try, it has many of the features described above.  Read more about this excellent visualisation by scrolling down the information linked here [KindredBritain Further info & credits](https://kindred.stanford.edu/notes.html) Kindred Britain was created by Nicholas Jenkins, Elijah Meeks, and Scott Murray, at Stanford University.

### Pitfalls and misrepresentations/misinterpretations

#### *Common pitfalls*
- Axis scaling - Has the visualisation used an axis scale accommodating the range of the data? values?
- Selective presentations -  are any data points or features obscured or truncated due to visual encoding or scaling?
- Misleading encodings - Has the incorrect visual variable been used to encode a data point, for example area for one dimensional quantities or using colour for categorical data (this would get messy very quickly)?
- Visual clutter - are there too many colours, labels and marks which takes away a viewers attention
- Convoluted layouts - is the spatial arrangement confusing?
- Considering colour blindness/ & perceptual difficulties - you can consider sizing, colour palettes, alt text. 
- Unsuitable data! Is the data suitable for the question asked? If data is incomplete then visual clarity cannot compensate. 

#### Further resources
1. [Edward Tufte on Chartjunk](https://www.edwardtufte.com/notebook/chartjunk/). Edward Tufte was an advocate of clarity and decluttering of visualisations, and commented on the data-to-ink ratio. 

Tufte’s principles are invaluable for keeping visualisations clear and uncluttered, but they do not mean you cannot include expressive elements when context calls for them. Work in areas like data physicalisation and affective visualisation shows that design can convey emotion and meaning as well as information. For instance, when communicating topics that require urgency or action, such as climate or health issues, careful use of colour and symbolism can strengthen impact. These alongside the use of infographics for data representation move beyond traditional graphics to explore how data can be represented in more embodied or emotional ways.

#### Some playful examples: 
1. [Dragon Ball Z](https://dragonballz.visualcinnamon.com/) All of the fights from Dragon Ball Z visualised by Nadieh Bremer (Go to projects on this link and view some visualisations) -> [Data Sketches](https://www.datasketch.es/)

2. [Mapping the Republic of Letters](https://republicofletters.stanford.edu/) is a major Digital Humanities project that explores correspondence networks across space and time.

It is useful for thinking about:

- correspondence;
- networks;
- geography;
- historical movement;
- distant reading;
- the relationship between maps and archives.

3. [Kindred Britain](http://kindred.stanford.edu/) is an interactive network visualisation of relationships among thousands of British historical figures.

It is useful for thinking about:

- networks;
- biography;
- cultural history;
- interaction;
- public-facing Digital Humanities design.

Further information:

[Kindred Britain notes and credits](https://kindred.stanford.edu/notes.html)

4. W. E. B. Du Bois and collaborators created powerful hand-drawn data visualisations for the 1900 Paris Exposition.

These works are useful for thinking about:

- visualisation and social justice;
- design and argument;
- colour and form;
- historical data storytelling;
- visualisation before computers.

[Library of Congress: W. E. B. Du Bois data visualizations](https://www.loc.gov/pictures/search/?st=grid&co=anedub)


## Best practices
1. Understand the data and types first
2. Consider story and audience
3. Consider scaling and aggregated data, or single focus views
3. Encode effectively with consideration for simple and clear variable representations (visual variable to data type)
4. Choose chart formats and colour palettes that suit the number of items, the target audience, and ensure clear representations
5. Ensure legends match visual elements relating to data features, are well placed and readable. 
6. You don't have to use one chart to capture all of your data, consider linking sub charts to dive in from an overarching visualisation.

- [Fell In Love With Data Blog](https://filwd.substack.com/)

## Programming tools for data visualisation

A non exhaustive list

- [Seaborn, Python](https://seaborn.pydata.org/)
- [Matplotlib, Python](https://matplotlib.org/)
- [GGplot, R ](https://ggplot2.tidyverse.org/) based on the Grammar of Graphics
- [Tidyverse](https://tidyverse.org/)
- [D3.js javascript](https://d3js.org/what-is-d3)
- [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) Structuring a web page 
- [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)  Styling a page 

Interactive data visualisation tools:
- [Plotly, Python](https://plotly.com/python/)
- [Bokeh](https://bokeh.org/)
- [D3.js javascript](https://d3js.org/what-is-d3)
- [Vega-Lite](https://vega.github.io/vega-lite/)

Larger projects may use web development frameworks. These are useful when a project needs reusable components, multiple pages, state management, or a more complex interface.

| Framework or library | Useful for |
|---|---|
| [React](https://react.dev/) | Building component-based user interfaces |
| [Vue](https://vuejs.org/) | Building approachable, flexible web interfaces |
| [Svelte](https://svelte.dev/) | Building compiled, component-based web interfaces |
| [Observable Framework](https://observablehq.com/framework/) | Building data apps and reports with JavaScript and Markdown |

A framework is not always necessary. For a smaller projects plain HTML, CSS, JavaScript, D3, and Leaflet are easier to understand and work with.

## Software tools with GUI (graphical user interface) - no-code options
- [Tableau](https://www.tableau.com/en-gb) based on the Grammar of Graphics
- [Charticulator](https://donghaoren.org/charticulator/)
- [Flourish](https://flourish.studio/) | Interactive stories, charts, and maps |
- [Datawrapper](https://www.datawrapper.de/) | Clear charts, maps, and tables for publication |
- [Figma](https://www.figma.com/) | Designing interfaces, wireframes, prototypes, layout mockups, and visualisation concepts before coding |
- [Rawgraphs](https://www.rawgraphs.io/)

## Community initiatives for data viz
*Getting involved*

- [MakeoverMondays](https://makeovermonday.co.uk/)
- [Tidy Tuesday](https://github.com/rfordatascience/tidytuesday/blob/main/README.md)

## Getting started with your own applied data visualisation

Have data? Great, start breaking down the data types, visual variables to match, and go from there for your visualisation design! Try starting with a sketch or drawing, and keep an eye on the task the visualisation is performing as well as your goal with the data. 
When starting your own visualisation, try this sequence.

### 1. Define the question

Ask:

```text
What do I want someone to understand, explore, or question?
```

### 2. Inspect the data

Ask:

```text
What fields/variables do I have?
What types of variables are they?
What do I want to ask of the data?
Who is my audience?
What is missing?
What has been cleaned or transformed?
```

### 3. Identify the data types

Ask:

```text
Which fields are dates?
Which fields are places?
Which fields are categories?
Which fields are numbers?
Which fields describe relationships?
```

### 4. Choose a visual form

| If your question is about... | Think about... |
|---|---|
| Change over time | Timeline, line chart, area chart |
| Place | Map |
| Relationships | Network diagram/Sankeys/Connections
| Categories | Bar chart, grouped chart |
| Parts of a whole | Stacked bar chart, treemap, carefully used pie chart |
| Distributions | Histogram, dot plot, box plot |
| Individual records plus detail | Map markers, table, popups, linked views |

### 5. Sketch before coding

Try out the 5 design sheet approach and start with a sketched prototype: [5 Design Sheet](https://towardsdatascience.com/five-design-sheet-methodology-approach-to-data-visualisation-603d760f2418/)

Want to get some data? Many available datasets but you can also responsibly scrape some data from the web
1. [Beautiful soup, Python](https://www.crummy.com/software/BeautifulSoup/)

Or try some data from the data visualisation community:

2. [MakeoverMonday Data Links](https://makeovermonday.co.uk/)

## Full reading list for theory and depth:

- [Royal Statistical Society: Best Practices for Data Visualisation](https://royal-statistical-society.github.io/datavisguide/)
- [Tamara Munzner — Visualization Analysis and Design](https://www.cs.ubc.ca/~tmm/vadbook/)
- [Tamara Munzner — Research group](https://www.cs.ubc.ca/~tmm/)
- [Alberto Cairo — The Truthful Art](https://www.oreilly.com/library/view/the-truthful-art/9780133440492/)
- [Edward Tufte — Chartjunk](https://www.edwardtufte.com/notebook/chartjunk/)
- [John Mackinlay, 1986 — Automating the design of graphical presentations](https://dl.acm.org/doi/10.1145/22949.22950)
- [Johanna Drucker - Digital Humanities Quarterly - Humanities Approaches to Graphical Display](https://dhq.digitalhumanities.org/vol/5/1/000091/000091.html)

### Visualisation Labs & Teams (non-exhausive)
- [UCLAB](https://uclab.fh-potsdam.de/)
- [uw Interactive Data Lab](https://idl.uw.edu/)
- [VisHub - University of Edinburgh](https://vishub.net/)
- [Data Visualisation Society](https://www.datavisualizationsociety.org/)
- [giCentre](https://www.gicentre.net/)
- [Georgia Tech Visualisation Lab](https://vis.gatech.edu/)
- [MIT visualisation Lab](https://vis.mit.edu/)

### Articles and write-ups on visualisation

- [UW Interactive Data Lab](https://medium.com/@uwdata/next-steps-for-data-visualization-research-3ef5e1a5e349)

### Design, critique, and storytelling

- [Nightingale: Journal of the Data Visualization Society](https://nightingaledvs.com/)
- [Data Visualization Society](https://www.datavisualizationsociety.org/)
- [The Pudding](https://pudding.cool/)
- [Visual Cinnamon](https://www.visualcinnamon.com/)
- [FlowingData](https://flowingdata.com/)

### Visual vocabularies and chart choice

- [Financial Times Visual Vocabulary](https://ft-interactive.github.io/visual-vocabulary/)
- [Data Visualisation Catalogue](https://datavizcatalogue.com/)
- [Chart Maker Directory](https://chartmaker.visualisingdata.com/)
- [Datawrapper Academy](https://academy.datawrapper.de/)
## Other resources and links
1. [Information is beautiful](https://informationisbeautiful.net/)
2. [The Chart Maker Directory & associated tools](https://chartmaker.visualisingdata.com/)
3. [Dear Data project](https://www.dear-data.com/theproject)
4. [VisHub Edinburgh](https://vishub.net/)
5. [Material Design - Overview of data visualisation](https://m2.material.io/design/communication/data-visualization.html#principles)
6. [Summarised article on the topics above](https://towardsdatascience.com/a-comprehensive-guide-to-the-grammar-of-graphics-for-effective-visualization-of-multi-dimensional-1f92b4ed4149/)

Much of the content for this document was inspired by early tuition from University of Edinburgh Fellow Dr Shane Sheehan [See his work](https://scholar.google.com/citations?user=z4FMYRMAAAAJ&hl=en)


[![License: CC BY-NC 4.0](https://licensebuttons.net/l/by-nc/4.0/80x15.png)](https://creativecommons.org/licenses/by-nc/4.0/)






