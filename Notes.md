I want to build an app that displays profiles for children who are sponsored or need to be sponsored.
The index page lists all children that can be sponsored
Only admins can CRUD children
CRUD functionalities for children

AdminUser (Can CRUD a Child)
  username
  password


User (Can sponsor a Child)
  has_many children
  has_many comments
  has_many children, through comments
  
  username
  password
  

Child
  belongs_to user
  has_many comments
  has_many users, through comments
  has_many categories

  name
  student_id
  gender
  birthdate
  sponsored/unsponsored
  

Category
  belongs_to child
  
  gender
  home_name
  girls
  boys
  sponsored
  unsponsored


Comment
  belongs_to user
  belogns_to child

  content