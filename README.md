# tippitytappity-design

tippitytappity is a program to practice typing


## Data model

```mermaid
classDiagram
  phrases <|-- typingSpeed
  phrases <|-- typingAccuracy
  class phrases{
        - id: int
        - email: string
        - password: string
        + login(user: string, pass: string) boolean
        + get_email() string
  }
  class typingSpeed{
        - badges vector~string~
        + add_badge(title: string)
        + get_badges() vector~string~
  }
  class typingAccuracy{
        - correct vector~string~
        - numOfLines int
        + accuracyCalc( correct )
  }
```
