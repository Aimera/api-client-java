Aimera platform API class and examples for Java
===

Due to 256 bit keys usage it may be needed to install Java Cryptography Extension (JCE) Unlimited Strength Jurisdiction Policy Files. For Java version 7 (https://www.oracle.com/technetwork/java/javase/downloads/jce8-download-2133166.html) or version 8 (https://www.oracle.com/technetwork/java/javase/downloads/jce8-download-2133166.html)

## Event tracking example

This code prepares a call to Challenger server on event happened to a client identified by {client_id}:

```java
import ChallengerPlatform.*;

// ... your code ...

Challenger myChallenger = new Challenger('api.aimera.io');

myChallenger.setOwnerId('{owner_id}'); // Optional
myChallenger.setClientId('{client_id}');
myChallenger.setKey('{secret_key}');
myChallenger.addParam('multiple', '{multiple}'); // Optional

bool resp = myChallenger.trackEvent('{event}');
```
