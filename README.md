# jbang-picocli-native
simple picocli, jbang, graalvm native-image example

# Setup

- Install JBang obviously
- Installed GraalVM native-image via SDKMAN!
  - as per https://www.jbang.dev/documentation/jbang/latest/native-images.html
- Followed this great guide on creating native images for picocli which finally led me to realize you need the reflection config not only for the mixinStandardHelpOptions, but also for your class and parameters as well - hence the entry for GreetApp where I specify the parameters fields
  - https://www.infoq.com/articles/java-native-cli-graalvm-picocli/
- then simply run `jbang export native helloWorldCLI.java` to create the "helloWorldCLI" binary

# Stats
GraalVM obviously offers a much faster startup time, suited to actually using these jbang scripts for scripting if you don't feel like writing bash:

<img width="767" height="426" alt="image" src="https://github.com/user-attachments/assets/695c5b0b-c91c-4068-aebd-28af11dffb57" />

But, there's a tradeoff on size:

<img width="592" height="83" alt="image" src="https://github.com/user-attachments/assets/bded7390-cedb-4dba-a4c3-61bab89c0295" />
