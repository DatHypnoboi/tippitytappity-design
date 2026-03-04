# tippitytappity-design

tippitytappity is a program to practice typing


## Data model

```mermaid
classDiagram
  User --> Tester : used in
  Attempt --> Tester : used in
  Attempt --> User : used in
  class User{
        - id: UUID
        - name: string
        - email: string
        - password: string
        - attempts: vector~Attempt~
        + login(user: string, pass: string) boolean
        + getEmail() string
        + logScore(scores: Attempt)
        + getHistory() : vector~Attempt~
  }

  class Attempt{
        - wpm: double
        - accuracy: double
        + getAccuracy() : double
        + getWPM() : double
  }

  class Tester{
        - generatePhraseList(length: int) vector~string~
        + runTest(user: User) : Attempt
        + logScore(user: User, attempt: Attempt)
  }

```
