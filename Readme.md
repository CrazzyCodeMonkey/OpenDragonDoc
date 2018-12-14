# Open Dragon Doc

## Purpose

This repository will describe a standard way to document CFML code, Open Dragon Docs (ODDoc)

## Inspiration

There are a lot of different ways to implement blocks of code in CFML, and some of those ways can be very obscure.  This repository will not describe how to write or structure code, but will provide standard format for how to document CFML code.

Java has JavaDocs, and JavaScript has JSDoc and YUIDoc, Open Dragon Doc is an attempt to solve that problem for CFML

## Blocks to be documented

Below are the major blocks of a CFML application that this will allow you to document

* CFML Page
* User Defined Function
* Custom Tag
  * Domain Specific Language tags
  * Content generating tags
* Cold Fusion Components
  * Component Functions

## More than comments

In addition to a coding standard, ODDoc will provide a set of CFML files for parsing CFML files to render readable documenations pages.  Additionaly this application will be able to lint and verify adherance to the ODD standard.

## Getting Started

All ODDoc will follow a basic structure with that embends them inside of comment blocks `/** ... */`.  Content that requires documentation outside of a CFScript area, the ODDoc comment block can be embeded in a CFML comment block `<!--- --->`.  All subsequent line in the ODDoc should start with a `* `.

### Basic structure

The format of a ODDoc can be broken into a couple areas
* Short Descriptionhttp://www.strategicemployment.com/jobs.html#/job-details/Job-8578-sp
* Long Description
* Explanation
* Tags
* Example

#### Short Description
This is a 1 line description of of what the documented block is.

#### Long Description
This is a single HTML tag worth of content to describe in more detail the documented block

#### Explanation
Additional content should be broken with html br tags and will be grouped together as paragraphs

#### Tags
Tags are structured pieces of data about the block being documented.  This will always begin with an `@` immediately followed by a word and any additional information

#### Example
The Example code will be started with `@example` tag, and all following content will be treated as example code.

## Tag Definitions

| Tag & Parameters | Usage | Applies To | Since |
| --- | --- | --- | --- |
| **@page** _url_      | Used to the absolute url define a url accessible page | CFML pages | v0.0  |