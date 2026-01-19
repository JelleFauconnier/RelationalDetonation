# Relational Detonation

A TouchDesigner/WikiData visualization project where you go on a real-time journey through the WikiData graph.

## Table of Contents

- [Overview](#overview)
- [Requirements](#requirements)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Components](#components)
- [Usage](#usage)
- [Optional Components](#optional-components)

## Overview

The system performs a live bidirectional search on Wikidata. 
Starting from two user-selected subjects, it traverses the graph simultaneously to find the shortest semantic link between them.
As the search progresses, blue spheres emerge from one side representing all Wikidata entries linked to the first subject. 
Red cubes appear on the opposite side for the second subject. 
They grow and expand until a path is found between them.
While the graph expands, images of discovered entries are flashed on screen in real-time. 
This creates a stream of visual data representing the ongoing search.

## Website

[https://relationaldetonation.jellefauconnier.ikdoeict.be/](https://relationaldetonation.jellefauconnier.ikdoeict.be/)

## Requirements

- TouchDesigner
- A decently powerful graphics card

## Installation

1. Clone this repository:
   ```bash
   git clone [repository-url]
   ```
2. Open `WIKIDATA.toe` in TouchDesigner.

## Project Structure

```
├── WIKIDATA.toe          # Main TouchDesigner project file
├── imageloading.tox        # Component for loading images
└──CRT_Filter.tox      # Optional component (see below)
```

## Components

### Image Loading (`imageloading.tox`)

This component takes a table DAT with a column 'image' and loads the corresponding images into a texture.

## Optional Components

### CRT_Filter (`CRT_Filter.tox`)

This component applies a CRT filter to the rendered image.
This component is optional and can be downloaded separately for additional functionality.

**What it does:**
Applies a CRT-style filter effect to the rendered output, giving it a retro aesthetic.

**How to install:**
1. Download the `CRT_Filter.tox` file from [this link](https://derivative.ca/community-post/asset/crt-tv-filter/68947)
2. Drag and drop into the root of your project folder
3. Leave a nice comment on the original post to thank the author!

## Usage

1. Open `WIKIDATA.toe` in TouchDesigner.
2. If you decide against installing the CRT_Filter component, remove the CRT_Filter node from the graph.
3. Run the project in perform mode by pressing F1.


---


