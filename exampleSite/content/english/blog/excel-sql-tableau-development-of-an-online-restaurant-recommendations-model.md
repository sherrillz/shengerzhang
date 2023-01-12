+++
author = "Shenger Zhang"
date = 2022-12-08T05:00:00Z
description = "Built an interactive map using Tableau to show the top 5 restaurants by filtering restaurant categories "
image = "/images/terpfood.png"
image_webp = "/images/terpfood-copy.webp"
title = "Excel, SQL, Tableau: Development of an Online Restaurant Recommendations Model"

+++
The Terp Foodie project aims to helping foodie in College Park to find the highest rated restaurants from different categories, and recommend a top dish for each top restaurant in its field.

**What sources it includes?**  
We use data from 5 most famous review platform: Google Review, Yelp, TripAdvisor, Grubhub and Zomato.

![](/images/blog/food1.png)

* **Project Processes**

We built a database for the restaurants in College Park to track each restaurant to analyze what kind of restaurants attract more customers’ reviews and higher ratings

* **Mission Statement**

1\.To connect people with great local restaurants along the way, Terp foodie hopes to enrich the lives of consumers and small business owners. In pursuit of this mission, we aspire to provide the most helpful information possible about local restaurants.

2\.To analyze the customers’ reviews to help local restaurants elevate service quality, Terp foodie hopes to build insight on the food preference from the customers’ reviews and ratings.

* **Mission Objectives**

1\.To find the top 5 categories of local restaurants that get the highest rating.

2\.To find the top 5 categories of local restaurants that get the most customer reviews.

3\.To find the taste differences from each platform

4\.To find the restaurant that gets the highest ratings

5\.To find the restaurant that gets the most customer reviews

6\.To find the recommendation for each popular category.

### **Database Design**

**Logical Database Design——ER Diagram**

![](/images/blog/food2.png)

**Logical Database Design——relational schema**

![](/images/blog/food3.png)

**Physical Database Design**

![](/images/blog/food4.png)

### **Application**

**1.What are the top 5 categories of local restaurants from all the platform that get the highest rating?**

![](/images/blog/food5.png)

![](/images/blog/food5_r.png)

**2.What are the top 5 categories of local restaurants from all the platform that get the most reviews?**

![](/images/blog/food6.png)

![](/images/blog/food6r.png)

**3.What are the top categories of local restaurants that get the highest ratings from each platform?**

![](/images/blog/food7.jpg)

![](/images/blog/food7r.png)

**4.What are the top 5 restaurants’ names and addresses and categories that get the highest ratings?**

![](/images/blog/food9.png)

![](/images/blog/food9r.png)

![](/images/blog/foodtableau.png)

### **Project Proposal Document**

**1. restaurant processes**

We built a database for the restaurants in College Park to track each restaurant to analyze what kind of restaurants attract more customers’ reviews and higher ratings.

Each restaurant has a unique identifier and is required to restore restaurant name, address and restaurant categories.

Each Dish has a unique identifier and is required to restore the dish name, dish price, dish category, and dish review number.

Each platform has a unique platUrl and is required to restore the plat name, platFounder, platProduct, and platBusinessType.

Each user has a unique identifier and is required to restore the user name and user review count, number of useful and user start date .

**2. Identify at least four entity types.**

Restaurant, Dish, Platform, User

**3. Perform database analysis on entity and relationship types, i.e.**

**ER schema.**

Restaurant (**restaurantId,** restaurantName, restaurantCag, restaurantIsOpen, restaurantAddress, -restaurantStreet, -restaurantCity, -restaurantState, -restaurantZipCode, restaurantGeoCoord, -restaurantGeoLatitude, - restaurantGeoLongitude)

Dish (**dishId**, dishName, dishPrice, dishCategory, =dishReviewNum)

Platform (**platName**, platUrl, platFounder, platProduct, platBusinessType)

User (**userId**, userName, =userReviewCount, userStDate, userUseful)

**Relationship:**

**(**_1. Identify relationship types including at least one many-to-many binary or_

_higher-degree relationship type - no singleton entity type._**)**

Produce: binary relationship

1 dish to 1 restaurant

1 restaurant to 0 or more dishes

Record: binary relationship

1 platform to 1 or more restaurants

1 restaurant to 1 or more platform

Review (reviewDate): binary relationship

1 user to 0 or more restaurants

1 restaurant to 1 or more users

Sign: binary relationship

1 user to 0 or more platforms

1 plat to 1 or more users

**Convert ER model into the relational schema and identify primary and foreign keys.**

Restaurant (**restaurantId**_, _restaurantName, restaurantCag, isOpen, restaurantStreet, restaurantCity, restaurantState, restaurantZipcode, geoLatitude ,geoLongitude)

dishes (**dishId**, _restaurantId_**,** dishName, dishPrice, dishCategory, dishReviewNum)

User (**userId,** userName, userStDate, userUseful)

Review(**_userId_**, **_restaurantId_**, reviewDate,reviewStar, reviewText, isReviewUseful)

Platform (**platName**,platURL,platFounder,platProduct,platBusinessType)

Record (**_restaurantId_**, **_platName_**, restaurantStar, restaurantReviewCount)

Sign (**_platName,userId_)**

 **Generate business rules and determine referential integrity actions.**

**_Business rules:_**

 1. \[R1\] When the restaurant is closed or the information of the restaurant changes, the information of the restaurant’s dish should be deleted or changed.
 2. \[R2\] When a restaurant is closed, the restaurant’s review should be deleted.
 3. \[R3\] When the restaurant’s information is changed, the information on the review should be changed.
 4. \[R4\] When a user logs out, the user’s review should still remain.
 5. \[R5\] When a user’s information is changed, the user’s information on the review should also change.
 6. \[R6\] When a restaurant is closed or the information of the restaurant changes, the information of the restaurant should be deleted or changed from the platform’s record.
 7. \[R7\] When a platform is closed or the information of the platform changes, the platform’s information in the records should be deleted or changed.
 8. \[R8\] When a user logs out, the user’s information should still remain in the platform
 9. \[R9\] When users change their information, the user’s information should change in the platform
10. \[R10\] When a platform is closed or the information of the platform changes, the user cannot sign in to that platform.
11. \[R11\] When a platform changes its information like URL, the user can sign in to that new URL.

**_Referential integrity:_**

 **Describe sample data for every relation.**

The restaurant’s entity will contain 20 restaurants for each from Yelp, Google map and Tripadvisor and 5 from Zomato and Grubhub. The category will contain at least 5 types to make the comparison more meaningful. The sample data will be like this.

The User entity will contain more than 40 users from all the platforms. The sample data will be like this.

The Dish entity will contain 3 dishes from each restaurant. The sample data will be like this.

The Reviews relation will contain 3 latest reviews if exists from each restaurant. The sample data will be like this.

The Platform entity will contain 5 platforms: Yelp, Google, TripAdvisor, Grubhub, Zomato. The sample data will be like this.

The Record relation will contain approximately 100 relations. The sample data will be like this.

The Sign relation will contain more than 20 relations. The sample data will be like this

Link to the slides: [https://docs.google.com/presentation/d/1_wrtAFHbON8hmTHzrc8hhKWnHe5P0RUA/edit?usp=sharing&ouid=102714240654033739195&rtpof=true&sd=true](https://docs.google.com/presentation/d/1_wrtAFHbON8hmTHzrc8hhKWnHe5P0RUA/edit?usp=sharing&ouid=102714240654033739195&rtpof=true&sd=true "Project slide")