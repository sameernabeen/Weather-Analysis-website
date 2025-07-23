# Weather Info App

A simple web application that allows users to fetch and view real-time weather information for any city using the [OpenWeatherMap API](https://openweathermap.org/api). Built with Java Servlets, JSP, Maven, and styled with custom CSS. Deployable on Apache Tomcat.

---

## 🖥️ Features

- 🌎 Search current weather for any city worldwide
- 🌡 Displays temperature, humidity, and conditions in a user-friendly card
- 🎨 Modern, responsive, animated CSS design
- 🔑 Easy configuration of your own OpenWeatherMap API key

---

## 🚀 Getting Started

### 1. **Clone or Download**

git clone https://github.com/sameernabeen/WeatherInfoApp.git
cd WeatherInfoApp

text

Or [Download as ZIP](https://github.com/sameernabeen/WeatherInfoApp/archive/main.zip) and extract.

---

### 2. **Prerequisites**

- Java 11 or higher
- [Apache Tomcat 10+](https://tomcat.apache.org/) (or compatible Jakarta EE 9+ Servlet container)
- [Maven 3+](https://maven.apache.org/)
- Free API key from [OpenWeatherMap](https://openweathermap.org/api)

---

### 3. **Setup**

#### a. **Configure Your API Key**

- Open `src/main/java/com/your/example/WeatherServlet.java`
- Replace the placeholder key with your real API key:
private static final String API_KEY = "YOUR_API_KEY_HERE";

text

#### b. **Build the Project**

mvn clean package

text

#### c. **Deploy to Tomcat**

- Copy the generated `.war` file from `target/WeatherInfoApp.war` to your Tomcat's `webapps/` directory
- Or run directly in Eclipse/IDE

---

### 4. **Usage**

- Start Tomcat
- Open: [http://localhost:9090/WeatherInfoApp/index.jsp](http://localhost:9090/WeatherInfoApp/index.jsp)
- Enter a city name and view real-time weather details

---

## 🛠️ Project Structure

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

## 📦 Dependencies

- `jakarta.servlet-api` (scope: provided)
- `org.json:json` *(for weather result parsing)*

All dependencies managed via Maven; see `pom.xml`.

---

## 🧩 Customization

- **Styling**: Edit `style.css` to adjust layout, colors, or animations.
- **Data Display**: Edit `index.jsp` and `WeatherServlet.java` to add or format fields (like icons, forecasts, etc).

---

## ❓ Troubleshooting

- **API returns 401/403/404**: Double check your API key and its activation, or your city name spelling.
- **Blank Output**: Ensure servlet attribute names match those expected in `index.jsp`.
- **Dependency errors**: Run `Maven > Update Project` or `mvn clean install` in your IDE/CLI.
- **No weather on submit**: Confirm Tomcat logs and console for JSON parsing or network errors.

---

## 📝 License

MIT

---

**Created as a learning project using modern Java web app principles.**
How to use:

Copy all content above into README.md at your project root.

Replace YOUR_API_KEY_HERE, all example usernames/paths as needed.

Update project URLs if you change directory names or artifactId.

