---
layout: post
title: "GRAVITY VIEW"
name: gravity-view
date: 2017-05-12 12:00:00
categories: project
description: Introducing Gravity View - Because swiping is so yesterday!
img: gravity-view_logo.png
github_url: "https://github.com/gofynd/gravity-view"

---
<p>
Consumers don’t expect shopping to extend beyond the visual cues in a layered two dimensional space. What do we change first in the 2D world to transition the shopping experience to the 3D world with motion physics? With Gravity View you can now tilt your phone to browse through product images without having to swipe.
</p>

<p>
Mobile shopping just got so much fun! :)
</p>

<p>
Our vision at fynd was to empower users to navigate quickly through all product images without having to swipe through all of them. It was necessary to ensure seamless transition between images to avoid nausea and irritation.
</p>
<p>
Android Team took inspiration from Facebook's <a href="https://instantarticles.fb.com/">Instant Articles</a>. The concept behind the library is to utilize the motion sensors of an Android device and allow the end user to explore the product by rotating his device. It uses gyroscope motion sensor readings to scroll the image. Initially, team explored few libraries to achieve a smooth tilt experience and played around with the g vector values and tilt measurements but none of them gave us the results as needed. Since an accelerometer alone wasn't sufficient to avoid issues like gimbal lock and Sensor Fusion technique was the approach to provide accurate information by using rotation vector sensor, accelerometer, geomagnetic sensor, and gyroscope. After doing math calculation to solve this problem considering the number of images, range of tilting angle, pan speed for the canvas, and a few other variables to form an equation. Finally, figured the way to give a smooth scroll to the image on device tilt :)
</p>


<p>
You can view the code on <a href="https://github.com/gofynd/gravity-view">Github</a>. We’d love to hear your feedback.
</p>
