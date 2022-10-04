### Common service
 repository for common services (such as common utility or common messages)

1. Project build settings
```
// build.gradle 

// 1. add maven-publish plugins

plugins {
    id 'maven-publish'
}

// 2. add mavenLocal repository 
repositories {
    mavenLocal()
}

// 3. add publishing task 
publishing {
    publications {
        maven(MavenPublication) {
            from components.java
        }
    }
}
```

2. Publish on local repository
```
./gradlew build publishToMavenLocal
```


3. Related Project  
3-1. project build settings
```
  // 1. add mavenLocal repository 
  repositories {
    mavenLocal()
  }

// 2. add dependencies
  implementation 'org.example:common:1.0-SNAPSHOT'
  ```
3-2. build dependencies
```
./gradlew build
```
