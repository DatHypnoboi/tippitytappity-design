# tippitytappity-design

tippitytappity is a program to practice typing


## Data model

```mermaid
classDiagram
  class User{
        - name: string
        - email: string
        - password: string
        - highscore: double
        - average: double
        - attempts: int
        + login(user: string, pass: string) boolean
        + get_email() string
        + log_score(score: int)
  }

  class Phrasebank{
        - phrases: vector~string~
        + generate_test(length: int) vector~string~
}

```
