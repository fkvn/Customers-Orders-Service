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
