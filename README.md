

<div align="center">
<img src="logo.png" height="90px" width="auto" /> 
<h2>
    <em>Résumé</em> minimalista maquetado para web y pdf
</h2>
<p>
Esquema del JSON de CV de <a href="https://jsonresume.org/schema/">jsonresume.org</a>
</p>


<p>
Basado en el diseño de <a href="https://github.com/BartoszJarocki/cv">Bartosz Jarocki</a>

</p>

</div>

<div align="center">
    <a href="#🚀-empezar">
        Empezar
    </a>
    <span>&nbsp;✦&nbsp;</span>
    <a href="#🧞-comandos">
        Comandos
    </a>
    <span>&nbsp;✦&nbsp;</span>
    <a href="#🔑-licencia">
        Licencia
    </a>
    <span>&nbsp;✦&nbsp;</span>
    <a href="https://midu.dev">
        Personal
    </a>
   
</div>

<p></p>

<div align="center">

![Astro Badge](https://img.shields.io/badge/Astro-BC52EE?logo=astro&logoColor=fff&style=flat)
![GitHub stars](https://img.shields.io/github/stars/midudev/minimalist-portfolio-json)
![GitHub issues](https://img.shields.io/github/issues/midudev/minimalist-portfolio-json)
![GitHub forks](https://img.shields.io/github/forks/midudev/minimalist-portfolio-json)
![GitHub PRs](https://img.shields.io/github/issues-pr/midudev/minimalist-portfolio-json)

</div>

<img src="portada.png"></img>

## 🛠️ Stack

- [**Astro**](https://astro.build/) - El framework web de la nueva época.
- [**Typescript**](https://www.typescriptlang.org/) - JavaScript con sintaxis de tipado.
- [**Ninja Keys**](https://github.com/ssleptsov/ninja-keys) - Menu desplegable con atajos de teclado hecho en puro Javascript.


## 🚀 Empezar

### 1. Usa este [repo](https://github.com/midudev/minimalist-portfolio-json) como _template_ de un proyecto de Astro


- Yo uso [pnpm](https://pnpm.io/installation) como gestor de dependencias y empaquetador.

```bash
# Activa pnpm en MacOS, WSL & Linux:
corepack enable
corepack prepare pnpm@latest --activate

# Inicializa el proyecto
pnpm create astro@latest -- --template midudev/minimalist-portfolio-json
```

### 2. Añade tu contenido:
Edita el archivo `cv.json` para crear tu propio Portafolio/CV imprimible.
### 3. Lanza el servidor de desarrollo:

```bash
# Disfruta del resultado
pnpm dev
```


1. Abre [**http://localhost:4321**](http://localhost:4321/) en tu navegador para ver el resultado 🚀


## 🧞 Comandos

|     | Comando          | Acción                                        |
| :-- | :--------------- | :-------------------------------------------- |
| ⚙️  | `dev` o `start` | Lanza un servidor de desarrollo local en  `localhost:4321`.  |
| ⚙️  | `npm run build`          | Comprueba posibles errores y hace un empaquetado de producción en `./dist/`.      |
| ⚙️  | `preview`        | Vista previa en local `localhost:4321` |
| ⚙️  | `npm run deploy`        | Vista previa en local `localhost:4321` |



## 🔑 Licencia

[MIT](LICENSE.txt) - Creado por [**midudev**](https://midu.dev).


#######################################################################################################################################

1. Cambios dentro de cv.json

- Realizamos los cambios pertinentes
- Podemos ver el status con git status
- Añadimos los cambios, empaquetamos con git add .
                                         git add cv.json Hero.astro 
- Podemos hacer un commit con git commit -m "Descripción del cambio"
- Lo subimos con git push

2. Iniciar servidor para ver cambios en directo

- Iniciar npm start
- Seguimos con npm run deploy

3. Realizar cambios desde el navegador

- Abrimos el navegador y vamos a la url http://localhost:4321/portfolio-celine-jin
- F12 o ajustes > más herramientas > herramientas para desarrolladores
- Ventanita con flechita lateral izquierdo, cambiar según se mire y copiar los códigos al .astro indicado


Extras:

* Si quiero añadir párrafos, hay dos maneras para hacerlo:
- Puedo hacerlo directamente en el archivo .astro. En este caso en About.astro.
- Opción 1: insertar un if en el que recorra una lista y si se encuentra con (ejemplo: \n) haga un salto de párrafo, es decir un <br>

<Section title="Sobre mí">
  {
    summary.map( parrafo => {
      
      if (parrafo == "\n") {
      return (<br/>)

    } else {
      return (<p>{parrafo}</p>)

    }})
  }
  
</Section>

En el .json debería aparecer algo así:
"summary": ["Revelo los secretos de la vida a través de la bioinformática.", "\n",
            "Licenciada en Biología...", "\n",
            "Mi experiencia...", "\n",
            "Con fluidez en chino..."],
    


- Opción 2: configurar el espacio de los márgenes según guste

<style>
  p {
  margin-top: 20px;
  }

</style>







