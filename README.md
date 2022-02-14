## Reparar VS Code Menu Opciones Windows10

### Problema
Al instalar VS Code y reiniciar, no Aparece la Opcion de VS Code en el menu de Windows.
![Sin título-1](https://user-images.githubusercontent.com/16279201/153812225-c26d3296-c39e-42c3-8d2c-4d0f43ab6c2c.png)


## Solución
Copiamos en un archivo con extención archivo.reg 
### Copiamos el siguiente código en un editor de texto
```cmd
Windows Registry Editor Version 5.00
	
	[HKEY_CLASSES_ROOT\*\shell\VSCode]
	@="Abrir con Visual Studio Code"
	"Icon"=" PEGAR_AQUI "
	
	[HKEY_CLASSES_ROOT\*\shell\VSCode\command]
	@="\" PEGAR_AQUI \" \"%1\""
	
	Windows Registry Editor Version 5.00
	
	[HKEY_CLASSES_ROOT\Directory\shell\VSCode]
	@="Abrir con Visual Studio Code"
	"Icon"=" PEGAR_AQUI "
	
	[HKEY_CLASSES_ROOT\Directory\shell\VSCode\command]
	@="\" PEGAR_AQUI \" \"%V\""
	
	Windows Registry Editor Version 5.00
	
	[HKEY_CLASSES_ROOT\Directory\Background\shell\VSCode]
	@="Abrir con Visual Studio Code"
	"Icon"=" PEGAR_AQUI "
	
	[HKEY_CLASSES_ROOT\Directory\Background\shell\VSCode\command]
	@="\" PEGAR_AQUI \" \"%V\"" 
```

#### Debe Quedar asi

![Captura4](https://user-images.githubusercontent.com/16279201/153817827-5d975e69-fe46-4b4c-a374-eb3eb3fcbac4.PNG)

### Carpeta de Archivo de Origen
Nos vamos a la carpeta donde esta instalado el VS Code, en mi caso es C:\Users\Aldo\AppData\Local\Programs\Microsoft VS Code

### Copiar la ruta de acceso
Con Shif y clic derecho copiamos como ruta de Acceso <br>
![Captura2](https://user-images.githubusercontent.com/16279201/153815533-3ea9118f-b35d-4028-8d98-0db423b4112f.PNG)

### Realizamos el Escape de Cadena
Realizamos los Siguientes Pasos:
- <a href="https://onlinestringtools.com/escape-string" target="_blank">Ingresar Aqui</a>
- Pegamos 
- Quitamos las Comillas
- Copiamos el resultado <br>

![Captura6](https://user-images.githubusercontent.com/16279201/153818836-ecf33b08-7c8b-4824-af14-3ec04acb447a.PNG)

 Pegamos en donde Dice PEGAR_AQUI con todo y espacios dentro de las comillas "" <br>
![Captura5](https://user-images.githubusercontent.com/16279201/153817922-e80eb374-6e09-4491-bab8-a52aa0df9287.PNG)

Debe quedar de esta manera, guardar y Cerrar!  <br>
![Captura7](https://user-images.githubusercontent.com/16279201/153819329-02d7209e-3467-4303-a438-9f2a3541ce56.PNG)

Agregamos las Claves de REgistros haciendo doble clic <br>

![Captura8](https://user-images.githubusercontent.com/16279201/153819777-5af282c7-dd44-49ce-b96e-4bd297f17733.PNG)

Aceptar  <br>

![Captura9](https://user-images.githubusercontent.com/16279201/153820215-7710620e-bc9a-4b0c-9c96-e0581ad01c00.PNG)
![Captura99](https://user-images.githubusercontent.com/16279201/153820264-c3554e81-e537-46cc-83ae-2622bd881fb3.PNG)

## Finalizado, espero que te haya servido
