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
