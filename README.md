# PharmaCare Pro | Enterprise Pharmacy Inventory & Sales Management System

> **University DBMS Final Project**  
> **Course:** Database Management Systems (DBMS)  
> **Batch:** 25-Batch  
> **Assigned Group:** Group No. 07  
> **Topic:** Pharmacy Inventory and Sales System  
> **Platform:** SQL Server Management Studio (SSMS) & Microsoft SQL Server 2019/2022/2025  

---

## 👥 Group Members (Group No. 07)

| Roll No. | Student Name | Assigned Role |
| :--- | :--- | :--- |
| **25F-DS-019** | **Faraz** (Project Lead) | Full-Stack Architecture, Database Design & Stored Procedures |
| **25F-DS-028** | **Adeena Amjad** | Frontend POS, UI/UX Components & Testing |
| **25F-DS-033** | **Hadin Tariq** | SQL Views, Triggers & Backend Routing |
| **25F-DS-035** | **Mahruk Khan** | Reporting Queries, Documentation & Data Seeding |
| **25F-DS-038** | **Abdul Moiz** | Supplier & Procurement Module |
| **25F-DS-039** | **Talha Siddiqui** | Customer Loyalty & Returns Module |

---

## 🚀 Technology Stack

### Backend & API
- **Language:** Python 3.10+
- **Framework:** FastAPI (RESTful Architecture)
- **ORM & DB Connectivity:** SQLAlchemy 2.0 & PyODBC
- **Database Driver:** Microsoft ODBC Driver 17 / 18 for SQL Server
- **Security & Cryptography:** Passlib, BCrypt password hashing, Python-JOSE (JWT Tokens)
- **Documentation:** Interactive OpenAPI Swagger UI (`/docs`) & ReDoc (`/redoc`)
- **Testing:** Pytest & Starlette TestClient

### Database
- **Engine:** Microsoft SQL Server 2019 / 2022 / 2025
- **Tool:** SQL Server Management Studio (SSMS)
- **Concepts Implemented:** DDL/DML, Primary/Foreign Keys, Constraints (`CHECK`, `UNIQUE`, `NOT NULL`, `DEFAULT`), 15 Tables, 5 SQL Views, 2 Stored Procedures, 2 Database Triggers, and 15 Reporting Queries.

### Frontend
- **Framework:** React.js 18 + Vite
- **Styling:** Tailwind CSS (Modern Emerald & Slate palette)
- **Icons:** Lucide React
- **Analytics & Visualizations:** Recharts (Area charts, Bar charts, Donut charts)
- **Routing:** React Router v6

---

## 📂 Project Architecture

```
pharmacy-inventory-and-sale-system/
├── backend/
│   ├── app/
│   │   ├── __init__.py
│   │   ├── config.py              # Environment settings & DB connection string
│   │   ├── database.py            # SQLAlchemy engine for SQL Server
│   │   ├── models.py              # 15 SQLAlchemy Relational Models
│   │   ├── schemas.py             # Pydantic request/response schemas
│   │   ├── auth.py                # BCrypt verification & JWT token management
│   │   ├── main.py                # FastAPI entrypoint & router registry
│   │   └── routers/
│   │       ├── auth.py            # Authentication & user management
│   │       ├── medicines.py       # Medicine catalog, search & stock adjustment
│   │       ├── categories.py      # Therapeutic drug categories
│   │       ├── suppliers.py       # Supplier directory & performance
│   │       ├── customers.py       # Patient profiles & loyalty tracking
│   │       ├── purchases.py       # Supply procurement & automatic batch generation
│   │       ├── sales.py           # POS billing engine & FEFO stock deduction
│   │       ├── returns.py         # Sales returns & batch restocking
│   │       ├── dashboard.py       # Real-time KPIs, charts & demand forecasting
│   │       ├── reports.py         # 10+ University analytical reporting queries
│   │       └── logs.py            # Security audit trail
│   └── .env                       # Backend environment credentials
├── frontend/
│   ├── src/
│   │   ├── api/axios.js           # Axios instance with JWT interceptor
│   │   ├── context/AuthContext.jsx# React auth context & role checking
│   │   ├── components/
│   │   │   ├── Layout.jsx         # Sidebar navigation & notification banner
│   │   │   ├── ProtectedRoute.jsx # Role-based route guard
│   │   │   └── ReceiptModal.jsx   # Professional printable thermal receipt
│   │   ├── pages/
│   │   │   ├── Login.jsx          # Modern login screen with demo shortcuts
│   │   │   ├── Dashboard.jsx      # Summary metrics, charts & predictive forecasting
│   │   │   ├── POS.jsx            # High-speed Point of Sale checkout
│   │   │   ├── Inventory.jsx      # Medicine catalog, stock alerts & audit adjustments
│   │   │   ├── Purchases.jsx      # Purchase orders & stock replenishment
│   │   │   ├── Suppliers.jsx      # Distributor directory & spend performance
│   │   │   ├── Customers.jsx      # Patient profiles & loyalty ledger
│   │   │   ├── Returns.jsx        # Refund vouchers & batch replenishment
│   │   │   ├── Reports.jsx        # 15 University DBMS analytical reports & CSV export
│   │   │   └── AuditLogs.jsx      # Activity audit logs
│   │   ├── App.jsx
│   │   ├── main.jsx
│   │   └── index.css
│   ├── package.json
│   └── vite.config.js
├── database/
│   ├── schema.sql                 # Complete DDL for 15 tables with university constraints
│   ├── seed_data.sql              # Rich seed data (>= 10 records per core table)
│   ├── views.sql                  # 5 SQL Views for reporting (Advanced Topic 1)
│   ├── stored_procedures.sql      # 2 Transactional Stored Procedures (Advanced Topic 2)
│   ├── triggers.sql               # 2 Database Triggers (Advanced Topic 3)
│   └── reporting_queries.sql      # 15 Comprehensive SQL Analysis Queries
├── documentation/
│   ├── ER_DIAGRAM.md              # Entity-Relationship diagram & cardinality explanation
│   ├── DATABASE_DESIGN.md         # Full relational schema documentation
│   ├── API_DOCUMENTATION.md       # Complete REST API specification
│   └── MANUAL_TESTING_CHECKLIST.md# Step-by-step evaluation guide
├── tests/
│   ├── conftest.py
│   └── test_api.py                # 14 Automated integration tests
├── .env.example
├── .gitignore
└── README.md
```

---

## 🔑 Demo Login Credentials

The database comes pre-seeded with accounts for all roles:

| Role | Username | Password | Full Name | Access Privileges |
| :--- | :--- | :--- | :--- | :--- |
| **Admin** | `admin` | `admin123` | Dr. Faraz Ahmed (Lead) | Complete System Access, User Management, Audit Logs |
| **Pharmacist** | `adeena` | `staff123` | Adeena Amjad | POS Billing, Purchases, Medicine CRUD, Returns, Reports |
| **Pharmacist** | `hadin` | `staff123` | Hadin Tariq | POS Billing, Purchases, Medicine CRUD, Returns, Reports |
| **Staff / Cashier** | `mahruk` | `staff123` | Mahruk Khan | POS Billing, Customer Lookup, Catalog Browsing |
| **Staff / Cashier** | `abdulmoiz` | `staff123` | Abdul Moiz | POS Billing, Customer Lookup, Catalog Browsing |
| **Staff / Cashier** | `talha` | `staff123` | Talha Siddiqui | POS Billing, Customer Lookup, Catalog Browsing |

---

## 🛠️ Installation & Setup Instructions

### Prerequisites
1. **Microsoft SQL Server** (2019, 2022, or 2025) running locally.
2. **Microsoft ODBC Driver 18 for SQL Server** installed.
3. **Python 3.10+**
4. **Node.js (v18+) & npm**

---

### Step 1: Database Setup in SQL Server Management Studio (SSMS)
1. Open **SSMS** and connect to your local SQL Server instance (`localhost`).
2. Open and execute the SQL scripts in the following order:
   ```sql
   1. database/schema.sql             -- Creates PharmacyDB and 15 tables
   2. database/seed_data.sql          -- Inserts >= 10 realistic records per table
   3. database/views.sql              -- Creates 5 Reporting Views
   4. database/stored_procedures.sql  -- Creates Stored Procedures
   5. database/triggers.sql           -- Creates Automatic Triggers
   6. database/reporting_queries.sql  -- Executes & verifies the 15 queries
   ```

*Alternative via command line:*
```powershell
sqlcmd -S localhost -E -C -i database/schema.sql
sqlcmd -S localhost -E -C -i database/seed_data.sql
sqlcmd -S localhost -E -C -i database/views.sql
sqlcmd -S localhost -E -C -i database/stored_procedures.sql
sqlcmd -S localhost -E -C -i database/triggers.sql
sqlcmd -S localhost -E -C -i database/reporting_queries.sql
```

---

### Step 2: Backend Setup (FastAPI)
1. Ensure dependencies are installed:
   ```powershell
   python -m pip install fastapi uvicorn pyodbc sqlalchemy pydantic pydantic-settings python-multipart python-jose[cryptography] passlib[bcrypt] bcrypt httpx email-validator pytest
   ```
2. Start the FastAPI backend server:
   ```powershell
   cd backend
   python -m uvicorn app.main:app --host 127.0.0.1 --port 8000 --reload
   ```
3. Verify backend is running:
   - API Status: `http://localhost:8000/`
   - Interactive Swagger Docs: `http://localhost:8000/docs`

---

### Step 3: Frontend Setup (React + Vite)
1. In a new terminal, navigate to `frontend`:
   ```powershell
   cd frontend
   npm install
   npm run dev
   ```
2. Open your browser and navigate to:
   ```
   http://localhost:5173
   ```

---

## 🧪 Automated Testing

Run the automated test suite with pytest:
```powershell
python -m pytest tests/test_api.py -v
```

**14 automated tests** cover:
- Admin & staff authentication
- Medicine CRUD & price constraint validation (`selling_price >= purchase_price`)
- Barcode lookup
- Supplier directory & spend performance
- Customer creation & loyalty points
- Purchase order creation & automated batch generation
- POS checkout with automated **FEFO** (First Expiry, First Out) batch deduction
- Out-of-stock & expired stock rejection
- Stock adjustments (damage/audit)
- Expiry and low-stock alerts
- University reporting endpoints

---

## ✨ Core Features Implemented

1. **Smart FEFO Inventory Management:** Automatically prioritizes batches with the earliest expiry date during POS checkout and strictly forbids dispensing expired batches.
2. **Barcode Scanner Lookup:** Lookup medicines by scanning standard barcodes with automatic cart addition.
3. **Point of Sale (POS):** Fast multi-item billing, cash change calculation, discount inputs, and printable invoice receipts.
4. **Customer Loyalty Points:** Accumulate points on purchases (1 point per Rs. 100) and redeem points directly for cash discounts during checkout.
5. **Procurement & Auto Batching:** Receiving shipments creates batches with manufacturing lot numbers, purchase prices, and expiry dates, automatically updating inventory stock.
6. **Stock Reconciliation & Wastage Logs:** Track damaged or expired medicine disposal through audit entries.
7. **Predictive Demand Forecasting:** Transparent run-rate velocity calculations based on 30-day dispensing history, predicting days of stock remaining and replenishment urgency.
8. **15 University Analytical Reports:** Live SQL queries and views for inventory valuation, category profit margins, expiry alerts, supplier fulfillment, and best-selling medicines.
9. **Role-Based Access Control (RBAC):** Admin, Pharmacist, and Staff permission tiers with tamper-proof activity logging.
