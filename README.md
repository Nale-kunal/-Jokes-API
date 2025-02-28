# 🎭 Jokes API - Express.js RESTful API for Jokes  

## 📌 Project Overview  
Jokes API is a simple RESTful API built using **Node.js** and **Express.js**, designed to manage a collection of jokes. It allows users to **fetch, add, update, delete, and filter jokes** through HTTP requests.  

## 🚀 Features  
✅ **Get Random Joke** – Fetch a random joke from the collection.  
✅ **Get Joke by ID** – Retrieve a specific joke using its ID.  
✅ **Filter Jokes by Type** – Fetch jokes based on categories like Science, Puns, Wordplay, etc.  
✅ **Add a New Joke** – Add a joke with its category using a POST request.  
✅ **Update Existing Joke** – Modify a joke's text or type using PUT/PATCH requests.  
✅ **Delete a Specific Joke** – Remove a joke from the collection.  
✅ **Delete All Jokes (Admin Only)** – Clear all jokes using a master authentication key.  

## ⚙️ Tech Stack  
- **Backend:** Node.js, Express.js  
- **Middleware:** Body-parser  
- **Database:** In-memory JavaScript array (can be extended to MongoDB or SQL)  

## 📡 API Endpoints  

| Method | Endpoint           | Description |
|--------|-------------------|-------------|
| GET    | `/random`          | Get a random joke |
| GET    | `/jokes/:id`       | Get a joke by its ID |
| GET    | `/filter?type=xyz` | Get jokes filtered by type |
| POST   | `/jokes`           | Add a new joke |
| PUT    | `/jokes/:id`       | Update an entire joke |
| PATCH  | `/jokes/:id`       | Partially update a joke |
| DELETE | `/jokes/:id`       | Delete a specific joke |
| DELETE | `/all?key=MASTER_KEY` | Delete all jokes (requires authentication) |

## 🛠️ Installation & Setup  

1️⃣ **Clone the repository**  
```bash
git clone https://github.com/your-username/jokes-api.git
cd jokes-api
```
2️⃣ **Install dependencies**  
```bash
npm install
```
3️⃣ **Run the server**  
```bash
node index.js
```
The API will start on **localhost:3000**  

## 🔑 Authentication  
- To delete all jokes, pass the **masterKey** (`4VGP2DN-6EWM4SJ-N6FGRHV-Z3PR3TT`) as a query parameter:  
  ```http
  DELETE /all?key=4VGP2DN-6EWM4SJ-N6FGRHV-Z3PR3TT
  ```
- You can modify the masterKey in the code for security.

## 📝 Future Enhancements  
🔹 Connect to a **MongoDB** or **SQL database** for persistence  
🔹 Implement **user authentication** for adding/updating jokes  
🔹 Add a **frontend interface** for better accessibility  
🔹 Deploy on **Render / Vercel / Heroku**  
