# JEXPO Application Database Schema

### Table: JEXPO_Application

| Field Name | Suggested Data Type | Notes |
| :--- | :--- | :--- |
| **application_no** | VARCHAR(20) | **Primary Key** |
| applicant_name | VARCHAR(100) | |
| mobile_no | VARCHAR(15) | |
| email_id | VARCHAR(100) | |
| guardian_relation | VARCHAR(20) | e.g., Father, Mother |
| guardian_name | VARCHAR(100) | |
| gender | VARCHAR(10) | |
| nationality | VARCHAR(30) | |
| state_of_origin | VARCHAR(50) | |
| category | VARCHAR(20) | e.g., General, SC, ST |
| is_physically_challenged | BOOLEAN / VARCHAR(3) | |
| date_of_birth | DATE | |
| aadhar_no | VARCHAR(12) | |

---

### Table: Eligibility_Status
*(Linked via `application_no`)*


| Field Name | Suggested Data Type | Notes |
| :--- | :--- | :--- |
| is_land_loser | BOOLEAN | |
| is_tfw_scheme | BOOLEAN | Tuition Fee Waiver |
| is_ward_ex_serviceman | BOOLEAN | |

---

### Table: Examination_Preferences

| Field Name | Suggested Data Type | Notes |
| :--- | :--- | :--- |
| exam_zone_choice_1 | VARCHAR(50) | Includes name and code |
| exam_zone_choice_2 | VARCHAR(50) | |

---

### Table: Address_Details

| Field Name | Suggested Data Type | Notes |
| :--- | :--- | :--- |
| address_line | TEXT | Full street/quarter info |
| sub_division | VARCHAR(50) | |
| district | VARCHAR(50) | |
| state | VARCHAR(50) | |
| pin_code | VARCHAR(10) | |

---

### Table: Payment_Details

| Field Name | Suggested Data Type | Notes |
| :--- | :--- | :--- |
| amount_paid | DECIMAL(10,2) | |
| payment_status | VARCHAR(20) | e.g., Validated, Pending |
