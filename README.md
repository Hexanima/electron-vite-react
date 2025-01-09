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

### Ejemplo de configuracion

En el archivo `forge.config.js` Y usando la dependencia `@electron-forge/publisher-github` (Para publicar en github):

```
module.exports = {
  // ...
  publishers: [
    {
      name: '@electron-forge/publisher-github',
      config: {
        repository: {
          owner: 'me',
          name: 'awesome-thing'
        },
        prerelease: true
      }
    }
  ]
};
```

### Extras

Documentacion sobre las configuraciones de `electron-forge` (archivo `forge.config.js`) aca:

https://www.electronforge.io/config/configuration
