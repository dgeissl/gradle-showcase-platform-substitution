Showcasing a problem with dependency substitution in gradle, when applied to BOM dependencies:
Reported in https://github.com/gradle/gradle/issues/14396

# Usage

Substitute the BOM dependency via `eachDependency { useTarget ... }` (broken)
 
    gradlew resolveDependencies -Dsubstitution=useTarget
    
Substitute the BOM dependency via `dependencySubstitution { substitute module ... }` (half working and half broken)
    
    gradlew resolveDependencies -Dsubstitution=substituteModule

Substitute the BOM dependency via `eachDependency { useVersion ... }` (working)
    
    gradlew resolveDependencies -Dsubstitution=useVersion 
