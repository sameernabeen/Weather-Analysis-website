
# 🌦 Weather Info Web Application 🌍

This is a Java-based full stack web application that fetches real-time weather data for any city using the OpenWeatherMap API. Built using **Servlets, JSP, Maven**, and deployed on **Apache Tomcat**, it also features animated UI styling and logs weather queries to a local **text file**.

---

## 👨‍💻 Technologies Used

| Layer        | Tech                              |
|--------------|------------------------------------|
| Backend      | Java Servlets, File I/O (I/O Streams) |
| Frontend     | JSP, HTML, CSS (animated)          |
| Styling      | Custom animation with CSS          |
| Build Tool   | Maven                              |
| Server       | Apache Tomcat 10+                  |
| API Used     | [OpenWeatherMap](https://openweathermap.org/api) |
| IDE          | Eclipse / IntelliJ IDEA            |

---

## 🛠 Features

- 🔍 Search real-time weather by city
- 📊 Displays Temperature, Condition, Humidity
- 🎨 CSS-powered vertical layout with animations
- 🌡 Dynamic color/animation based on temperature
- 📝 Logs searches into a file: `weather-log.txt`
- ⚠️ Graceful error messages for invalid city, API error, parsing fail

---

## 📁 Folder Structure

WeatherInfoApp/
├── src/
│ └── main/
│ ├── java/
│ │ └── com/
│ │ └── your/
│ │ └── example/
│ │ └── WeatherServlet.java
│ └── webapp/
│ ├── index.jsp
│ ├── style.css
│ └── WEB-INF/
│ └── web.xml
├── pom.xml
└── README.md

text

---

## 💻 How It Works

1. User enters a city name in `index.jsp`
2. `WeatherServlet.java` calls OpenWeatherMap API
3. API JSON response is parsed using `org.json`
4. Output is set as request attributes
5. JSP shows city/weather info with animated styling
6. Details are logged to `weather-log.txt`

---

## 📝 File I/O Logging

- `weather-log.txt` is **auto-created** (if it doesn't exist)
- Stored in:
C:/Users/YourUsername/Documents/weather-log.txt

text
- Each entry includes city, temperature, condition, humidity, and timestamp

> ✅ This is done using `BufferedWriter`, `FileWriter`, and `System.getProperty("user.home")`

---

## ⚒ Setup Instructions

### 1. Clone Repo & Import

git clone https://github.com/yourusername/WeatherInfoApp.git
cd WeatherInfoApp

text

### 2. Add Your API Key

Open `WeatherServlet.java`:

private static final String API_KEY = "your_api_key_here";

text

Get your free key from [OpenWeatherMap](https://openweathermap.org/api)

### 3. Build Project

mvn clean install

text

### 4. Deploy on Apache Tomcat

- Copy the `.war` file to `tomcat/webapps/`
- Or run directly inside Eclipse

---

## 🌍 Access Web App

http://localhost:9090/WeatherInfoApp/index.jsp

text

---

## ✅ Sample Output

> Enter a city: `London`  
> Output:
- 📍 City: London
- 🌡 Temperature: 20.3°C (with animation)
- 🌤 Condition: clear sky
- 💧 Humidity: 76%
- Logged to: `/Documents/weather-log.txt`

---

## 📷 Screenshots (optional for GitHub page)
<img width="1389" height="783" alt="Screenshot 2025-07-23 220121" src="https://github.com/user-attachments/assets/70ac1f51-ecff-40a7-b5cf-edf097635b32" />
Log file creates automatically
<img width="1919" height="1037" alt="Screenshot 2025-07-23 220020" src="https://github.com/user-attachments/assets/58a74821-ab75-4961-b27e-ca1c95a29996" />
<img width="1919" height="1026" alt="Screenshot 2025-07-23 220000" src="https://github.com/user-attachments/assets/ca3a9174-8f83-4977-a7ef-b1548945f325" />
 Animated result card with temp color pulse

---

## 🚀 Future Enhancements

- 🔄 Show search history from file
- 📦 Store weather in a database
- 🌐 Detect location automatically
- 🌙 Dark/light mode toggle
- 🧊 Add icons for conditions (`☁️`, `🌧`, `❄`)

---

## 📗 License

MIT License © [Your Name]  
Use freely for educational or personal purposes

---

## 🙌 Acknowledgments

- OpenWeatherMap API
- CSS Gradient Inspiration: CSS-Tricks
- JSON Parsing: `org.json` library

---

**Built with ❤️ using Java Full Stack**
✅ How to Use:
Copy this Markdown into a file named README.md

Replace:

yourusername with your GitHub username

Customize the screenshots or license if needed

Push to your GitHub repository
