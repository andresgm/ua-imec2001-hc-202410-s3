<img src='./utils/uniandes_abet.png' width='850'/>

# IMEC 2001 - Herramientas Computacionales 
Ciclo de Talleres <br>
Curso Electivo – Sección 3 <br>
2024-10 – Ciclo 2 <br>

*La parábola de las piedritas.* <br>

*Un hombre que caminaba por el desierto escuchó una voz que le dijo: "Toma algunas piedritas del suelo y ponlas en tu bolsillo, y mañana estarás feliz y triste al mismo tiempo."
El hombre hizo caso. Tomó algunas piedritas del suelo y las guardó en su bolsillo. Al día siguiente, el hombre buscó en su bolsillo y encontró diamantes, rubíes y esmeraldas. Y el hombre estaba feliz y triste al mismo tiempo. Feliz de haber tomado algunas piedritas - triste de no haber tomado más.* <br>

*Lo mismo pasa con la educación*  <br>

## Instalación

#### Repositorio

Primero es necesario descargar los archivos de los protocolos y los aplicativos para la creación de los archivos de configuración y para correr los modelos. Los archivos se encuentran alojados en el repositorio del Consejo Nacional de Operación en [cno/cno_solar](https://git.cno.org.co/cno/cno_solar). Para [clonar](https://docs.github.com/es/repositories/creating-and-managing-repositories/cloning-a-repository) el repositorio `cnosolar` se recomienda usar el software [GitHub Desktop](https://desktop.github.com/). 

Una vez haya descargado e instalado *Github Desktop*, seleccione *File* y *Clone Repository...*. En la pestaña *URL*, en el campo *URL or username/repository* escriba la dirección `https://git.cno.org.co/cno/cno_solar.git`. Seleccione la ubicación donde quiere descargar los archivos y seleccione *Clone*. 

#### Distribución y Ambiente

Se recomienda instalar [Miniforge](https://github.com/conda-forge/miniforge) como ambiente para instalar Python y las librerías necesarias para la ejecución de los protocolos. Miniforge es una distribución de Python y el administrador de paquetes `conda`, permite fácilmente la configuración de ambientes y la instalación de paquetes desde el repositorio `conda-forge`.

Durante la instalación utilice las opciones recomendadas en las `Advanced Installation Options` como se muestra a continuación.

![conda-forge/miniforge](images/conda-forge.png)

Luego de descargar e instalar `Miniforge`, inicie el terminal mediante la aplicación `Miniforge Prompt`. Si la instalación se realizó de manera correcta, debe estar en el ambiente `(base)` como se muestra a continuación. 

![base-env](images/base-env.png)

Se creará un ambiente específico para correr los protocolos, el cual llamaremos `cno-solar`, y se instalarán los paquetes necesarios. Con este fin abra un terminal con la aplicación `Miniforge Prompt` y desde el ambiente `(base)` **muévase al directorio donde tiene descargado los archivos del protocolo**, por ejemplo, si los tiene descargados en el escritorio:

```terminal
cd C:\usuario\Desktop\cno_solar
```

Luego cree el ambiente con el comando:

```terminal
conda env create --file environment.yml
```
Ahora, se activa dicho ambiente:

```terminal
conda activate cno-solar
```

Después de ejecutar el comando anterior, se debe estar en el ambiente correspondiente, en este caso denotado por `(cno-solar)` como se muestra en la siguiente figura.

![cno-solar-env](images/cno-solar-env.png)

Ahora se instala el kernel correspondiente al ambiente recien creado.

```terminal
python -m ipykernel install --user --name cno-solar --display-name "cno-solar"
```

Finalmente, ejecute el siguiente comando para iniciar los cuadernos. 

```terminal
jupyter notebook
```

Si desea eliminar el ambiente creado, ejecute el siguiente comando:

```terminal
conda env remove -n cno-solar
```

Luego, para eliminar el kernel `cno-solar` creado, ejecute el siguiente comando:

```terminal
jupyter kernelspec remove cno-solar
```
