# Compiled Form Modules
*.fmx

# Compiled Menu Modules
*.mmx

# Compiled Pre-Linked Libraries
*.plx
/* Final project for Data Warehousing
Instructor: Dr. Tom Carlile
Summer 2015
*/
--Creating admin staff table which is not connected to any other table
CREATE TABLE admin_staff
  (
    staff_id   NUMBER(3,0) NOT NULL PRIMARY KEY,
    first_name VARCHAR2(25) NOT NULL,
    last_name  VARCHAR2(25) NOT NULL,
    phone      VARCHAR2(15),
    email      VARCHAR2(25),
    title      VARCHAR2(20)
  );
--Creating teacher table  with PK teacher_id but no foreign key
CREATE TABLE teacher
  (
    teacher_id NUMBER(3,0) NOT NULL PRIMARY KEY,
    first_name VARCHAR2(25) NOT NULL,
    last_name  VARCHAR2(25) NOT NULL,
    phone      VARCHAR2(15),
    email      VARCHAR2(25),
    subject    VARCHAR2(15)
  );
--creating guardian table  with PK guardian_id which refers to adm_id in student table which will be created later
CREATE TABLE guardian
  (
    guardian_id  NUMBER(4,0) NOT NULL ,
    first_name   VARCHAR2(25) NOT NULL,
    last_name    VARCHAR2(25) NOT NULL,
    relationship VARCHAR2(15),
    phone        VARCHAR2(15),
    adm_no       NUMBER(4,0) NOT NULL,
    PRIMARY KEY(guardian_id, adm_no)
  );
--creating sponsor table with FK adm_id in student table which will be created later
CREATE TABLE sponsor_table
  (
    sponsor_id        NUMBER(4,0) NOT NULL ,
    first_name        VARCHAR2(25 byte) NOT NULL,
    last_name         VARCHAR2(25 byte) NOT NULL,
    country           VARCHAR2(25 byte),
    province_or_state VARCHAR2(25 byte),
    street_address    VARCHAR2(64 byte),
    email             VARCHAR2(64 byte),
    phone             VARCHAR2(15 byte),
    adm_no            NUMBER(4,0) NOT NULL,
    PRIMARY KEY(sponsor_id, adm_no)
  );
--student table contains multiple FK and contains a recursive relationship
CREATE TABLE student_table
  (
    adm_no      NUMBER(4,0) NOT NULL PRIMARY KEY,
    first_name  VARCHAR2(25 byte) NOT NULL,
    last_name   VARCHAR2(25 byte) NOT NULL,
    hometown    VARCHAR2(25 byte),
    district    VARCHAR2(25 byte),
    mentor      NUMBER(4,0),
    guardian_id NUMBER(4,0),
    sponsor_id  NUMBER(4,0)
  );
CREATE TABLE grade_level
  (
    grade         VARCHAR2(2 byte) NOT NULL ,
    academic_year VARCHAR2(4 byte) NOT NULL,
    adm_no        NUMBER(4,0) NOT NULL,
    percentage    NUMBER(5, 2),
    class_rank    NUMBER(2, 0),
    teacher_id    NUMBER(3,0),
    PRIMARY KEY (grade, academic_year, adm_no)
  );
/*
Now i will insert data in each of the table
The table has been created and the some constraints are already in
tables. Some more will be created after the values are inserted
*/
--admin_staff
INSERT
INTO admin_staff VALUES
  (
    101,
    'Fernand',
    'Hanks',
    '212-555-1212',
    'hanks@gmail.com',
    'manager'
  );
INSERT
INTO admin_staff VALUES
  (
    102,
    'Tom',
    'Wojick',
    '212-555-1212',
    'woji@aol.com',
    'accountant'
  );
INSERT
INTO admin_staff VALUES
  (
    103,
    'Nina',
    'Schorin',
    '212-555-1222',
    'nina@mail.com',
    'cook'
  );
INSERT
INTO admin_staff VALUES
  (
    104,
    'Gary',
    'Pertez',
    '213-555-1212',
    'pete@yahoo.com',
    'peon'
  );
INSERT
INTO admin_staff VALUES
  (
    105,
    'Anita',
    'Morris',
    '212-655-1212',
    'ant@aol.com',
    'maintainance'
  );
INSERT
INTO admin_staff VALUES
  (
    106,
    'Todd',
    'Smythe',
    '212-555-1214',
    NULL,
    'guard'
  );
INSERT
INTO admin_staff VALUES
  (
    107,
    'Marilyn',
    'Frantzen',
    NULL,
    'mary@aol.com',
    'store-keeper'
  );
INSERT
INTO admin_staff VALUES
  (
    108,
    'Charles',
    'Lowry',
    '222-555-1212',
    'clo@gmail.com',
    NULL
  );
INSERT
INTO admin_staff VALUES
  (
    109,
    'Rick',
    'Chow',
    '212-212-1212',
    NULL,
    'sweeper'
  );
INSERT
INTO admin_staff VALUES
  (
    110,
    'Irene',
    'Willig',
    '212-566-1212',
    'ire@gmail.com',
    'secretary'
  );
--teacher
INSERT
INTO teacher VALUES
  (
    102,
    'Fred',
    'Crocitto',
    '718-555-5555',
    'cfred@aol.com',
    'math'
  );
INSERT
INTO teacher VALUES
  (
    103,
    'J.',
    'Landry',
    '201-555-5555',
    'l.j@school.com',
    'physics'
  );
INSERT
INTO teacher VALUES
  (
    104,
    'Laetia',
    'Enison',
    '718-555-5555',
    'laetia@aol.com',
    'chemistry'
  );
INSERT
INTO teacher VALUES
  (
    105,
    'Angel',
    'Moskowitz',
    '201-555-5555',
    'ang@school.com',
    'biology'
  );
INSERT
INTO teacher VALUES
  (
    106,
    'Judith',
    'Olvsade',
    '201-555-5555',
    'judy@school.com',
    'astronomy'
  );
INSERT
INTO teacher VALUES
  (
    107,
    'Catherine',
    'Mierzwa',
    '718-555-5555',
    'caty@school.com',
    'history'
  );
INSERT
INTO teacher VALUES
  (
    108,
    'Judy',
    'Sethi',
    '617-555-5555',
    'lary@school.com',
    'geography'
  );
INSERT
INTO teacher VALUES
  (
    109,
    'Larry',
    'Walter',
    '718-555-5555',
    'judy@school.com',
    'social studies'
  );
INSERT
INTO teacher VALUES
  (
    110,
    'Maria',
    'Martin',
    '718-555-5555',
    'mari@school.com',
    'english'
  );
INSERT
INTO teacher VALUES
  (
    111,
    'Peggy',
    'Noviello',
    NULL,
    'pegy@school.com',
    'nepali'
  );
INSERT
INTO teacher VALUES
  (
    112,
    'Thomas',
    'Thomas',
    '201-555-5555',
    'tom@school.com',
    'german'
  );
INSERT
INTO teacher VALUES
  (
    113,
    'Anil',
    'Kulina',
    '718-555-5555',
    'anil@school.com',
    'french'
  );
INSERT
INTO teacher VALUES
  (
    114,
    'Winsome',
    'Laporte',
    '718-555-5555',
    'lwin@school.com',
    'environment'
  );
INSERT
INTO teacher VALUES
  (
    117,
    'N',
    'Kuehn',
    '718-555-5555',
    'k.n@school.com',
    'sports'
  );
INSERT
INTO teacher VALUES
  (
    118,
    'Hiedi',
    'Lopez',
    '203-555-5555',
    'hiedi@aol.com',
    'economics'
  );
INSERT
INTO teacher VALUES
  (
    119,
    'Mardig',
    'Abdou',
    '718-555-5555',
    'mardi@aol.com',
    'accounting'
  );
INSERT
INTO teacher VALUES
  (
    120,
    'Ralph',
    'Alexander',
    '718-555-5555',
    'ralph@aol.com',
    'computer'
  );
INSERT
INTO teacher VALUES
  (
    121,
    'Sean',
    'Pineda',
    '212-555-5555',
    'sean@school.com',
    'arts'
  );
INSERT
INTO teacher VALUES
  (
    122,
    'Julita',
    'Lippen',
    '718-555-5555',
    'juli@school.com',
    'music'
  );
INSERT
INTO teacher VALUES
  (
    123,
    'Pierre',
    'Radicola',
    '718-555-5555',
    'pier@school.com',
    'dance'
  );
--guardian
INSERT
INTO guardian VALUES
  (
    3001,
    'Fred',
    'Silva',
    'Father',
    '2455335465',
    2001
  );
INSERT
INTO guardian VALUES
  (
    3002,
    'Bryant',
    'Dowd',
    'Brother',
    '2455335475',
    2002
  );
INSERT INTO guardian VALUES
  (3003,'Steph','Silva','Aunt','2455335485',2003
  );
INSERT
INTO guardian VALUES
  (
    3004,
    'Kristi',
    'March',
    'Mother',
    '2455335466',
    2004
  );
INSERT INTO guardian VALUES
  (3005,'Dave','March','Uncle','2455335467',2005
  );
INSERT
INTO guardian VALUES
  (
    3006,
    'Taj',
    'Gibson',
    'Grandfather',
    '2455335468',
    2006
  );
INSERT
INTO guardian VALUES
  (
    3007,
    'Tajika',
    'Silva',
    'Grandmothre',
    '2455335469',
    2007
  );
INSERT INTO guardian VALUES
  (3008,'Uncle','Tom','Uncle','2455335470',2008
  );
INSERT
INTO guardian VALUES
  (
    3009,
    'Harry',
    'Peace',
    'Brother',
    '2455335471',
    2009
  );
INSERT INTO guardian VALUES
  (3010,'Sam','Cassa','Father','2455335472',2010
  );
INSERT INTO guardian VALUES
  (3011,'Doug','Bolle','Father','2455335473',2011
  );
INSERT
INTO guardian VALUES
  (
    3012,
    'Frecks',
    'Famma',
    'Cousin',
    '2455335474',
    2012
  );
INSERT
INTO guardian VALUES
  (
    3013,
    'Drake',
    'Docta',
    'Cousin',
    '2455335476',
    2014
  );
INSERT
INTO guardian VALUES
  (
    3014,
    'Fredrika',
    'Silvastone',
    'Great Uncle',
    '2455335477',
    2015
  );
INSERT
INTO guardian VALUES
  (
    3015,
    'Heather',
    'Silva',
    'Mother',
    '2455335478',
    2016
  );
INSERT
INTO guardian VALUES
  (
    3016,
    'Freddie',
    'Rosco',
    'Father',
    '2455335479',
    2017
  );
INSERT
INTO guardian VALUES
  (
    3017,
    'Fredriks',
    'Miller',
    'Father',
    '2455335480',
    2018
  );
INSERT
INTO guardian VALUES
  (
    3018,
    'Fried',
    'Peters',
    'Father',
    '2455335481',
    2019
  );
INSERT INTO guardian VALUES
  (3019,'Fran','Silva','Mother','2455335482',2020
  );
INSERT INTO guardian VALUES
  (3020,'Dred','Silva','Father','2455335483',2021
  );
INSERT
INTO guardian VALUES
  (
    3021,
    'Kilo',
    'Charlie',
    'Mother',
    '2455335484',
    2022
  );
INSERT
INTO guardian VALUES
  (
    3022,
    'Kima',
    'Silver',
    'Father',
    '2455335490',
    2023
  );
INSERT
INTO guardian VALUES
  (
    3023,
    'Nina',
    'Dilver',
    'Father',
    '2455335460',
    2024
  );
INSERT INTO guardian VALUES
  (3024,'Fama','Fama','Aunt','2455335486',2025
  );
INSERT INTO guardian VALUES
  (3025,'Dil','Tamang','Father','2455335487',2026
  );
INSERT
INTO guardian VALUES
  (
    3026,
    'Yakub',
    'Habsee',
    'Father',
    '2455335488',
    2027
  );
INSERT
INTO guardian VALUES
  (
    3027,
    'Chris',
    'Harris',
    'Father',
    '2455335489',
    2028
  );
INSERT
INTO guardian VALUES
  (
    3028,
    'Christa',
    'Harris',
    'Mother',
    '2455335491',
    2029
  );
INSERT
INTO guardian VALUES
  (
    3029,
    'Ramen',
    'Noodles',
    'Father',
    '2455335493',
    2030
  );
INSERT
INTO guardian VALUES
  (
    3030,
    'Chicken',
    'McDonald',
    'Cousin',
    '2455335497',
    2031
  );
--sponsor_table
INSERT
INTO sponsor_table VALUES
  (
    1001,
    'Prabhat',
    'Raut',
    'USA',
    'IA',
    '416 E st.',
    'raut123@gmail.com',
    '319-961-3391',
    2001
  );
INSERT
INTO sponsor_table VALUES
  (
    1002,
    'Tenzing',
    'Bajracharya',
    'USA',
    'IA',
    '417 G st.',
    'tenz123@gmail.com',
    '319-961-3392',
    2002
  );
INSERT
INTO sponsor_table VALUES
  (
    1003,
    'Mike',
    'Murphy',
    'USA',
    'IA',
    '418 E st.',
    'mike123@gmail.com',
    '319-961-3393',
    2003
  );
INSERT
INTO sponsor_table VALUES
  (
    1004,
    'Tom',
    'Ertz',
    'USA',
    'IA',
    '419 E st.',
    'tom123@gmail.com',
    '319-961-3394',
    2004
  );
INSERT
INTO sponsor_table VALUES
  (
    1005,
    'Elizabeth',
    'Agey',
    'USA',
    'IA',
    '420 E st.',
    'agey123@gmail.com',
    '319-961-3395',
    2005
  );
INSERT
INTO sponsor_table VALUES
  (
    1006,
    'Liz',
    'Seffrin',
    'USA',
    'IA',
    '421 E st.',
    'liz123@gmail.com',
    '319-961-3396',
    2006
  );
INSERT
INTO sponsor_table VALUES
  (
    1007,
    'Russel',
    'Karim',
    'USA',
    'IA',
    '422 E st.',
    'karim123@gmail.com',
    '319-961-3397',
    2007
  );
INSERT
INTO sponsor_table VALUES
  (
    1008,
    'Kancho',
    'Kami',
    'USA',
    'IA',
    '423 E st.',
    'kami123@gmail.com',
    '319-961-3398',
    2008
  );
INSERT
INTO sponsor_table VALUES
  (
    1009,
    'Puntey',
    'Chettri',
    'USA',
    'IA',
    '424 E st.',
    'puntey123@gmail.com',
    '319-961-3399',
    2009
  );
INSERT
INTO sponsor_table VALUES
  (
    1010,
    'Kaley',
    'Damai',
    'USA',
    'IA',
    '425 E st.',
    'kaley123@gmail.com',
    '319-961-3310',
    2010
  );
INSERT
INTO sponsor_table VALUES
  (
    1011,
    'Hari',
    'Gouchan',
    'USA',
    'IA',
    '426 E st.',
    'hari123@gmail.com',
    '319-961-3311',
    2011
  );
INSERT
INTO sponsor_table VALUES
  (
    1012,
    'Ashis',
    'Dahal',
    'USA',
    'IA',
    '427 E st.',
    'dalal123@gmail.com',
    '319-961-3312',
    2012
  );
INSERT
INTO sponsor_table VALUES
  (
    1014,
    'Bivek',
    'Mainali',
    'USA',
    'IA',
    '428 E st.',
    'daari123@gmail.com',
    '319-961-3313',
    2014
  );
INSERT
INTO sponsor_table VALUES
  (
    1015,
    'Meena',
    'Gurung',
    'USA',
    'IA',
    '429 E st.',
    'dalle123@gmail.com',
    '319-961-3314',
    2015
  );
INSERT
INTO sponsor_table VALUES
  (
    1016,
    'Kul',
    'Magar',
    'USA',
    'IA',
    '430 E st.',
    'sungur123@gmail.com',
    '319-961-3315',
    2016
  );
INSERT
INTO sponsor_table VALUES
  (
    1017,
    'Raja',
    'Timilsina',
    'USA',
    'IA',
    '431 E st.',
    'budo_bachha@gmail.com',
    '319-961-3316',
    2017
  );
INSERT
INTO sponsor_table VALUES
  (
    1018,
    'Anit',
    'Kaley',
    'USA',
    'IA',
    '432 E st.',
    'kaley@gmail.com',
    '319-961-3317',
    2018
  );
INSERT
INTO sponsor_table VALUES
  (
    1019,
    'Radha',
    'Shrestha',
    'USA',
    'IA',
    '433 E st.',
    'moti@gmail.com',
    '319-961-3318',
    2019
  );
INSERT
INTO sponsor_table VALUES
  (
    1020,
    'Sangita',
    'Shrestha',
    'USA',
    'IA',
    '434 E st.',
    'kachhu@gmail.com',
    '319-961-3319',
    2020
  );
INSERT
INTO sponsor_table VALUES
  (
    1021,
    'Sara',
    'Sapkota',
    'USA',
    'IA',
    '435 E st.',
    'sara.sapkota@gmail.com',
    '319-961-3320',
    2021
  );
INSERT
INTO sponsor_table VALUES
  (
    1022,
    'Sohil',
    'Poudel',
    'USA',
    'IA',
    '436 E st.',
    'naikap@gmail.com',
    '319-961-3321',
    2022
  );
INSERT
INTO sponsor_table VALUES
  (
    1023,
    'Sijan',
    'Guragain',
    'USA',
    'IA',
    '437 E st.',
    'alien@gmail.com',
    '319-961-3322',
    2023
  );
INSERT
INTO sponsor_table VALUES
  (
    1024,
    'Shrijal',
    'Rupakhati',
    'USA',
    'IA',
    '438 E st.',
    'image_vj@gmail.com',
    '319-961-3323',
    2024
  );
INSERT
INTO sponsor_table VALUES
  (
    1025,
    'Binod',
    'Gautam',
    'USA',
    'IA',
    '439 E st.',
    'photographer@gmail.com',
    '319-961-3324',
    2025
  );
INSERT
INTO sponsor_table VALUES
  (
    1026,
    'Nischal',
    'Karki',
    'USA',
    'IA',
    '440 E st.',
    'challa@gmail.com',
    '319-961-3325',
    2026
  );
INSERT
INTO sponsor_table VALUES
  (
    1027,
    'Prakat',
    'Khati',
    'USA',
    'IA',
    '442 E st.',
    'md_feature@gmail.com',
    '319-961-3326',
    2027
  );
INSERT
INTO sponsor_table VALUES
  (
    1028,
    'Rishav',
    'Khand',
    'USA',
    'IA',
    '441 E st.',
    'biker@gmail.com',
    '319-961-3327',
    2028
  );
INSERT
INTO sponsor_table VALUES
  (
    1029,
    'Roshan',
    'Lekhak',
    'USA',
    'IA',
    '443 E st.',
    'teen_patti@gmail.com',
    '319-961-3328',
    2029
  );
INSERT
INTO sponsor_table VALUES
  (
    1030,
    'Chandan',
    'Jha',
    'USA',
    'IA',
    '444 E st.',
    'nobelist@gmail.com',
    '319-961-3329',
    2030
  );
INSERT
INTO sponsor_table VALUES
  (
    1031,
    'Ayush',
    'Bhtta',
    'USA',
    'IA',
    '445 E st.',
    'prem_pidit@gmail.com',
    '319-961-3330',
    2031
  );
--student_table
INSERT
INTO student_table VALUES
  (
    2001,
    'Prabhat',
    'Raut',
    'Jhapa',
    'Chandragadhi',
    2031,3001,1001
  );
INSERT
INTO student_table VALUES
  (
    2002,
    'Tenzing',
    'Bajracharya',
    'Oochu',
    'Lalitpur',
    2030,3002,1002
  );
INSERT
INTO student_table VALUES
  (
    2003,
    'Mike',
    'Murphy',
    'Sallaghari',
    'Bhaktapur',
    2029,3003,1003
  );
INSERT
INTO student_table VALUES
  (
    2004,
    'Tom',
    'Ertz',
    'Naikap',
    'Kathmandu',
    2028,3004,1004
  );
INSERT
INTO student_table VALUES
  (
    2005,
    'Elizabeth',
    'Agey',
    'Khanikhola',
    'Dhading.',
    2027,3005,1005
  );
INSERT
INTO student_table VALUES
  (
    2006,
    'Liz',
    'Seffrin',
    'Chapagaun',
    'Baitadi',
    2026,3006,1006
  );
INSERT
INTO student_table VALUES
  (
    2007,
    'Russel',
    'Karim',
    'Chautaro',
    'Sindupalchowk',
    2025,3007,1007
  );
INSERT
INTO student_table VALUES
  (
    2008,
    'Kancho',
    'Kami',
    'Chiyabagan',
    'Illam',
    2024,3008,1008
  );
INSERT
INTO student_table VALUES
  (
    2009,
    'Puntey',
    'Chettri',
    'Lagankhel',
    'Biratnagar',
    2023,3009,1009
  );
INSERT
INTO student_table VALUES
  (
    2010,
    'Kaley',
    'Damai',
    'Satdobato',
    'Sunsari',
    2022,3010,1010
  );
INSERT
INTO student_table VALUES
  (
    2011,
    'Hari',
    'Gouchan',
    'Kagbeni',
    'Jomsom',
    2021,3011,1011
  );
INSERT
INTO student_table VALUES
  (
    2012,
    'Ashis',
    'Dahal',
    'Marpha',
    'Mustang',
    2020,3012,1012
  );
INSERT
INTO student_table VALUES
  (
    2014,
    'Bivek',
    'Mainali',
    'Khonj',
    'Manang',
    2019,3013,1014
  );
INSERT
INTO student_table VALUES
  (
    2015,
    'Meena',
    'Gurung',
    'hattiban',
    'Dhanusa',
    '2018',
    '3014',
    1015
  );
INSERT
INTO student_table VALUES
  (
    2016,
    'Kul',
    'Magar',
    'Imadol',
    'Saptari',
    2017,3015,1016
  );
INSERT
INTO student_table VALUES
  (
    2017,
    'Raja',
    'Timilsina',
    'Gwarkho',
    'Bardia',
    2016,3016,1017
  );
INSERT
INTO student_table VALUES
  (
    2018,
    'Anit',
    'Kaley',
    'Tansen',
    'Palpa',
    2015,3017,1018
  );
INSERT
INTO student_table VALUES
  (
    2019,
    'Radha',
    'Shrestha',
    'Besi',
    'Syangja',
    2014,3018,1019
  );
INSERT
INTO student_table VALUES
  (
    2020,
    'Sangita',
    'Shrestha',
    'lumbini',
    'Bhairawa',
    2012,3019,1020
  );
INSERT
INTO student_table VALUES
  (
    2021,
    'Sara',
    'Sapkota',
    'Gaidakot',
    'Nawalparasi',
    2011,3020,1021
  );
INSERT
INTO student_table VALUES
  (
    2022,
    'Sohil',
    'Poudel',
    'sanepa',
    'Khotang',
    2010,3021,1022
  );
INSERT
INTO student_table VALUES
  (
    2023,
    'Sijan',
    'Guragain',
    'Salleri',
    'Solukhumbu',
    2009,3022,1023
  );
INSERT
INTO student_table VALUES
  (
    2024,
    'Shrijal',
    'Rupakhati',
    'Kirtipur',
    'Siraha',
    2008,3023,1024
  );
INSERT
INTO student_table VALUES
  (
    2025,
    'Binod',
    'Gautam',
    'Siddharthanagar',
    'Rupendhi',
    2007,3024,1025
  );
INSERT
INTO student_table VALUES
  (
    2026,
    'Nischal',
    'Karki',
    'Mygadi',
    'Beni',
    2006,3025,1026
  );
INSERT
INTO student_table VALUES
  (
    2027,
    'Prakat',
    'Khati',
    'Pokhara',
    'Kaski',
    2005,3026,1027
  );
INSERT
INTO student_table VALUES
  (
    2028,
    'Rishav',
    'Khand',
    'Byas',
    'Tanahun.',
    2004,3027,1028
  );
INSERT
INTO student_table VALUES
  (
    2029,
    'Roshan',
    'Lekhak',
    'Janakpur',
    'Kapilvastu',
    2003,3028,1029
  );
INSERT
INTO student_table VALUES
  (
    2030,
    'Chandan',
    'Jha',
    'Sandhikharka',
    'Arghakhanchi',
    2002,3029,1030
  );
INSERT
INTO student_table VALUES
  (
    2031,
    'Ayush',
    'Bhtta',
    'Tamghas',
    'Gulmi',
    2001,3030,1031
  );
--grade_level
INSERT INTO grade_level VALUES
  ('1','2001',2001,70.5,NULL,102
  );
INSERT INTO grade_level VALUES
  ('1', '2001',2002,71.0,NULL,102
  );
INSERT INTO grade_level VALUES
  ('1', '2001',2003,85.0,NULL,102
  );
INSERT INTO grade_level VALUES
  ('1', '2001',2004,97.0,NULL,102
  );
INSERT INTO grade_level VALUES
  ('1', '2000',2005,57.0,NULL,104
  );
INSERT INTO grade_level VALUES
  ('1', '2000',2006,66.5,NULL,104
  );
INSERT INTO grade_level VALUES
  ('1', '2000',2007,69.5,NULL,104
  );
INSERT INTO grade_level VALUES
  ('1', '2000',2008,80.0,NULL,104
  );
INSERT INTO grade_level VALUES
  ('1', '2000',2009,81.0,NULL,104
  );
INSERT INTO grade_level VALUES
  ('1', '2000',2010,35.0,NULL,104
  );
INSERT INTO grade_level VALUES
  ('1', '2001',2010,57.0,NULL,102
  );
INSERT INTO grade_level VALUES
  ('2', '2000',2012,80.0,NULL,103
  );
INSERT INTO grade_level VALUES
  ('2', '2000',2014,81.0,NULL,103
  );
INSERT INTO grade_level VALUES
  ('2', '2000',2015,80.5,NULL,103
  );
INSERT INTO grade_level VALUES
  ('2', '2000',2016,82.0,NULL,103
  );
INSERT INTO grade_level VALUES
  ('2', '2000',2017,83.0,NULL,103
  );
INSERT INTO grade_level VALUES
  ('2', '2001',2005,81.5,NULL,104
  );
INSERT INTO grade_level VALUES
  ('2', '2001',2006,86.5,NULL,104
  );
INSERT INTO grade_level VALUES
  ('2', '2001',2007,95.0,NULL,104
  );
INSERT INTO grade_level VALUES
  ('2', '2001',2008,78.0,NULL,104
  );
INSERT INTO grade_level VALUES
  ('2', '2001',2009,91.0,NULL,104
  );
INSERT INTO grade_level VALUES
  ('3', '2000',2011,34.5,NULL,105
  );
INSERT INTO grade_level VALUES
  ('3', '2000',2018,67.5,NULL,105
  );
INSERT INTO grade_level VALUES
  ('3', '2000',2019,77.0,NULL,105
  );
INSERT INTO grade_level VALUES
  ('3', '2000',2020,81.5,NULL,105
  );
INSERT INTO grade_level VALUES
  ('3', '2001',2011,93.0,NULL,106
  );
INSERT INTO grade_level VALUES
  ('3', '2000',2021,39.0,NULL,105
  );
INSERT INTO grade_level VALUES
  ('3', '2001',2021,90.0,NULL,106
  );
INSERT INTO grade_level VALUES
  ('3', '2001',2012,87.0,NULL,106
  );
INSERT INTO grade_level VALUES
  ('3', '2001',2014,88.5,NULL,106
  );
INSERT INTO grade_level VALUES
  ('3', '2001',2015,87.5,NULL,106
  );
INSERT INTO grade_level VALUES
  ('3', '2001',2016,83.0,NULL,106
  );
INSERT INTO grade_level VALUES
  ('3', '2001',2017,88.0,NULL,106
  );
INSERT INTO grade_level VALUES
  ('3', '2001',2019,77.0,NULL,106
  );
INSERT INTO grade_level VALUES
  ('4', '2001',2030,65.0,NULL,110
  );
INSERT INTO grade_level VALUES
  ('4', '2001',2020,73.0,NULL,110
  );
INSERT INTO grade_level VALUES
  ('4', '2001',2022,88.0,NULL,110
  );
INSERT INTO grade_level VALUES
  ('4', '2001',2023,79.0,NULL,110
  );
INSERT INTO grade_level VALUES
  ('4', '2001',2024,75.0,NULL,110
  );
INSERT INTO grade_level VALUES
  ('4', '2001',2025,82.0,NULL,110
  );
INSERT INTO grade_level VALUES
  ('4', '2001',2026,77.5,NULL,110
  );
INSERT INTO grade_level VALUES
  ('4', '2001',2027,88.0,NULL,110
  );
INSERT INTO grade_level VALUES
  ('4', '2001',2028,33.0,NULL,110
  );
--Adding foreign key constraints
ALTER TABLE grade_level ADD CONSTRAINT teacher_grade_fk FOREIGN KEY
(
  teacher_id
)
REFERENCES teacher
(
  teacher_id
)
;
ALTER TABLE grade_level ADD CONSTRAINT stu_grade_fk FOREIGN KEY
(
  adm_no
)
REFERENCES student_table
(
  adm_no
)
;
ALTER TABLE student_table ADD CONSTRAINT adm_adm_fk FOREIGN KEY
(
  mentor
)
REFERENCES student_table
(
  adm_no
)
;
ALTER TABLE student_table ADD CONSTRAINT sponsor_student_fk FOREIGN KEY
(
  sponsor_id
)
REFERENCES sponsor_table
(
  sponsor_id
)
;
ALTER TABLE student_table ADD CONSTRAINT guardian_stu_fk FOREIGN KEY
(
  guardian_id
)
REFERENCES guardian
(
  guardian_id
)
;
ALTER TABLE guardian ADD CONSTRAINT stu_guardian_fk FOREIGN KEY
(
  adm_no
)
REFERENCES student_table
(
  adm_no
)
;
ALTER TABLE sponsor_table ADD CONSTRAINT stu_sponsor_fk FOREIGN KEY
(
  adm_no
)
REFERENCES student_table
(
  adm_no
)
;
COMMIT;
ALTER TABLE student_table ADD CONSTRAINT check_student_name CHECK
(
  adm_no>= 2000
)
;
