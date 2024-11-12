
## Carga de terminologías

### Requisitos

- Java instalado.
- HAPI-FHIR Tool instalado.
  

### Instalar Java
1.- Se instala Java
```
sudo apt install openjdk-17-jre-headless  # version 17.0.12+7-1ubuntu2~24.04
```

### Instalar HAPI-FHIR Tool

Para instalar Hapi-Fhir Tool se utiliza la documentación entregada en https://hapifhir.io/hapi-fhir/docs/tools/hapi_fhir_cli.html.

1.- Descargar el archivo comprimido llamado hapi-fhir-[versión]-cli.zip desde https://github.com/hapifhir/hapi-fhir/releases .

2.- Descomprime el archivo descargado, utiliza la terminal, ubicate en el directorio donde se encuntra el archivo e ingresa el siguiente comando, recuerda cambiar la versión a la que estés ocupando.
```
unzip hapi-fhir-7.4.2-cli.zip
```

3.- Ejecuta el archivo hapi-fhir-cli.jar.
```
java hapi-fhir-cli.jar
```

4.- Inicia HAPI-FHIR Tool.
```
 ./hapi-fhir-cli
```

### Carga de terminología

#### Loinc
```
 ./hapi-fhir-cli upload-terminology -d Loinc_2.74.zip -v r4 -t http://localhost:8080/fhir -u http://loinc.org -s 10GB
```

#### Cie-10
```
 ./hapi-fhir-cli upload-terminology -d cie_10_deis.zip -v r4 -t http://localhost:8080/fhir -u http://hl7.org/fhir/sid/icd-10 -s 1GB
```

#### Norma 820


