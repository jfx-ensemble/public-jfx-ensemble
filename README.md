# Public Ensemble
[![Build Status](https://travis-ci.com/jfx-ensemble/public-ensemble.svg?branch=master)](https://travis-ci.com/jfx-ensemble/public-ensemble)

This repository contains many javafx-samples which can be found at https://www.jfx-ensemble.com/

You can add your own project to the ensemble by creating a pull request.
Travis will automatically check, whether its working properly and is free of memory leaks.
To do so, do the following:
 * Add your project to the file settings.xml
 * Add the file `<project>/build.gradle` to the project and configure it accordingly
 * Run the unit-tests with `./gradlew test`
 * Test the website with: `./gradlew jproRun -PONLY_PROJECT=<project>`
 * Create a pull request

Afterwards we will review your changes and integrate them to the website https://www.jfx-ensemble.com