<h1>This is an Entity Relationship Diagram of Instagram</h1>
<h2> Database strucure</h2>
<h3>account</h3>
<b>id (PK) (int)<br />
name: varchar(120)<br />
email: varchar(120)</b><br />
follower_id (FK)<br />
creation_dtae: datetime<br />
address: varchar (255)<br />
<h3>follower</h3>
<b>id (PK) (int)<br />
name: varchar(120)<br />
email: varchar(120)<br />
creation_date: datetime</b><br />
address: varchar (255)<br />
<h3>photo_account</h3>
<b>account_id (PK,FK) (int)<br />
photo_id (PK,FK)</b><br />
<h3>photo</h3>
<b>id (PK) (int)<br />
privacy: varchar(50)</b><br />
location_id (FK1) <br />
comment_id (FK2) <br />
like_id (FK3) <br />
album_id (FK4) <br />
<h3>album</h3>
<b>id (PK) (int)<br />
title: varchar(120)<br />
post_date: datetime</b><br />
description: varchar (255)<br />
<h3>location</h3>
<b>id (PK) (int)<br />
name: varchar(120)<br />
longitude: varchar(120)<br />
latitude : varchar (120)<br /></b>
description: varchar (255)<br />
<h3>comment</h3>
<b>id (PK) (int)<br />
photo_id (FK1)<br />
post_date: datetime<br />
content: varchar(255)</b><br />
like_id(FK2)<br />
<h3>like</h3>
<b>id (PK) (int)<br />
follower_id(FK1)</b><br />
photo_id (FK2)<br />
comment_id(FK3)<br />


<h2>Use of the database</h2>

<p>We will use this database to see:<br />
* The followers to an account<br />
* The photos shared by an account<br />
* If the photo belongs to an album<br />
* The comments on a photo<br />
* The like on photos and comments, and by which follower<br /></p>

<h2>Relation between tables description</h2>
<p >* An account have zero or many followers.<br />
* Each follower have only one personal account.<br />
* There is a many to many relation between account and photo.<br />
* Photo_account is a bridge table.<br />
* An album have one or many photos.<br />
* A photocan be in zero or many albums.<br />
* A comment or a photo have zero or many likes.</p>
