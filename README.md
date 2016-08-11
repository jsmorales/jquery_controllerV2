# jquery_controllerV2.js
Plugin controlador de CRUDs para jsFramework Versión-2.

<br>

<h3>Ajustes por defecto:</h3>

tipo:'nuevo', //tipo de instancia<br>
action:'insertar', //accion a realizar el botón<br>
tipo_load:1, //tipo de carga puede ser 1(normal) o 2(especificando el form)<br>
objt_f:'', //objeto del formulario<br>
id : '', //id del registro de BD<br>
subida : false, //si sube o no archivos<br>
recarga : true, //si recarga o no la pagina despues de cada accion (sirve para debug)<br>
//------------------------<br>
//ajustes del form/modulo<br>
nom_modulo:'', //el nombre del modulo usado<br>
titulo_label:'', //titulo de la ventana del modal<br>
nom_tabla:'', //nombre de la tabla en la BD<br>
//-----------------------------------------------------------------<br>
//Datos resultado funcion crear<br>
id_resCrear:'', //resultado de la insercion del registro(last_id)<br>
functionResCrear:function(){<br>
    console.log('El ultimo creado fue: '+ajustes.id_resCrear);<br>
    console.log('Ejecutando luego de Insertar!!!');<br>                
},<br>
//----------------------------------------------------------------- <br>           
functionResEliminar:function(){<br>
    //console.log('El eliminar registro: '+ajustes.id_resCrear);<br>
    console.log('Ejecutando luego de Eliminar!!!');<br>                
},<br>
//-----------------------------------------------------------------<br>
functionResCarga:function(){<br>
    //console.log('El eliminar registro: '+ajustes.id_resCrear);<br>
    console.log('Ejecutando luego de Cargar!!!'); <br>               
},<br>
functionResEditar:function(){<br>
    console.log('Se editó registro: '+ajustes.id_resCrear);<br>
    console.log('Ejecutando luego de Editar!!!');<br>                
},<br>
//-----------------------------------------------------------------<br>
//variable que dice si hay que ejecutar una funcion<br>
//esto depende del tipo<br>
ejecutarFunction:false<br>

<br>

Ejemplo set del plugin boton:
<br>
$("#btn_xxx").jquery_controllerV2({<br>
  		tipo:'inserta/edita',<br> 
  		titulo_label:'Nuevo Contenido'<br> 
  		nom_modulo:'contenido',<br>
  		nom_tabla:'contenido',<br>
  		subida:true,<br>
  		recarga:true,<br>
  		ejecutarFunction:true,<br>
  		functionResCrear:function(){<br>
                
                console.log('Ejecutando luego de Insertar!!!');
                console.log('El ultimo insertado fue '+this.id_resCrear);
                
                //------------------------------------------------------------------------------------------------------------
	 	},
	 	functionResEditar:function(){
            console.log('Se editó registro: '+this.id_resCrear);
            console.log('Ejecutando luego de Editar!!!');                
        },
  	});

