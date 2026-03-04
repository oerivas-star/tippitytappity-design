# tippitytappity-design

tippitytappity is a program to practice typing


## Data model

```mermaid
classDiagram
  typingTest <|-- phrases
  typingTest <|-- typingSpeed
  typingTest <|-- typingAccuracy
  typingTest <|-- users
  history <|-- users
  class phrases{
        - id: int
        - listOfWords: vector~string~
        - wpm: double 
        + get_Word() string
        + getWPM(): double
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
  class history{
        - tests: vector~typing Test~
        + addTest(pass: typingTest)
        + getTests: vector~typing Test~
  }
  class typingTest{
    - testID: int
    - attemptedAt: int
    - phraselD: int
    +  getTestID() : int + getAttemptedAt() : int
  }
```
