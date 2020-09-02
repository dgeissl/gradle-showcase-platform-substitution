Showcasing a problem with dependency substitution in gradle, when applied to BOM dependencies:

# Usage

Substitute the BOM dependency via `eachDependency { useTarget ... }` (broken)
 
    gradlew resolveDependencies -Dsubstitution=useTarget
    
Substitute the BOM dependency via `dependencySubstitution { substitute module ... }` (broken)
    
    gradlew resolveDependencies -Dsubstitution=substituteModule

Substitute the BOM dependency via `eachDependency { useVersion ... }` (working)
    
    gradlew resolveDependencies -Dsubstitution=useVersion 