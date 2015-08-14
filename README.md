
#Test Android My First App


<link href="https://github.com/JFCatKeyneosoft/TestAndroidMyFirstApp/blob/master/Resources/JavaScript/lightbox/css/lightbox.css" rel="stylesheet">
</link>


<script src="https://github.com/JFCatKeyneosoft/TestAndroidMyFirstApp/blob/master/Resources/JavaScript/lightbox/js/lightbox-plus-jquery.js">
</script>


######Learn to develop

Just create new app for Android device
* create new app in Android Studio (https://developer.android.com/sdk/index.html)
* create GitHub repository (https://gitgub.com)
* move project in git repository
* commit your project on GitHub 

<a href="https://github.com/JFCatKeyneosoft/TestAndroidMyFirstApp/blob/master/Resources/Images/image1.png" data-lightbox="roadtrip">Image #1</a>

<a href="https://github.com/JFCatKeyneosoft/TestAndroidMyFirstApp/blob/master/Resources/Images/image2.png" data-lightbox="roadtrip">Image #2</a>

<a href="https://github.com/JFCatKeyneosoft/TestAndroidMyFirstApp/blob/master/Resources/Images/image3.png" data-lightbox="roadtrip">Image #3</a>

######Learn continuous integration

Add continuous integration of our repository
* go on Travis CI (https://travis-ci.org)
	* login with your GitHub account
	* add project in continuous integration
* in your project create ".travis.yml" file at root
* in ".travis.yml" write the configuration to continuous integration

		sudo: false
		language: android
		jdk: oraclejdk7
		
		android:
   		 components:
  		  - platform-tools
  		  - android-22
  		  - build-tools-22.0.1
		- extra
		
		before_install:
		- chmod +x ./travis/before_script.sh
		- chmod +x ./travis/install.sh
		- chmod +x ./travis/script.sh
		
		before_script: ./travis/before_script.sh
		install: ./travis/install.sh
		script: ./travis/script.sh

* create the folder "travis"`
* create the file "travis/before_script.sh" empty for the time
* create the file "travis/install.sh" to prepare dependaencies
		
		git submodule update --init --recursive
		
* create the file "travis/script.sh" write the script to build, to tests, etc.

		./gradlew clean build
	
* commit your project on GitHub 

######Learn coverage

######Learn branch
On GitHub your project have one branch : "master". Create 3 branchs : "development", "release", "distribution"

* "development" the brach to commit the development, not stable, not building
* "master" the branch to merge development, stable, building, Continous integration and coverage!
* "release" the branch of release of project, stable, build
* "distribution" the branch of distribution, stable, build, distribute in store

When the development is in progress, it's push on "development". When the development is finish it's push on "master". When the project it's usable and need user's test push it on "release". When the project is ok to be distribute on App's store push on distribute.

You can create more than one "development" branch, for example one branch per developer like this "developement-jfcatkeyneosoft" or one branch per module like this "developement-homescreen" … 

##Authors
![Licence Status](https://img.shields.io/badge/Author-Jean--François%20CONTART-purple.svg)

##Original Path 
[![Path](https://img.shields.io/badge/GitHub-TestAndroidMyFirstApp-ff4488.svg)](https://GitHub.com/JFCatKeyneosoft/TestAndroidMyFirstApp/)

##States of Projet

[![Build Status](https://travis-ci.org/JFCatKeyneosoft/TestAndroidMyFirstApp.svg?branch=master)](https://travis-ci.org/JFCatKeyneosoft/TestAndroidMyFirstApp)
[![Build Status](http://img.shields.io/coveralls/JFCatKeyneosoft/TestAndroidMyFirstApp.svg?)](https://coveralls.io/GitHub/JFCatKeyneosoft/TestAndroidMyFirstApp)

## Platform and Languages
![Platform Status](https://img.shields.io/badge/platform-Android-lightgray.svg)
![Language Status](https://img.shields.io/badge/IDE-Android%20Studio-blue.svg)
![Language Status](https://img.shields.io/badge/language-Java-blue.svg)

##Licence
![Licence Status](https://img.shields.io/badge/licence-Copyleft-yellowgreen.svg)

##Services
Special thanks for these services!

This repository use :
 - GitHub for source control : https://github.com
 - Travis CI for continous integration : https://travis-ci.org
 - Coveralls for code coverage : https://coveralls.io
 

