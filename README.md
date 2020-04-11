<h1>OTTO</h1>
## The automated micropipette

OTTO is an open-source liquid handler that can automatically prepare samples for qPCR, flow cytometry, and other biological assays that rely on accurate liquid dispensing. It features designs that optimize speed and accuracy, unattended automation, and modular components, all with easily sourceable or 3D-printed parts. In total, OTTO only costs approximately $1000 and works with most commercially available micropipettes and plastic labware, so you can use materials you already own.

<iframe width="560" height="315" src="https://www.youtube.com/embed/qub5chyIQ0s" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

We created an interactive 3D model of OTTO, hosted by Onshape, to make it easy to see how all of the mechanical components fit together physically: 

<iframe src="https://myhub.autodesk360.com/ue29183a6/shares/public/SH7f1edQT22b515c761e2c8d8d3b6a07c5ab?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

OTTO uses custom firmware to feed G-code into an Arduino Due, which controls the step and direction of stepper motors that drive the machine. All of these components work in tandem to form a robust, accurate, and reliable automated liquid handling system for generating reproducible data at an affordable price point.

The necessary components of our design, including materials and set-up instructions, are all separated and detailed in the <a href="mechanical.md">Mechanical</a>, <a href="electrical.md">Electrical</a>, and <a href="software.md">Software</a> descriptions. All files are linked in each section, and can also be found in the GitHub repository: https://drd-flo.github.io/OTTO/.
