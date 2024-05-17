<h1 align="center" style="font-weight: bold;">Java CRUD 💻</h1>

<p align="center">
 <a href="#tech">Technologies</a> • 
 <a href="#started">Getting Started</a> • 
  <a href="#routes">API Endpoints</a> •
 <a href="#colab">Collaborators</a> •
 <a href="#contribute">Contribute</a>
</p>

<p align="center">
    <b>A simple CRUD in Java 17 with authentication.</b>
</p>

<h2 id="tech">💻 Technologies</h2>

- Java 17
- Spring Boot
  - H2 Database
  - Spring Security
  - Lombok
  - Spring Web
  - Spring Boot DevTools
  - Spring Data JPA
  - Jakarta
- JWT (Token)

<h2 id="started">🚀 Getting started</h2>

<h3>Prerequisites</h3>

- [Java 17](https://www.oracle.com/java/technologies/javase-jdk17-downloads.html)
- [Maven](https://maven.apache.org/)
- [Git](https://git-scm.com/)

<h3>Cloning</h3>

```bash
git clone https://github.com/matheusarjc/auth_CRUD.git
```

<h3>Config .env variables</h2>

Use the `.env.example` as reference to create your configuration file `.env` with your Credentials

```yaml
SPRING_DATASOURCE_URL=jdbc:h2:mem:testdb
SPRING_DATASOURCE_USERNAME=sa
SPRING_DATASOURCE_PASSWORD=password
JWT_SECRET={YOUR_JWT_SECRET}
```

<h3>Starting</h3>

```bash
cd login-auth
mvn spring-boot:run
```

<h2 id="routes">📍 API Endpoints</h2>

| route                          | description                         |
|--------------------------------|-------------------------------------|
| <kbd>POST /auth/register</kbd> | register an user into the app.      |
| <kbd>POST /auth/login</kbd>    | authenticate user into the api.     |
| <kbd>GET /user</kbd>           | retrieves user info with JWT token. |


<h3 id="post-auth-detail">POST /auth/register</h3>

**REQUEST**
```json
{
  "name" : "Matheus",
  "email": "test@test.com",
  "password": "123456789"
}
```

**RESPONSE**
```json
{
  "name" : "Matheus",
  "token": "OwoMRHsaQwyAgVoc3OXmL1JhMVUYXGGBbCTK0GBgiYitwQwjf0gVoBmkbuyy0pSi"
}
```

<h3 id="post-auth-detail">POST /auth/login</h3>

**REQUEST**
```json
{
  "email": "test@test.com",
  "password": "123456789"
}
```

**RESPONSE**
```json
{
  "name" : "Matheus",
  "token": "OwoMRHsaQwyAgVoc3OXmL1JhMVUYXGGBbCTK0GBgiYitwQwjf0gVoBmkbuyy0pSi"
}
```

<h3>GET /user</h3>

**REQUEST**

```json
{
  Bearer
  "token":"OwoMRHsaQwyAgVoc3OXmL1JhMVUYXGGBbCTK0GBgiYitwQwjf0gVoBmkbuyy0pSi"
}
```

**RESPONSE**
```json
{
  "Success!"
}
```

<h2 id="colab">🤝 Collaborators</h2>


<table>
  <tr>
    <td align="center">
      <a href="#">
        <img src="https://avatars.githubusercontent.com/u/96945958?v=4" width="100px;" alt="Matheus Araujo Profile Picture"/><br>
        <sub>
          <b>Matheus Araujo</b>
        </sub>
      </a>
    </td>
  </tr>
</table>

<h2 id="contribute">📫 Contribute</h2>

Do you wanna contribute with this project? Follow this steps :>)

1. `git clone https://github.com/matheusarjc/auth_CRUD.git`
2. `git checkout -b feature/NAME`
3. Follow commit patterns
4. Open a Pull Request explaining the problem solved or feature made, if exists, append screenshot of visual modifications and wait for the review!

<h3>Documentations that might help</h3>

[📝 How to create a Pull Request](https://www.atlassian.com/br/git/tutorials/making-a-pull-request)

[💾 Commit pattern](https://gist.github.com/joshbuchea/6f47e86d2510bce28f8e7f42ae84c716)