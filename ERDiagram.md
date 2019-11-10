# ER Diagram

Based on the [Data Requirements](./DataRequirements.md), we can define the the ER Diagram to show the entities and the relationship between those entities for our desired database.

**Descriptions**:

1. Rectangle shapes represent for the entities.

2. Eclipse shapes represent for the entities' attributes.

4. Diamond shapes represent for the relationship'name between 2 entities

3. The arrow between 2 entities (cross the Diamond shape) represents for their relationship.

    * One to One:`   ` `One   <----<name of relationship>----->   One`
    
    * One to Many:`  ` `One   <-----<name of relationship>-----   Many`
   
    * Many to One:`  ` `Many   -----<name of relationship>----->   One`
    
    * Many to Many:`    ` ` Many  -----<name of relationship>------   Many`

For example: ``` Users ------<order>---- Items```: **Many to Many** relationship

-> Each users can order the same items, and each item can be ordered by many users (multiple users can order the same items)


![Image of ER Diagram](./ER%20Diagram/Business_store_ERDiagram.png)
