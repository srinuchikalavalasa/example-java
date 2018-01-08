

# [Codecov][0] Java Example
## Guide
### Travis Setup

Add the following to your `travis.yml`:
```yml
language:
  LANG_FOR_REPO
after_success:
  - bash <(curl -s https://codecov.io/bash)
```
### Produce Coverage Reports
1. Add JaCoCo Plugin to your pom.xml file, [see here](https://github.com/codecov/example-java/blob/master/pom.xml#L38-L56)
## Caveats
#### Private Repo
You will need to add the following your `travis.yml`:
```yml
env:
  global:
    - CODECOV_TOKEN=:uuid-repo-token
```
We can add more caveats for the language/framework(s) here

## Support

### FAQ
- Q:  How do I enable multi-module projects?<br/>A: In your `pom.xml` file please append a list of modules in your projects:
```xml
<project>
  <modules>
    <module>module_a/</module>
    <module>module_b/</module>
  </modules>
</project>
```
- Q:  Seeing `Skipping JaCoCo execution due to missing execution data file`?<br/>A: Please see [http://stackoverflow.com/questions/18107375/...](http://stackoverflow.com/questions/18107375/getting-skipping-jacoco-execution-due-to-missing-execution-data-file-upon-exec).
- We should talk about using other CIs here.
- Q: Does Codecov accept `jacoco.exec` reports?<br/>A: **No**, these files are not supported. Please produce a `xml` file as detailed in the pom.xml file at [codecov/example-java][1].
- Q: Is there a Gradle example?<br/>A: **Yes**, enter [codecov/example-gradle][2]
- Q: Is there a Andorid example?<br/>A: **Yes**, enter [codecov/example-android][3]

### Contact
- Intercom (in-app messanger)
- Email: support@codecov.io
- Slack: slack.codecov.io
- [gh/codecov/support](https://github.com/codecov/support)

View source and learn more about [Codecov Global Uploader](https://github.com/codecov/codecov-bash)


[0]: https://codecov.io/
[1]: https://github.com/codecov/example-java
[2]: https://github.com/codecov/example-gradle
[3]: https://github.com/codecov/example-android
[4]: https://github.com/codecov/example-java-maven
[5]: https://docs.codecov.io/docs/about-the-codecov-bash-uploader#section-upload-token
