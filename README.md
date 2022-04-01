# ScrapyngPruebas 
Antes de poner en marcha el proyecto necesitas hacer los siguiente:
primero en la carpeta "config" se encuentra el archivo bd.py este archivo tiene la coneccion de la base de  datos
puede ver que estan de la siguiente manera

1# -direccion_servidor = '#tu servidor de sql server'
2# -nombre_bd = '#nombre de tu base de datos'
3# -nombre_usuario = 'Usuario de sql server'
4# -password = 'La contraseÑa de tu usuario'


una vez configurdo crea la siguiente tabla 
query: para la tabla de funcionario
CREATE TABLE [dbo].[FuncionarioDemo](
	[Id] [int] NOT NULL,
	[Nombre] [varchar](100) NULL,
	[Apellido] [varchar](100) NULL,
	[Categoria] [varchar](100) NULL,
	[Cargo] [varchar](100) NULL,
	[Area] [varchar](100) NULL,
	[Institución] [varchar](max) NULL,
	[Correo_electrónico] [varchar](max) NULL,
	[Funciones] [ntext] NULL,
	[Decreto] [varchar](max) NULL,
	[Fecha_ingreso] [date] NULL,
	[Teléfono] [varchar](max) NULL,
	[Extension] [varchar](max) NULL,
	[Fecha_de_Salida] [date] NULL,
	[Estado] [varchar](10) NULL
)

query de onapiv1
CREATE TABLE demoOnapy(
    ID int IDENTITY(1,1) PRIMARY KEY not null, 
	[numeroExpediente] [Nvarchar](max),
	value_for_indexing as cast(left(numeroExpediente,896) as varchar(896)) persisted,
UNIQUE CLUSTERED (value_for_indexing),
	[Tipo] [varchar](max) NULL,
	[subTipo] [varchar](max) NULL,
	[Texto] [varchar](max) NULL,
	[Clases] [varchar](max) NULL,
	[aplicadoAProtege] [varchar](max) NULL,
	[Certificado] [varchar](max) NULL,
	[Expedicion]  [datetime2]  NULL,
	[Vencimiento]  [datetime2] NULL,
	[Titular] [varchar](max) NULL,
	[Gestor] [varchar](max) NULL,
	[Domicilio] [varchar](max) NULL,
	[estatus] [varchar](max) NULL,
	[tipoSigno] [varchar](max) NULL,
	[Idf] int NULL,
	[EnTramite] [varchar](max) NULL)
  
  una vez la tabla creada ejecutadas en el la base de datos
  damo el siguiente paso para encender nuestro entorno virtual para probar el codigo en visual studio code o cmd,
  "c:/Desktop/ScrapingBackEnd/virtual/Scripts/activate.bat"
  lo mas importante es esto: virtual/Scripts/activate.bat
  virtual: nombre del entorno virtual
  Scripts: nombre de la carpeta 
  activate.bat: es el actividador del entorno virtual
  
