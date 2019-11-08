# Data Requirements

##### The system must manage the following data and constrains: 

1. The business will store and manage **Items** where everything is associated with it.  

1. A **User** can add one or more item into a cart before checking out. Each cart belongs to each user.

1. Each user will have the following information: Full name, username, password, address, phone, email, payment types. Each user can have multiple addresses and multiple phone numbers.

1. Each user can have many types of payments. Each payment should include its basic information. For instance, type (cash, debit, or credit), card numbers (no need if the payment type is cash).

1. There are 4 types of users:

    1. **Admins**: who have all privillege on the system, including manage staff’, items’ and customers’ information
    1. **Staff**: who can see and edit customers' information. Staff can see items' information, but don't have privillege to edit or delete any item. On top of that, each staff can't delete or block customer account. However, they can unlock customers' accounts.
    1. **Unregistered customers**: who will be able to view the list of items with its information.
    1. **Registered Customers**: who can not only view the list of items and its information, but also can performs all basic operations. For instance, they can add items to their cart, check out, also can see and edit their own information.

1. Each user can have one or more orders.

1. Each **ORDER** will be created after users checked out their items in their cart (after payment processed). Each order will have the following information: order number(ID), timestamp, payment type (cash, debit, or credit), list of items with all their basic information (name, color, size, price, etc.) and **the quantity** of each item. The **shipping information** also should be included in order's information. For example, shipping address, receiver name, type (self-pickup, ground, or express), tracking number (given by delivery company, **no tracking number for self-pickup**). Lastly, each order should display total price after considering subtotal, shipping fee, tax, discount, and etc.

1. Each user can only have one cart.

1. Each cart can have one or more items. Each cart contains items' information (name, color, type, size, price, etc.), the quantity of each item. The system should allow users to update items' quantity as well as remove the item from the cart. Each cart also displays the subtotal of the current status (sum of all items' price without external fees, such as tax or discount). However, each cart could support **Estimate the total cost** feature by allowing users to add discount or promo code and apply it to the subtotal and calculate the total price. For shipping fee, the system will ask users the zipcode only to calculate the estimate of shipping fee.

1. Each item will contain all required information for a basic item and be able to extend needed information in the future. Basic information involves manufacturer, category, size, color, timestamp (the date the item is created/imported to the system), unit, price per unit, quantity (total units), description, images.

    * Each item will belong to one manufacturer, while each manufacturer can have one or more items.

    * Each item can belong to one or more categories and each category can relate to one or more items.

    * Each item can have one or more sizes and colors. Multiple items can have the same size and color.
    
    * Each item can have one or more related images. However, each item should have up to only 15 images.

1. Each manufacturer will have name, phone number, and address information.

1. Each category should include name and description.

1. For size, the system should save its name and unit. For example, 8.5 US, or 8 UK.

1. Each color contains its name only unless we need more information later.

1. For each image stored in each item, we will the image name and link to download the image.

1. We should store information for **SALE ITEM** also. The needed information could be: event name, all basic item's information (name, type, size, color, etc.), timeline (start and end date of sale event), sale amount (percentage of original price per unit), and, finally, quantity condition. Quantity condition means the condition to apply the sale amount. For example, if we have an sale event called "buy one get one free" which will be from 12/1/2019 to 12/6/2019, all sale items of "buy one get one free" will be sale off 50% if they buy two items at a time. Therefore, the system should be able to query all the following information:
    1. Event: "Buy one get one free"
    1. Start Date: 12/1/2019
    1. End Date: 12/6/2019
    1. Items' list:
        * Item 1: name, manufacturer, category, size, color, etc.
        * Item 2: name, manufacturer, category, size, color, etc.
        * .....
    1. **sale amount: 50** (%)
    1. **quantity condition: 2**.


