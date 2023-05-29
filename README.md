 Pagina web de la asignatura de Lenguaje de Marcas (M4UF1)

## **_XML_**

 
  En **_XML_** es necesario comenzar agregando ```\<?xml version="1.0" encoding="UTF-8" ?>```, esto es una cabecera. 
  
  Gracias a esta etiqueta el lenguaje puede funcionar correctamente. 
  
  En todo archivo **XML** es necesario que haya una etiquieta raiz.
  
  Existen varios tipos de etiquetas:
  
  * Pares
  * Impares 
  * Booleanas
   
  **PARES:** Estas etiquetas son las que tienen una etiqueta para abrir y otra para cerrar. _EJEMPLO:_```<name>Eustaquio\</name>```
  
  **IMPARES:** Estas etiquetas solo necesitan una etiqueta que cierre. _EJEMPLO:_ ```<age years="197" />```
  
  **BOOLEANAS:** Con esta etiqueta puedes determinar el estado de una variable por defecto, si es true o false. _EJEMPLO:_ ```<tienelaeso />``` 
  
  Para que todos los archivos xml sigan una estructura concreta es necesario que haya un archivo que determine dicha estructura. 
  El lenguaje de estas estructuras pueden ser **DTD** o **XSD**.
  
  Codigo basico de **XML**:
```
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE character SYSTEM "character.dtd">
<character id_character="1">
	<name>Eustaquio</name>
	<surname>Mendoza</surname>
	<age years="197" />
	<race>Enano</race>
	<class>Artificiero</class>
	<gender abbrev="N">Non-Binary</gender>
	<height cm="130" />
	<weight kg="80" />
	<language abbrev="prt" prefix="+32">Portugues</language>
	<tienelaeso />
	<weapons>
		<weapon id_weapon="1"/>
		<weapon id_weapon="3"/>
		<weapon id_weapon="4"/>
		<weapon id_weapon="7"/>
	</weapons>
		
</character>
  ```

### **_HISTORIA XML_**


Lenguaje base de lenguajes de marcas. Viene de un lenguaje de los años 70 que se llama SGML. Utilizaba etiquetas como la  <i> <b> y demás. Word es un texto binario con texto enriquecido.
Los lenguajes de marcas tienen como objetivo remarcar palabras. En los años 70 no había gráfica, por lo que se usaba este lenguaje de marcas para printar este tipo de texto. Lo que hacía era colocar estas etiquetas <B> etc para que la impresora parseara estas etiquetas e imprimiera las palabras como se quería.  
En los 80 con las gráficas era posible usar interfaces gráficas. HTTP  (Hyper Text Transfer Protocol) este protocolo conseguía transformar el texto en tres dimensiones en vez de dos. La tercera dimensión son los enlaces, gracias a esto existe la capacidad de poner enlaces en las palabras.
En los 90 SGML se transformó en HTML. Gracias a esto se consiguió enlazar páginas web que estén en servidores HTTP. El primer browser se llamó Mosaic creado por el mismo que creó HTML. Apareció una empresa llamada NetScape que creó un navegador gratuito que interpretaba lenguaje HTML. IRC es un protocolo de chat que usa twitch. Microsoft compró internet explorer.
La expresión de navegar viene de netScape y Microsoft intentó implementar el término surfear. Microsoft intentó imponer Internet Explorer haciendo que sea del propio núcleo y haciendo que el explorador de archivos se vea como una web de internet explorer. Internet Explorer aplicaba mal el lenguaje HTML y como era el navegador predominante todo el mundo programaba páginas webs de la forma que lo interpretaba Internet Explorer.
Esto consiguió acabar con todos los navegadores. W3C era el consorcio de navegadores. Al morir netscape liberó el código fuente con el nombre del proyecto mozilla. El consorcio quería delimitar los estándares en las estructuras de las páginas web con html. 

Después de html4 se creó XTML, se hizo para determinar cómo eran las etiquetas y para determinar las normas. Con XTML se podrían crear otros lenguajes de marcas, no impone visualización, lo que impone es una estructura.  

En los años 99 al 2008 estaba XHTML e hicieron que todo pasará por las normas de XTML.

Gracias a la estructura impuesta comenzaron a demandar a Microsoft ya que no seguía ninguna estructura acordada. Así que Microsoft comenzó a decir que lo intentaría.

## **_DTD_**
Los _apuntes_ de **DTD**

```dtd
<!ELEMNT character (name, surname, age, race, 
 class,gender, height,
 weight, language, tienelaeso?, weapons?)>
<!ELEMENT name (#PCDATA)>
<!ELEMENT surname (#PCDATA)>
<!ELEMENT age EMPTY>
<!ELEMENT race (#PCDATA)>
<!ELEMENT class (#PCDATA)>
<!ELEMENT gender (#PCDATA)>
<!ELEMENT height EMPTY>
<!ELEMENT weight EMPTY>
<!ELEMENT language (#PCDATA)>
<!ELEMENT tienelaeso EMPTY>
<!ELEMNT weapons (weapon*)>
<!ELEMENT weapon EMPTY>

<!ATTLIST age years CDATA #REQUIRED>
<!ATTLIST gender abbrev CDATA #REQUIRED>
<!ATTLIST height cm CDATA #REQUIRED>
<!ATTLIST weight kg CDATA #REQUIRED>
<!ATTLIST language abbrev CDATA #REQUIRED>
<!ATTLIST language prefix CDATA>
<!ATTLIST id_weapon CDATA #REQUIRED>

```
Gracias a esto tenemos un estandar para los archivos de characters en **XML**. 

Los archivos dtd son principalmente las estructuras de archivos **XML**, como la cantidad de veces qeu se repite una cosa o su contenido mismo. 
Gracias a estas estructuras podemos comprobar si un archivo que nos han mandado sigue la estructura predefinida del resto de archivis **XML**. 
