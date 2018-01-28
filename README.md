# travis-test

added:

* swift package init --type library
* swift package generate-xcodeproj
* pod init
* pod install

### build success

try now adding env variable

framework_name = DavidsFramework

added

script:
  - - mkdir $framework_name
 
### build failed 
The command "mkdir $framework_name" exited with 0.

trying

script:
  - echo $framework_name
  - mkdir $framework_name
  
# BUILD SUCCESS

language: objective-c
env:
  - FOLDER_NAME=David
  - FRAMEWORK_NAME=Framework
os: osx
osx_image: xcode9.2
before_install:
  - swift package init --type library
  - swift package generate-xcodeproj
script: 
  - mkdir $FOLDER_NAME
  - touch $FOLDER_NAME/$FRAMEWORK_NAME
  - ls -ll

# Build failed

It made 2 builds rather than 1

trying

env:
  - FOLDER_NAME=David FRAMEWORK_NAME=Framework
  

# Build success

trying to force a fail with git push

# Build failed because I added develop rather than master
