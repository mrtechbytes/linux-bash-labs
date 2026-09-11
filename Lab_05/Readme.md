# Día 05: Control de acceso a usuarios y permisos

## Escenario/objetivos
Implementar el principio del mínimo privilegio para inspeccionar y modificar los permisos de archivos en Linux para restringir el acceso de miembros de grupos u otros usuarios a archivos con información sensible.

## Comandos ejecutados

### 1. Creación de archivo con información sensible 
echo "DB_PASS=SuperSecret123" > credentials.txt

### 2. Inspección inicial de permisos y metadata
ls -l credentials.txt

### 3. Restringir permisos para el creador del archivo (Lectura y Escritura)
chmod 600 credentials.txt

### 4. Verificar los nuevos permisos (-rw-------)
ls -l credentials.txt

### 5. Crear un respaldo conservando los atributos originales.
cp -p credentials.txt credentials_backup.txt

## Evidencia de salida
![Picture lab] (picture.png)
