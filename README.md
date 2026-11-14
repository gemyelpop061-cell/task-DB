Patient(
  ID PK,
  Name,
  DOB,
  Ward_ID FK,
  Consultant_ID FK
)

Consultant(
  ID PK,
  Name
)

Ward(
  ID PK,
  Name,
  Supervisor_Nurse_ID FK UNIQUE
)

Nurse(
  ID PK,
  Name,
  Ward_ID FK
)

Drug(
  Code PK,
  Rec_Dosage
)

Drug_Brand(
  Drug_Code PK, FK,
  Brand PK
)

Gives(
  Patient_ID PK, FK,
  Nurse_ID PK, FK,
  Drug_Code PK, FK,
  Date PK,
  Time PK,
  Dosage
)

Examines(
  Patient_ID PK, FK,
  Consultant_ID PK, FK
)



؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟
Sales_Office(
  NUM PK,
  Loc,
  Manager_Employee_ID FK UNIQUE
)

Employee(
  ID PK,
  Name,
  Sales_Office_NUM FK
)

Property(
  ID PK,
  Add,
  City,
  State,
  Zip,
  Sales_Office_NUM FK
)

Owner(
  ID PK,
  Name
)

Has(
  Property_ID PK, FK,
  Owner_ID PK, FK,
  Percent_Owned
)


؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟؟
Musician(
  ID PK,
  Name,
  St,
  City,
  Phone
)

Album(
  ID PK,
  Date,
  Title,
  Musician_ID FK
)

Instrument(
  Name PK,
  Key
)

Song(
  Title PK,
  Author PK,
  Album_ID FK
)

Play_Instrument(
  Musician_ID PK, FK,
  Instrument_Name PK, FK
)

Play_Song(
  Musician_ID PK, FK,
  Song_Title PK, FK,
  Song_Author PK, FK
)
