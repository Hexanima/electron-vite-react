# Electron Vite React Testing

Creado segun: https://www.electronforge.io

Mas especifico usando el siguiente comando: `npx create-electron-app@latest my-app --template=vite-typescript`

# Modo de ejecucion

## Desarrollo:

`npm start`: Levanta la aplicacion (ejecuta una nueva ventana, se actualiza en tiempo real al guardar cambios al codigo

## Compilar "distribuibles" (archivo.exe y datos necesarios de la aplicacion):

`npm run make`: Compila toda la aplicacion segun las configuraciones de los archivos de forge

Investigar configuraciones aca: https://www.electronforge.io/config/makers

## Publicar aplicacion:

`npm install --save-dev @electron-forge/publisher-github`: UNA SOLA VEZ, es una dependencia necesaria para publicar los ejecutables en GitHub

Investigar configuraciones de publicacion aca: https://www.electronforge.io/config/publishers/github

`npm run publish`: Publica los ejecutables segun la configuracion dada
