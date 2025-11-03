Healthcare Appointment Microservices (Starter)
---------------------------------------------
Projects included:
  - eureka-server
  - patient-service (MySQL: patientdb)
  - doctor-service  (MySQL: doctordb)
  - appointment-service (MySQL: appointmentdb)
  - ai-agent-service

Quick start (after editing DB credentials in application.yml):
  1) Create databases: mysql -u root -p < setup-databases.sql
  2) Start eureka-server (port 8761)
  3) Start doctor-service (port 8082) and create a doctor via POST /doctors
  4) Start patient-service (port 8081) and create a patient via POST /patients
  5) Start ai-agent-service (port 8090)
  6) Start appointment-service (port 8083)
  7) Create appointment: POST http://localhost:8083/appointments body: { "patientId":1, "symptoms":"fever and cough", "preferredTime":"2025-11-05T10:00:00" }

Notes:
  - Update MySQL user/password in each service's application.yml before running.
  - This is a starter skeleton. Add validation, exception handling, and security as needed.
