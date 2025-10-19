Para realizar las puebas en el programa, seguir los siguientes pasos
1- realizar 'mvn clean package' en la carpeta servidor springboot en donde se encuentra el archivo Maven
2- En la terminar, escribir mvn spring-boot run para inicializar el servidor
3- En una nueva terminal, inicializar el archivo ControladorSistemas.py para realizar pruebas en la terminal

Ademas, se poseen Screenshots en la carpeta Cliente-Postman para copiar la estructura de peticiones en Postman


Por ultimo, se necesita una Base de datos con las siguientes tablas
CREATE TABLE public.juego (
	id int4 NOT NULL,
	nombre varchar(1000) NULL,
	porcentaje numeric(14, 8) NULL,
	CONSTRAINT pk_juego PRIMARY KEY (id)
);

CREATE TABLE public.persona (
	cedula int4 NOT NULL,
	nombre varchar(1000) NULL,
	apellido varchar(1000) NULL,
	dineroapostado int8 NULL,
	dineroganado int8 NULL,
	CONSTRAINT pk_cedula PRIMARY KEY (cedula)
);

CREATE TABLE public.cuenta_bancaria (
	idbanco int4 NOT NULL,
	denominacion varchar(1000) NULL,
	nrocuenta int8 NULL,
	saldo int8 NULL,
	cuenta_padre bool NULL,
	CONSTRAINT pk_cuenta2 PRIMARY KEY (idbanco)
);
