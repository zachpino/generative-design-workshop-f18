# Week 2 · Parametric Rigs

This week, let's discuss how we as designers can fully *parameterize* a specific opportunity into a set of dimensionable, flexible, understandable, and ultimately manufacturable or implementable aspects. This approach has much in common with traditional design and engineering methods, though differs meaningfully in its intentionality and expression.

-----

### References for the Week

- [Tylko Bookshelves](week1-sculpting-data.pdf)
- [Article on Tylko with Founder Interview](https://www.curbed.com/2015/6/24/9946872/tylko-furniture-app-augmented-reality)
- [Floyd](https://floydhome.com/products)
- [De-Sk](https://de-sk.co/buy)
- [Radiolaria by Nervous System](https://n-e-r-v-o-u-s.com/projects/albums/radiolaria-2/)

-----

### Parametric Rigs

A critical phase in any generative design approach is the creation of a parametric rig. A parametric rig is the determination of the *designable* and *intentional* aspects of a product, service, or experience. It is important that these aspects all be given names, and have a known degree of flexibility.

When parameters are fully determined, we should then have a skeleton of the product to be. Playing with the parameters should allow a designer to see the full expression of their design — the constellation of all products that might result from their design intent.

![breeding tables](http://www.kramweisshaar.com/media/projects/breeding_tables/KRAM_WEISSHAAR_BREEDINGTABLES_Algorithm_Output_Diversity.jpg)

It is easiest to consider physical products when implementing parametric rigs. For example, the simple parameters of a ceramic cup might be total height, radius/diameter at top, radius/diameter at bottom, foot height, and wall thickness. It is often the case that the simple parameters of a product align with what would be defined in a standard engineering drawing.

![cup simple parameters](cup.png)

More complex parameters might allow for material selection, overall (non-conic) shape, handle shape and size, lip geometry, styling and surface finish...

-----

### Types of Parameters

- Flexible : The parameter is entirely free (a shoe could be *any* length)
- Categorical : The parameter is allowed to be any member of a set of fixed values (a table could be a *circle*, a *hexagon*, or a *square*)
- Fixed : The parameter has a set value that cannot change (a fork must have *four* tines)
- Dependent : The parameter is algorithmically calculated or determined based on other parameters (the width of a car is *exactly half* its length)

Further, any of the above parameter types may be *optional*, and need not always be numbers!

-----

### Grasshopper Definition

Let's take a look at how a table like [De-Sk](https://de-sk.co/buy) could be parameterized and recreated in Grasshopper.

[Download](desk-generator.gh)

![Grasshopper Definition](grasshopper.png)

![desks](desks.png)

What other parameters could we imagine implementing? 

-----

### Homework

Let's see how today goes! 