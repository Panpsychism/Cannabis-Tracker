Open Source i-502 Tracking Software
===========

Requirements:
-----------
1. Users should be able to input inventory information with a flow that follows product from seeds to sale.
   a) need entity relationship diagram
   b) tables: 
employee (id, firstname, lastname, datejoined, departuredate), 
location(id, description), productid (id, added, strainid, description),
licenses (id, tradename, location, licensetype, licensestatus, ubi),
seed(id, added, strainid, indica, sativa, cbd, description), 
product (id, strainid, thc%, cbd%, name, description)
sexing(id, added, strainxid, strainyid, newstrainid), 
germination (id, added, modified, locationid, productid, modified, quarantineid, locationid), 
seedlings (id, added, locationid, modified, germinationid, seedid, quarantineid), 
vegitative (id, added, modified, locationid, productid, seedlingid, germinationid, quarantineid), 
bloom (id, added, modified, locationid, vegitativeid, seedlingid, germinationid, productid, quarantineid), 
process(id, phase, productid, bloomid, producttype, 
quarantine(id, added, locationid, removed, productid, germinationid, seedlingid, vegitativeid, bloomid, saleid),
lots(id, added, modified, strainid, productid), 
sales(id, added, modified, sellerid, buyerid, returnid),
taxes(id, added, licenseid, paymentid),
refunds(id, added, sellerid, buyerid, taxid)

### any suggestions/requirements I'm not considering? ###

2. Data should be stored in a relational database (MySQL?)
3. User should be able to extract data from this database and upload it to the Liquor Control Board's tracking node.
