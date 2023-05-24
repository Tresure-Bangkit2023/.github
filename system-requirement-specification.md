# System Requirement Specification
This is a repo for breaking down the desired system requirement.

## Data Design
Below are the defined model to implement on the application:

### User
Attributes:
- user_id: string
- username: string
- password: string
- email: string
- full_name: string
- age: int
- location: string
- places_preferences:
  - category_id: list:Categories
  - price_range: int
  - solo_traveler: boolean

### Category
- category_id: string
- name: string

### Place
- place_id: string
- category_id (FK): string
- name: string
- description: string
- price: int
- lat: float
- lng: float
- rating: float -> avg from user rating
- image: string

### Place_Rating
- user_id (FK): string
- place_id (FK): string
- rating: int
