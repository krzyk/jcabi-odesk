<img src="http://img.jcabi.com/logo-square.png" width="64px" height="64px" />

[![Made By Teamed.io](http://img.teamed.io/btn.svg)](http://www.teamed.io)
[![DevOps By Rultor.com](http://www.rultor.com/b/jcabi/jcabi-odesk)](http://www.rultor.com/p/jcabi/jcabi-odesk)

[![Build Status](https://travis-ci.org/jcabi/jcabi-odesk.svg?branch=master)](https://travis-ci.org/jcabi/jcabi-odesk)
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.jcabi/jcabi-odesk/badge.svg)](https://maven-badges.herokuapp.com/maven-central/com.jcabi/jcabi-odesk)

More details are here: [odesk.jcabi.com](http://odesk.jcabi.com/)

Set of classes in `com.jcabi.odesk` package is
an object oriented API of [Odesk](http://www.odesk.com):

```java
import com.jcabi.odesk.RtOdesk;
import com.jcabi.odesk.Odesk;
public class Main {
  public static void main(String[] args) {
    Odesk odesk = new RtOdesk(
      key, // odesk application key
      secret, // odesk application secret code
      token, // OAuth access token
      tsecret // OAuth access token, secret part
    );
    Team team = odesk.teams().team(/* team reference ID */);
    String ref = team.adjustments().add(
      "13369463", // contract number,
      new Cash.S("10.00"), // amount to be paid to the supplier
      new Cash.S("0.0"),
      "bonus payment for you dude", // comments
      "thanks for your good work, keep it up!" // notes
    );
  }
}
```

## Questions?

If you have any questions about the framework, or something doesn't work as expected,
please [submit an issue here](https://github.com/jcabi/jcabi-odesk/issues/new).

## How to contribute?

Fork the repository, make changes, submit a pull request.
We promise to review your changes same day and apply to
the `master` branch, if they look correct.

Please run Maven build before submitting a pull request:

```
$ mvn clean install -Pqulice
```
