# jbang-picocli-native
simple picocli, jbang, graalvm native-image example

# Setup

- Install JBang obviously
- Installed GraalVM native-image via SDKMAN!
  - as per https://www.jbang.dev/documentation/jbang/latest/native-images.html
- Followed this great guide on creating native images for picocli which finally led me to realize you need the reflection config not only for the mixinStandardHelpOptions, but also for your class and parameters as well - hence the entry for GreetApp where I specify the parameters fields
  - https://www.infoq.com/articles/java-native-cli-graalvm-picocli/
- then simply run `jbang export native helloWorldCLI.java`

# Stats
GraalVM obviously offers a much faster startup time, suited to actually using these jbang scripts for scripting if you don't feel like writing bash:

<img width="743" height="142" alt="image" src="https://github.com/user-attachments/assets/26b9a86a-d424-48d4-992c-4294bf79e2ea" />

But, there's a tradeoff on size:

<img width="705" height="62" alt="image" src="https://github.com/user-attachments/assets/d2bca7ef-a803-48b3-b2e8-07b88e43e16b" />
