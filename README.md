# Santander Bootcamp Java Project

Welcome to the Santander Bootcamp Java project, developed with dedication and learning through the Dio (Digital Innovation One) platform. This project represents a RESTful API designed to provide a range of financial services.

## Project Structure

The project follows a modular structure with various components, as illustrated in the class diagram below:

```mermaid
classDiagram
  class User {
    - String name
    - Account account
    - Feature[] features
    - Card card
    - News[] news
  }
  
  class Account {
    - String number
    - String agency
    - Number balance
    - Number limit
  }
  
  class Feature {
    - String icon
    - String description
  }
  
  class Card {
    - String number
    - Number limit
  }
  
  class News {
    - String icon
    - String description
  }
  
  User "1" *-- "1" Account : Has
  User "1" *-- "N" Feature : Has
  User "1" *-- "1" Card : Has
  User "1" *-- "N" News : Receives
