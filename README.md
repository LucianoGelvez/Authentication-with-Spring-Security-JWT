# Spring-Security-JWT
JSON Web Token (JWT) es una norma estándar de la industria para crear tokens de acceso que permiten el acceso seguro a recursos específicos en una aplicación. En Spring Boot, la autenticación y autorización de JWT se pueden lograr con Spring Security.

## Cómo funciona generalmente:

Verificación de usuarios y Generación de Tokens: Cuando un usuario se autentica con éxito (por ejemplo, utilizando su nombre de usuario y contraseña), el servidor puede generar un JWT que incluye detalles del usuario y una firma digital. Este token se envía de vuelta al cliente.

Token en las solicitudes subsiguientes: Cuando el cliente necesita acceder a un recurso protegido, incluye el token JWT en la cabecera de la solicitud. Típicamente se coloca en el campo "Authorization" con el prefijo "Bearer".

Verificación de token: Cuando el servidor recibe la solicitud con un JWT, la decodifica, verifica la firma digital y valida la reclamación del usuario que se encuentra dentro del token.

Acceso concedido o denegado: Si el token es válido, el acceso a los recursos se concede según los detalles del usuario en el token. Si no es válido, el acceso se deniega.

Para usar JWT con Spring Boot y Spring Security, necesitarás dependencias como "spring-boot-starter-security" y "spring-security-jwt". Spring Security proporciona clases para la generación de tokens, como "Jwts", y para la configuración de la seguridad del JWT, como "JwtTokenStore", "TokenEnhancerChain", y "JwtAccessTokenConverter".

Las personalizaciones adicionales, como configurar los detalles de expiración del token y usar roles en JWT para la autorización basada en roles, también son posibles.

![Untitled](https://github.com/LucianoGelvez/Authentication-with-Spring-Security-JWT/assets/111015329/ba68fd73-2db0-46b5-b4d7-427ec71b20cd)
