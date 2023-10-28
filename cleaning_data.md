What issues will you address by cleaning the data?

--As stated in the instructions, the all_sessions.productPrice column and the analytics.unit_price column both required dividing by 1000000.

--Replaced all instances of "not available in demo dataset" from all_sessions.city with "N/A"




Queries:
Below, provide the SQL queries you used to clean your data.

--Dividing the prices by 1000000--

    UPDATE all_sessions
    SET "productPrice" = "productPrice" / 1000000
    
    UPDATE analytics
    SET unit_price = unit_price / 1000000

--Updating city column--

    UPDATE city
    SET city = REPLACE (city, 'not available in demo dataset', 'N/A');

