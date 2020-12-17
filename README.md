# Public JFX-ensemble
[![Build Status](https://travis-ci.com/jfx-ensemble/public-ensemble.svg?branch=master)](https://travis-ci.com/jfx-ensemble/public-ensemble)

This repository contains many JavaFX-samples which can be found at https://www.jfx-ensemble.com/

You can add your own project to the ensemble by creating a pull request.
Travis will automatically check, whether its working properly and is free of memory leaks.
To do so, do the following:
* Add your project to the file settings.xml
* Add the file `<project>/build.grdle` to the project and configure it accordingly
* Run the unit-tests with `./gradlew test`
* Test the website with: `./gradlew jproRun -PONLY_PROJECT=<project>`
* Create a pull request

Afterward we will review your changes and integrate them to the website https://www.jfx-ensemble.com

These Projects are currently added and can be used as an reference:
* [PickerFX](https://github.com/dlsc-software-consulting-gmbh/PickerFX)
* [PDFViewFX](https://github.com/dlsc-software-consulting-gmbh/PDFViewFX)
* [GemsFX](https://github.com/dlsc-software-consulting-gmbh/GemsFX)

### How does it work?
The website will check the file `ensemble-samples.json` in the root package.
Each sample listed in the file will get added to the ensemble-page.
Take a look at this example: `https://github.com/dlsc-software-consulting-gmbh/GemsFX/blob/master/gemsfx-demo/src/main/resources/ensemble-samples.json`

Each sample has the following required properties:
* name: The name of the sample.
* preview: An image that will be used as a preview.
* category: Usually the name of the project. Usually, all samples in a project have the same category.
* desc: The description of the sample. It's shown below the name.

The following properties are optional:
* classname: The name of the class which shall be shown. This has to be of the type Application.
* fxml: The fxml-file.
* controller: The controller of the fxml file
* css: a list of css resources, which are added to the node defined by the fxml-file.

The sample has to either define the class name or the fxml-file (with an optional controller and optional css-files)