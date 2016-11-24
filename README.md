# jquery_controllerV2.js
Plugin controlador de CRUDs para jsFramework Versión-2.

<br>

## Ajustes por defecto:
```JavaScript
tipo:'nuevo', //tipo de instancia
action:'insertar', //accion a realizar el botón
tipo_load:1, //tipo de carga puede ser 1(normal) o 2(especificando el form)
objt_f:'', //objeto del formulario
id : '', //id del registro de BD
subida : false, //si sube o no archivos
recarga : true, //si recarga o no la pagina despues de cada accion (sirve para debug)
//------------------------
//ajustes del form/modulo
nom_modulo:'', //el nombre del modulo usado
titulo_label:'', //titulo de la ventana del modal
nom_tabla:'', //nombre de la tabla en la BD
//-----------------------------------------------------------------
```

## CallBacks
```JavaScript
functionAfter:function(data){               
    console.log('Ejecutando luego de Cualquier cosa!!!');                
},           
functionBefore:function(ajustes){ 
    console.log('Ejecutando antes de cualquier cosa!!!');              
}
```

## Ejemplo set del plugin boton:
```JavaScript
$("#selector_boton").jquery_controllerV2({
    tipo:'inserta/edita',
    titulo_label:'Nuevo Contenido'
    nom_modulo:'contenido',
    nom_tabla:'contenido',
    subida:true,
    recarga:true,  		
    functionAfter:function(data){
        console.log('Ejecutando luego de Cualquier cosa!!!');
    },
    functionBefore:function(ajustes){
        console.log('Ejecutando antes de cualquier cosa!!!');
    },
});
```
