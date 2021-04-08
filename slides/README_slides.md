---
jupyter:
  jupytext:
    text_representation:
      extension: .md
      format_name: myst
      format_version: '1.1'
      jupytext_version: 1.1.0
  kernelspec:
    display_name: Python 3
    language: python
    name: python3
---
<!-- 
+++ {"slideshow": {"slide_type": "slide"}}

# Tutorial slides

- Slides are optional (e.g., you may not use them if your presentation is via live coding).
- If the pre-recorded presentations will use slides, we request that you deposit the slides in this folder.

+++ {"slideshow": {"slide_type": "slide"}}

## Use text-based source

- We ask that you use text-based formats for your slides, e.g., markdown 
- This markdown file is an example source for slides using `nbconvert` and Reveal. See the GitHub action '.github/workflows/slides.yml' in this repo so see how this markdown file is converted to a HTML slide show and published on GitHub Pages - https://fawazsiddiqi.github.io/slides_to_pages

+++ {"slideshow": {"slide_type": "subslide"}}

## An example sub-slide

- Another option: you can write your slide content using markdown and use an app for slide design, like [Deckset](https://www.deckset.com) or similar.

+++ {"slideshow": {"slide_type": "slide"}}

## Naming convention and file list

- Use a **naming convention** where each file name starts with a number, reflecting the order of use in the presentation of the tutorial.
- List your slide files in a markdown, with a brief description.


+++ {"slideshow": {"slide_type": "slide"}} 
-->


**🌟 Overview** <br />
This tutorial provides a solution starter that shows you how to provision a prototype Climate Impact Rating system that supports consumer APIs.

🎓 What will you learn? <br />
This tutorial provides a solution starter that shows you how to provision a prototype Climate Impact Rating system that supports consumer APIs. The tutorial provides a basic architecture for you to experiment with building out additional climate rating components and includes: <br />

- A CouchDB NoSQL database layer holding both individual product ratings. <br />
- A basic API server that allows data to be inserted and extracted from the database. This API is expressed as an OpenAPI (Swagger) document, so you can build your own clients. <br />
- Deployment tools to stand up the above on the IBM Cloud, within the free-tier plan. <br />

👩‍💻 Who should attend? <br />
- Students who are interested in AI, Data Science but don't know where to start
- Data Science & AI enthusiasts who want to learn what IBM is doing
- Professional Developers who want to know more about the world of Data & AI

+++ {"slideshow": {"slide_type": "subslide"}}

🎙️ Speakers <br />
- Anam Mahmood, IBM Developer Advocate, https://www.linkedin.com/in/anam-mahmood-sheikh/
- Mridul Bhandari, IBM Developer Advocate, https://www.linkedin.com/in/mridul-bhandari

🎈 Prerequisites <br />
☁ Register for a free IBM Cloud Account: https://ibm.biz/ArabAISummit <br />
☁ Complete this 3 question anonymous survey: https://ibm.biz/ArabAISummit-Survey 

🍉 Register for the live stream: <br/>
https://www.runtheworld.today/app/invitation/19465

👩‍💻Resources <br />
- GitHub Repository - https://ibm.biz/ClimateImpact
- Workshop Slides - https://Anam-Mahmood.github.io/Solution-Starter-Kit-Energy-2020/#/
- Survey - https://ibm.biz/ArabAISummit-Survey 
- Meetup page - https://www.meetup.com/IBM-Cloud-MEA/events/ 

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/Anam-Mahmood/Solution-Starter-Kit-Energy-2020/blob/master/images/slide_images/Slide1.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/Anam-Mahmood/Solution-Starter-Kit-Energy-2020/blob/master/images/slide_images/Slide2.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/Anam-Mahmood/Solution-Starter-Kit-Energy-2020/blob/master/images/slide_images/Slide3.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/Anam-Mahmood/Solution-Starter-Kit-Energy-2020/blob/master/images/slide_images/Slide4.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/Anam-Mahmood/Solution-Starter-Kit-Energy-2020/blob/master/images/slide_images/Slide5.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/Anam-Mahmood/Solution-Starter-Kit-Energy-2020/blob/master/images/slide_images/Slide6.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/Anam-Mahmood/Solution-Starter-Kit-Energy-2020/blob/master/images/slide_images/Slide7.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/Anam-Mahmood/Solution-Starter-Kit-Energy-2020/blob/master/images/slide_images/Slide8.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/Anam-Mahmood/Solution-Starter-Kit-Energy-2020/blob/master/images/slide_images/Slide9.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/Anam-Mahmood/Solution-Starter-Kit-Energy-2020/blob/master/images/slide_images/Slide10.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/Anam-Mahmood/Solution-Starter-Kit-Energy-2020/blob/master/images/slide_images/Slide11.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/Anam-Mahmood/Solution-Starter-Kit-Energy-2020/blob/master/images/slide_images/Slide12.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/Anam-Mahmood/Solution-Starter-Kit-Energy-2020/blob/master/images/slide_images/Slide13.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/Anam-Mahmood/Solution-Starter-Kit-Energy-2020/blob/master/images/slide_images/Slide14.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/Anam-Mahmood/Solution-Starter-Kit-Energy-2020/blob/master/images/slide_images/Slide15.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/Anam-Mahmood/Solution-Starter-Kit-Energy-2020/blob/master/images/slide_images/Slide16.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/Anam-Mahmood/Solution-Starter-Kit-Energy-2020/blob/master/images/slide_images/Slide17.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/Anam-Mahmood/Solution-Starter-Kit-Energy-2020/blob/master/images/slide_images/Slide18.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/Anam-Mahmood/Solution-Starter-Kit-Energy-2020/blob/master/images/slide_images/Slide19.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

## License

**Recommend** that slides be shared under a [CC-BY](https://creativecommons.org/licenses/by/4.0/) license.
