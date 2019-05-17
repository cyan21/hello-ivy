# Demo Ivy integration with Artifactory


This project is a "fork" of the "hello-ivy" example in the apache-ivy distribution

> Requirements :
> Ant and Ivy have to be installed + JFrog CLI configured with Artifactory


## How to 

* build, generate jar and publish to artifactory

```
$ ant publish 
```
it will publish the following artifact : org/ych/hello-ivy-0.1.jar along with a build info  into Artifactory 



* clean project

```
$ ant clean 

```

> check out the build.xml for other targets



## Info

### Resolution 

here are all the steps to fetch dependencies from Artifactory (already implmented) : 

* generated ivysettings.xml from artifactory 
* specified the ivysettings.xml in the build.xml with <ivy:settings> tag

> Make sure your ~/.ivy2/cache doesn't contain already your dependencies !


### Deployment 

here are all the steps to push the generated jar to Artifactory (already implmented) : 

* added the target "publish" to the build.xml

notes :

> the resolver name is a referenced to the one in the ivysettings.xml
> [artifact] and [revision] refer to the module name and revision in ivy.xml 


