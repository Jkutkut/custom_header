# Custom Header

([ENGLISH VERSION](./README.md))

Este proyecto está basado en el repositorio [42 header](https://github.com/42Paris/42header). Por tanto, todo el mérito por el desarrollo de la lógica es de los autores originales.


### **Introducción**

Lógica para tener un encabezado personalizado para el editor de vim.


		/* ************************************************************************** */
		/*                                                                            */
		/*                           .                      .                         */
		/*        .    __ _o|                        .                                */
		/*            |  /__|===--        .                                           */
		/*     *      [__|______~~--._                      .                         */
		/*      .    |\  `---.__:====]-----...,,_____                *                */
		/*           |[>-----|_______<----------_____;::===--         .==.            */
		/*           |/_____.....-----'''~~~~~~~                     ()''()-.         */
		/*      +               ·                         .---.       ;--; /          */
		/*                                              .'_:___". _..'.  __'.         */
		/*   aa.c                                        |__ --==|'-''' '...;         */
		/*                                              [  ]  :[|       |---\         */
		/*   By: jre-gonz <jre-gonz@student.42madr      |__| I=[|     .'    '.        */
		/*                                              / / ____|     :       '._     */
		/*   Created: 2022/02/24 15:41:54 by jre-g     |-/.____.'      | :       :    */
		/*   Updated: 2022/02/24 15:42:41 by jre-gon    /___ /___      '-'._----'     */
		/*                                                                            */
		/* ************************************************************************** */


### **Configuración UNIX**

Copia `customheader.vim` dentro de `~/.vim/plugin` o usa tu gestor de plugins favorito. Después, configura el usuario y el correo como se muestra a continuación.

#### Opción 1: exportar USER y MAIL en tu archivo de configuración de shell

Añade en `~/.zshrc` tus datos en las variables:

+ `USER`
+ `MAIL`

#### Opción 2: configurar los valores de usuario y correo directamente en tu archivo de configuración de vim

```vim
let g:user42 = 'yourLogin'
let g:mail42 = 'yourLogin@student.42.fr'
```

### **Uso**

En el modo **NORMAL** puedes usar `:Customheader` o simplemente pulsa la tecla <kbd>F2</kbd> (o la tecla/comando que quieras si quieres cambiarlo).

<br>

## **Modificar encabezado**

### **Cambiar tecla de activación**:
Abre el archivo `~/.vim/plugin/customheader.vim` y cambia la siguiente línea (ubicada al final):

	map <F2> :Customheader<CR>

Modifica la tecla que quieres usar (por defecto, <kbd>F2</kbd>).

### **Cambiar comando**:
Abre el archivo `~/.vim/plugin/customheader.vim` y cambia la siguiente línea (ubicada al final):

	command! Customheader call s:customheader ()

Modifica el comando que quieres usar (por defecto, `:Customheader`).

Recuerda cambiar también la siguiente línea con el nuevo comando:

	map <F2> :Customheader<CR>


### **Cambiar encabezado**:
Abre el archivo `~/.vim/plugin/customheader.vim` y cambia la siguiente línea (ubicada al comienzo):

	let s:asciiart = [
		\'         .----.        ',
		\'         |[XX]|        ',
		\' _.==.___/    \_______ ',
		\'| __ ____.-""-. ______|',
		\'|[__]   /."""".\ _    |',
		\'|      // /""\ \\_)   |',
		\'|      \\ \__/ //     |',
		\'|       \\.__.//      |',
		\'|        "-..-"       |',
		\" `-------------------' "
		\]

Cambialo por lo que quieras. Ten en cuenta que el uso de caracteres especiales puede no funcionar de manera directa.

Recuerda que el logo tiene que ser lo suficientemente alto para que el título, creador y última modificación se vean bien.

### **Ejemplos**:
Siéntete libre de usar y crear tus propios encabezados (con un pull request) :D

- 42:

		let s:asciiart = [
			\"        :::      ::::::::",
			\"      :+:      :+:    :+:",
			\"    +:+ +:+         +:+  ",
			\"  +#+  +:+       +#+     ",
			\"+#+#+#+#+#+   +#+        ",
			\"     #+#    #+#          ",
			\"    ###   ########.fr    "
			\]
<br>

		/* ************************************************************************** */
		/*                                                                            */
		/*                                                        :::      ::::::::   */
		/*   42.c                                               :+:      :+:    :+:   */
		/*                                                    +:+ +:+         +:+     */
		/*   By: jre-gonz <jre-gonz@student.42madrid.com>   +#+  +:+       +#+        */
		/*                                                +#+#+#+#+#+   +#+           */
		/*   Created: 2022/02/24 10:00:40 by jre-gonz          #+#    #+#             */
		/*   Updated: 2022/02/24 10:00:44 by jre-gonz         ###   ########.fr       */
		/*                                                                            */
		/* ************************************************************************** */

- Star wars:

		let s:asciiart = [
			\'                        .                      .                   ·  ',
			\'     .    __ _o|                        .                ·            ',
			\'         |  /__|===--        .                                  ·     ',
			\'  *      [__|______~~--._                      .                      ',
			\'   .    |\  `---.__:====]-----...,,_____                *          ·  ',
			\'        |[>-----|_______<----------_____;::===--             .==.     ',
			\"        |/_____.....-----'''~~~~~~~                         ()''()-.  ",
			\'   +               ·                           .---.         ;--; /   ',
			                                           \"  .'_:___\". _..'.  __'.    ",
			                                           \"  |__ --==|'-''' \'...;    ",
			                                           \'  [  ]  :[|       |---\    ',
			                                           \"  |__| I=[|     .'    '.   ",
			                                           \"  / / ____|     :       '._",
			                                           \" |-/.____.'      | :      :",
			                                           \"/___\ /___\      '-'._----'"
			\]
<br>

		/* ************************************************************************** */
		/*                                                                            */
		/*                           .                      .                         */
		/*        .    __ _o|                        .                                */
		/*            |  /__|===--        .                                           */
		/*     *      [__|______~~--._                      .                         */
		/*      .    |\  `---.__:====]-----...,,_____                *                */
		/*           |[>-----|_______<----------_____;::===--         .==.            */
		/*           |/_____.....-----'''~~~~~~~                     ()''()-.         */
		/*      +               ·                         .---.       ;--; /          */
		/*                                              .'_:___". _..'.  __'.         */
		/*   aa.c                                        |__ --==|'-''' '...;         */
		/*                                              [  ]  :[|       |---\         */
		/*   By: jre-gonz <jre-gonz@student.42madr      |__| I=[|     .'    '.        */
		/*                                              / / ____|     :       '._     */
		/*   Created: 2022/02/24 15:41:54 by jre-g     |-/.____.'      | :       :    */
		/*   Updated: 2022/02/24 15:42:41 by jre-gon    /___ /___      '-'._----'     */
		/*                                                                            */
		/* ************************************************************************** */

- Camera:

		let s:asciiart = [
			\'         .----.        ',
			\'         |[XX]|        ',
			\' _.==.___/    \_______ ',
			\'| __ ____.-""-. ______|',
			\'|[__]   /."""".\ _    |',
			\'|      // /""\ \\_)   |',
			\'|      \\ \__/ //     |',
			\'|       \\.__.//      |',
			\'|        "-..-"       |',
			\" `-------------------' "
			\]
<br>

		/* ************************************************************************** */
		/*                                                                            */
		/*                                                           .----.           */
		/*                                                           |[XX]|           */
		/*                                                   _.==.___/    \_______    */
		/*                                                  | __ ____.-""-. ______|   */
		/*   42.c                                           |[__]   /."""".\ _    |   */
		/*                                                  |      // /""\ \\_)   |   */
		/*   By: jre-gonz <jre-gonz@student.42madrid.com>   |      \\ \__/ //     |   */
		/*                                                  |       \\.__.//      |   */
		/*   Created: 2022/02/24 09:30:52 by jre-gonz       |        "-..-"       |   */
		/*   Updated: 2022/02/24 09:55:25 by jre-gonz        `-------------------'    */
		/*                                                                            */
		/* ************************************************************************** */

- Dobby:

		let s:asciiart = [
			\'   _____       ',
			\'  /     \      ',
			\'/- (*) |*)\    ',
			\'|/\.  _>/\|    ',
			\'    \__/    |\ ',
			\'   _| |_   \-/ ',
			\'  /|\__|\  //  ',
			\' |/|   |\\//   ',
			\" |||   | ~'    ",
			\' ||| __|       ',
			\' /_\| ||       ',
			\' \_/| ||       ',
			\'   |7 |7       ',
			\'   || ||       ',
			\'   || ||       ',
			\'   /\ \ \      ',
			\'  ^^^^ ^^^     '
			\]
<br>

	/* ************************************************************************** */
	/*                                                                            */
	/*                                                             _____          */
	/*                                                            /     \         */
	/*                                                          /- (*) |*)\       */
	/*                                                          |/\.  _>/\|       */
	/*                                                              \__/    |\    */
	/*                                                             _| |_   \-/    */
	/*                                                            /|\__|\  //     */
	/*                                                           |/|   |\\//      */
	/*                                                           |||   | ~'       */
	/*                                                           ||| __|          */
	/*                                                           /_\| ||          */
	/*   aa.c                                                    \_/| ||          */
	/*                                                             |7 |7          */
	/*   By: jre-gonz <jre-gonz@student.42madrid.com>              || ||          */
	/*                                                             || ||          */
	/*   Created: 2022/02/24 15:18:32 by jre-gonz                  /\ \ \         */
	/*   Updated: 2022/02/24 15:18:34 by jre-gonz                 ^^^^ ^^^        */
	/*                                                                            */
	/* ************************************************************************** */

### **Notas**

- Puedes crear el logo lo ancho que quieras (con el límite de los 80 caracteres).

- Puedes usar todo el espacio que quieras, pero recuerda que puede sobreponerse a las líneas de autor, título, etc.

- Dentro de los **42 clusters** puedes usar:

		./set_header.sh


### **Créditos a los creadores originales**

[@zazard](https://github.com/zazard) - creator  
[@alexandregv](https://github.com/alexandregv) - contributor  
[@mjacq42](https://github.com/mjacq42) - contributor  
[@sungmcho](https://github.com/lordtomi0325) - contributor  
