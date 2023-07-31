## notas

intalacion de tailwind:

antes de empezar se debe descargar en la pc "node" con el siguiente link:
https://nodejs.org/es

es recomdable descargar la version "LTS" ya que la version "actual" es para mayores cambios avanzados

despues de la descarga en nuestro archivo de visual studio hay que abrir la terminal integrada, se puede buscar en donde dice "view", la importancia de abrir esto es que nos posiciona dentro de nuestro proyecto para poder ejecutar los comandos

el primer comando que hay que usar es "node -v" para confirmar que la version que se esta utilizando es la actual, luego de que confirmen eso sea puede iniciar con la intalacion de tailwin

el comando "cls" sirve para limpiar la terminal

para empezar la instalacion usamos el comando "npm init -y" esto nos descargara un archivo que nos mostrara datos como el nombre del proyecto, la version, la descripcion etc, esto tendra las dependencias de nuestro proyecto

el siguiente comando seria "npm install tailwindcss" que nos descarga una carpeta con el contenido completo de nuestra dependencia del proyecto

despues de esa instalacion se abre una carpeta src, dentro de ella creamos un archivo css que contendra:

@tailwind base;
@tailwind components;
(es recomendable empezar a meter estilos desde aqui)
@tailwind utilities;

el siguiente comando pondremos "npx tailwindcss build ./src/style.css (esto se debe a porque esta en la carpeta src y el archivo se llama asi) -o ./asset/css/styles.css (esto seria porque abriremos un archivo por medio de la terminal en la carpeta css el cual tendra descargado todos los estilos de tailwind ) "

el archivo "styles.css" es el que vincularemos en el html para empezar a usar los estilos de la pagina (para saber si hicieron bien los pasos se daran cuenta que lo que se va metiendo en el html todas las palabras tendran el mismo tamaño asi se les meta las etiqueta h1, h2, h3, button etc, esto se debe a que tailwind nos resetea los estilos predeterminados, dejando decorar nuestra pagina desde 0 )

el proximo comando que vamos a implementar seria "npx tailwindcss init" esto nos abrira una carpeta que nos dejara meter configuraciones, como poner un color, una tipografia entre otras como por ejemplo

/\*_ @type {import('tailwindcss').Config} _/
module.exports = {
content: ["*.{html,js}"],
theme: {
extend: {
colors: {
blue:"#03a7d3",
red:"#ff4646",
graylight:"#999999"
},

      fontFamily:{
        roboto: ["Roboto, sans-serif "]
      },



    },

},
plugins: [],
};
