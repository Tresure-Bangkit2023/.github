# System Requirement Specification
This is a repo for breaking down the desired system requirement.

## Data Design
Below are the defined model to implement on the application:

### User
Attributes:
- user_id (PK): string
- username (Unique): string
- password: string
- email: string
- full_name: string
- location: string
- age: int
- liked_categories: list
- price_range_id (FK): int
- solo_traveler: boolean

### PriceRange
- price_range_id (PK): int
- name: string

### Plan
Attributes:
- plan_id (PK): string
- user_id (FK): string
- title: string
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
- category_id (PK): string
- name: string

### Place
Attributes:
- place_id (PK): string
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
