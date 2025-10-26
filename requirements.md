# Backend Requirement Specifications

## 1. User Authentication
- **Endpoints:**
  - `POST /api/register` → Register new user  
  - `POST /api/login` → Login and return JWT  
- **Input:** email, password  
- **Output:** success/error message  
- **Validation:** valid email, min 8-char password  
- **Performance:** respond within 2 seconds

---

## 2. Property Management
- **Endpoints:**
  - `POST /api/properties` → Add property  
  - `GET /api/properties/:id` → View property  
  - `PUT /api/properties/:id` → Update property  
  - `DELETE /api/properties/:id` → Delete property  
- **Input:** title, price, location  
- **Validation:** title required, price > 0  
- **Performance:** queries under 2 seconds

---

## 3. Booking System
- **Endpoints:**
  - `POST /api/bookings` → Create booking  
  - `GET /api/bookings/:id` → Get booking info  
- **Input:** property_id, user_id, dates  
- **Validation:** no overlapping dates  
- **Performance:** handle 50 requests/sec
