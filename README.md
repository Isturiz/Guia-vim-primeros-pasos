
# Guía vim / nvim primeros pasos


## Índice

##### 1. [Iniciar vim desde la terminal](#1)
##### 2. [Salir de Vim / Neovim](#2)
##### 3. [Moverse en el editor](#3)

**modes: normal, insert.**
### Modes
1. Normal mode
2. Insert mode
3. Command mode
4. Visual mode

### Iniciar vim desde la terminal<a name="1"></a>  

Vim: `vim`

Neovim: `nvim`

### Salir de Vim / Neovim<a name="2"></a>  

| Comando   | Acción |
| :-----:   | :---- | 
| `q`       | salir  | 
| `q!`      | salir sin guardar |

### Moverse en el editor<a name="3"></a> 

| Comando   | Acción    |
| :-----:   | :----    | 
| `h`       |izquierda  |
| `j`       |abajo      |
| `k`       |arriba     |
| `l`       |derecha    |
| `w`       |next word  |
| `e`       |end word  |
| `b`       |back word  |

### Editar<a name="4"></a> 

| Comando   | Acción    |
| :-----:   | :----     | 
| `esc`     |exit mode|


### Insert mode<a name="7"></a> 
| Comando   | Acción    |
| :-----:   | :----     | 
| `i`       |insert to left|
| `I`       |insert to start of the current line|
| `a`       |insert to right
| `A`       |insert to end of the current line|
|
### timeline in normal mode
| Comando   | Acción    |
| :-----:   | :----     | 
| `g+d`       |ir a la definición de la variable| d = definition
| `g+f`       |ir a al archivo | d = definition
| `ctrl+o`       |acción anterior| o = older
| `ctrl+i`       |acción posterior |

### delete in normal mode
| Comando   | Acción    |
| :-----:   | :----     | 
| `x`       |delete char|
| `d+w`     |delete word|
| `u`       |undo|
| `ctrl+r`  |redo|

### delete line in normal mode
| Comando   | Acción    |
| :-----:   | :----     | 
| `d+d`     |elimina la línea|
| `d+0`     |elimina todo lo de la izquierda|
| `shift+d`     |elimina todo lo de la derecha|
| `d+shift+4`  |eliminar desde el cursor hasta el final de la línea (no elimina la línea)|
shift+d y d+shift+4 son iguales

también se pueden combinar con los operadores de movimiento
| Comando   | Acción    |
| :-----:   | :----     | 
| `d+w`     |elimina |
| `d+e`     |elimina |
| `d+b`     |elimina |

| `number + d + operador de movimineto`     |elimina la cantidad de palabras especificadas en el number |

esto es un test
### copy, cut and paste
| command   | action   |
| :-----:   | :---     |  
| `y`       | copy     |
| `yy`      | copy line|
| `x`       | cut      |
| `dd`      | cut line |
| `p`       | paste    |
Los operadores de movimiento son 
-w
-e
-b

Al utilizar, por ejemplo, d+d lo eliminado queda el la clipboard y con la letra `p` podemos pegar lo que allí se encuentre guardado en la línea de abajo o `shift+p` para pegar en la línea superior

**NOTA SUPER IMPORTANTE:**
En vim no existe el concepto de 'eliminar', todo lo que sea similar es simplemente la acción de 'cortar'

`r` char replace
`shift + r` reemplazar varios
`c+w` change word desde donde está el puntero
`c + i + w` cambia la palabra completa


`g+g` va al inicio del archivo
`shift + g` va al final
`number + shift + g` va a la línea especificada 

`/ + texto` busca hacia adelante
`? + texto` busca hacia atrás
**nota:** solo en vim, en neovim ambas funcionan igual y buscan todas las coincidencias
luego de presionar `enter` para encontrar concurrencias podemos utilizar la letra `n` para ir a la siguiente concurrencia o `shift + n` para la concurrencia anterior

`%` para ir al parentesis par


#### Comand mode

:s/texto a reemplazar/texto nuevo /g -> en caso de querer reemplazar todas las concurrencias de la línea.

:%s/texto a reemplazar/texto nuevo -> reemplaza todas las concurrencias de lal archivo

`o` añade una nueva línea abajo
`shift + o` añade línea arriba


`v` para abrir el modo visual
`y` para copiar
`p` para pegar
## Autor

- [@isturiz](https://www.github.com/isturiz)

