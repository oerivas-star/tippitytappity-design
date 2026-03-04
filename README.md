# tippitytappity-design

tippitytappity is a program to practice typing


## Data model

```mermaid
classDiagram
  phrases <|-- typingSpeed
  phrases <|-- typingAccuracy
  users <|-- phrases
  class phrases{
        - id: int
        - listOfWords: vector~string~
        + get_Word() string
  }
  class typingSpeed{
        - startTime: int
        - endTime: int
        + compare(pass: startTime, pass: endTime)
  }
  class typingAccuracy{
        - correct vector~string~
        - numOfLines: int
        + accuracyCalc( pass: correct )
  }
  class users{
        - userID: int
        - userName: string
        + getUserID()
  }
  class histroy{
        - tests: vector~typing Test~
        + addTest(pass: typingTest)
        + getTests : vector~typing Test~
  }
```
