# System Requirement Specification
This is a repo for breaking down the desired system requirement.

## Data Design
Below are the defined model to implement on the application:

### User
Attributes:
- user_id: string
- password: string
- email: string
- full_name: string
- age: int
- location: string
- places_preferences:
  - category_id: list:Categories
  - price_range: int
  - solo_traveler: boolean

### Plan
Attributes:
- plan_id: string
- user_id (FK): string
- plan_title: string
- num_of_people: int
- city: string
- start_location: Place
- start_time: time

### Plan_Place
Attributes:
- plan_id (FK): string
- place_id (FK): string
- depart_time: time
- transport_mode: string -> user input
- transport_price: float -> user input

### Category
Attributes: 
- category_id: string
- name: string

### Place
Attributes:
- place_id: string
- category_id (FK): string
- name: string
- description: string
- city: string
- price: float
- lat: float
- lng: float
- rating: float -> avg from user rating
- image: string

### Place_Rating
Attributes:
- user_id (FK): string
- place_id (FK): string
- rating: int
