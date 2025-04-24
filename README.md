# STL Big Data Meetup
An example SQL coding challenge for the STL Big Data Meetup in May 2025

# Setup
```
-- Create the Attractions table
CREATE TABLE Attractions (
    AttractionID INT PRIMARY KEY,
    Name VARCHAR(255) NOT NULL,
    Category VARCHAR(100),
    Address VARCHAR(255),
    City VARCHAR(100),
    ZipCode VARCHAR(10)
);

-- Create the Reviews table
CREATE TABLE Reviews (
    ReviewID INT PRIMARY KEY,
    AttractionID INT,
    UserID INT,
    ReviewDate DATE,
    Rating INT,
    Comment TEXT,
    FOREIGN KEY (AttractionID) REFERENCES Attractions(AttractionID)
);

-- Insert data into the Attractions table
INSERT INTO Attractions (AttractionID, Name, Category, Address, City, ZipCode) VALUES
(1, 'Gateway Arch National Park', 'Landmark', '11 N 4th St', 'St. Louis', '63102'),
(2, 'City Museum', 'Museum', '750 N 16th St', 'St. Louis', '63103'),
(3, 'Saint Louis Zoo', 'Park', '1 Government Dr', 'St. Louis', '63110'),
(4, 'Missouri Botanical Garden', 'Garden', '4344 Shaw Blvd', 'St. Louis', '63110'),
(5, 'Forest Park', 'Park', '5595 Grand Dr', 'St. Louis', '63112'),
(6, 'Cahokia Mounds State Hist.', 'Historical Site', '30 Ramey St', 'Collinsville', '62234'),
(7, 'Ted Drewes Frozen Custard', 'Food', '6726 Chippewa St', 'St. Louis', '63109');

-- Insert data into the Reviews table
INSERT INTO Reviews (ReviewID, AttractionID, UserID, ReviewDate, Rating, Comment) VALUES
(1, 1, 101, '2025-04-15', 5, 'Amazing views!'),
(2, 2, 102, '2025-04-16', 5, 'So much to explore.'),
(3, 1, 103, '2025-04-17', 5, 'A must-see in St. Louis.'),
(4, 3, 101, '2025-04-18', 4, 'Great for families.'),
(5, 4, 104, '2025-04-19', 5, 'Beautiful gardens.'),
(6, 2, 103, '2025-04-20', 3, 'A bit crowded on the weekend.'),
(7, 5, 102, '2025-04-21', 5, 'Perfect for a walk or picnic.'),
(8, 1, 105, '2025-04-22', 3, 'The museum at the base is interesting.'),
(9, 7, 101, '2025-04-22', 5, 'Best frozen custard ever!'),
(10, 3, 104, '2025-04-23', 4, 'Lots of different animals to see.');
```

# Challenges

Question 1: Retrieve the names of all attractions located in the city of 'St. Louis'.
Question 2: List the names of attractions along with the number of reviews they have received. Order the results from the attraction with the most reviews to the least.
Question 3: Find the average rating for each attraction. Display the attraction name and its average rating, rounded to two decimal places.
Question 4: Identify the names of attractions that have at least one review with a rating of 5 and at least one review with a rating of 3.
Question 5: For each attraction category, find the attraction with the highest average rating. Display the category, attraction name, and its average rating. (Hint: You might need to use window functions or a subquery).
