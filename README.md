# VIM / NEOVIM: The beginner's guide

number + j = salto de línea relativo
### Index

* [Start, save and exit](#sse)
	* [Start Vim / Neovim](#start)
	* [Exit Vim / Neovim](#exit)
* [Modes](#modes)
* [Move in the editor](#moveEditor)
* [Move operators](#moveOperators)

### Start Vim / Neovim<a name="start"></a>

| command | action       |
| :-----: | :----:       |
| `vim`   | Start Vim    |
| `nvim`  | Start Neovim |

### Save Vim / Neovim<a name="save"></a>  
| command | action       |
| :-----: | :----:       |
| `vim`   | Start Vim    |
| `nvim`  | Start Neovim |

### Exit Vim / Neovim<a name="exit"></a>  
| command   | action            |
| :-----:   | :----:            |
| `q`       | quit              |
| `q!`      | quit without save |

### Modes<a name="modes"></a>
| command   | mode    |
| :-----:   | :----:  |
| `esc`     | normal  |
| `i`       | insert  |
| `:`       | command |
| `v`       | visual  |

### Move in the editor<a name="moveEditor"></a> 
| command   | action |
| :-----:   | :----: |
| `h`       |left    |
| `j`       |down    |
| `k`       |up      |
| `l`       |right   |

### Move operators
| command   | action    |
| :-----:   | :----:    |
| `w`       | next word |
| `e`       | end word  |
| `b`       | back      |

### Insert mode<a name="7"></a>
| Comando   | Acción    |
| :-----:   | :----:    |
| `i`       |insert to left|
| `I`       |insert to start of the current line|
| `a`       |insert to right
| `A`       |insert to end of the current line|

### timeline in normal mode
| Comando   | Acción    |
| :-----:   | :----:    |
| `g+d`     |ir a la definición de la variable| d = definition
| `g+f`     |ir a al archivo | d = definition
| `ctrl+o`  |acción anterior| o = older
| `ctrl+i`  |acción posterior |

### delete in normal mode
| Comando   | Acción    |
| :-----:   | :----:    | 
| `x`       |delete char|
| `d+w`     |delete word|
| `u`       |undo|
| `ctrl+r`  |redo|

### delete line in normal mode
| Comando   | Acción    |
| :-----:   | :----:    | 
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

### copy, cut and paste
| command   | action   |
| :-----:   | :---     |  
| `y`       | copy     |
| `yy`      | copy line|
| `x`       | cut      |
| `dd`      | cut line |
| `p`       | paste    |
**IMPORTANT NOTE**
`delete` doesn't exist in Vim, use `cut` action
Al utilizar, por ejemplo, d+d lo eliminado queda el la clipboard y con la letra `p` podemos pegar lo que allí se encuentre guardado en la línea de abajo o `shift+p` para pegar en la línea superior

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


## Autor

- [@isturiz](https://www.github.com/isturiz)

