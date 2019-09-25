## Manual de uso ordendecompra.cl

<div style="background-color: white; padding: 12px;"> 
  <h3>Bienvenido a OC! Órdenes de Compra On-Line<h3> 
  <h4>Contenidos:</h4> 
  <ul>
    <li><a @click="${()=> this.scrollTo('s1')}">Primeros Pasos</a></li>
    <li><a @click="${()=> this.scrollTo('s2')}">Órdenes de Compra</a></li>
    <li><a @click="${()=> this.scrollTo('s27')}">Flujograma Órdenes de Compra</a></li>
    <li><a @click="${()=> this.scrollTo('s3')}">Centros de Costo</a></li>
    <li><a @click="${()=> this.scrollTo('s4')}">Proveedores</a></li>
    <li><a @click="${()=> this.scrollTo('s5')}">Pagos</a></li>
    <li><a @click="${()=> this.scrollTo('s6')}">Configuración</a></li>
    <li><a @click="${()=> this.scrollTo('s7')}">Roles de usuario</a></li>
    <li><a @click="${()=> this.scrollTo('s8')}">Solución de Problemas / Contacto</a></li>
    <li><a @click="${()=> this.scrollTo('s9')}">Planes</a></li>
    <li><a @click="${()=> this.scrollTo('s10')}">Seguridad de los Datos y Confidencialidad</a></li>
    <li><a @click="${()=> this.scrollTo('s11')}">Preguntas Frecuentes</a></li>
    <li><a @click="${()=> this.scrollTo('s12')}">CHANGELOG</a></li>
    <li><a @click="${()=> this.scrollTo('s13')}">Términos y Condiciones</a></li>
  </ul>
  <h4 id="s1">Primeros pasos</h4>
  <h5>Requisitos</h5>
  <p>Cualquier dispositivo que cuente con el Navegador Google Chrome</p>
  <p>Cuenta de correo de empresa 'usuario@tuempresa...'</p>
  <h5>Comenzar</h5>
  <p>Para utilizar nuestra aplicación es necesario completar primero unos sencillos pasos:</p>
  <ol>
    <li><a @click="${()=> this.scrollTo('s61')}">Llenar todos los datos</a> de su empresa en el menú configuración</li>
    <li><a @click="${()=> this.scrollTo('s41')}">Crear su primer Proveedor</a></li>
    <li><a @click="${()=> this.scrollTo('s31')}">Crear su primer Centro de Costo</a></li>
  </ol> 
  <p>Una vez completados, el sistema contará con todos los datos necesarios para generar y guardar sus órdenes de compra on line.</p>
  <p>Si accede desde Chrome para Windows o MacOS puede instalar nuestro sitio como aplicación en el menú Chrome ${moreVert} Opción 'Instalar OC'</p>
  <p>Si accede desde un dispositivo móvil puede agregar nuestra aplicación a la pantalla de inicio desde el mensaje que se despliega al abrir la página por primera vez o desde menú Chrome ${moreVert} Opción 'Agregar a la pantalla principal'</p>
  <h4 id="s2">Órdenes de Compra</h4>
  <div class="segmento"> 
    <h5>Crear una Orden de Compra</h5>
      <p>Todos los usuarios pueden crear órdenes de compra.</p>
      <p>Se accede al menú para crearla al presionar el botón <mwc-fab mini id="newOC" icon="add" disabled></mwc-fab> ubicado en la región superior derecha de la página.</p>
      <p>Son necesarios los siguientes datos:</p>
      <ol>
        <li>Centro de Costo</li>
        <li>Proveedor</li>
        <li>Al menos un item</li>
      </ol>
      <p>Puede agregar los siguientes datos:</p>
      <ul>
        <li>Destinatario de OC ('Dirigido a' / 'Atención')</li>
        <li>Cotización</li>
      </ul>
      <p>Para agregar un ítem debe completar los datos: nombre, cantidad, precio unitario (neto) y presionar el botón ${addToCartIcon}</p> 
    <h5>Numeración de Órdenes de Compra</h5> 
      <p>La numeración de las órdenes de compra es correlativa por unidades.</p> 
      <p> El número de orden de compra tiene dos partes:</p>
      <ol>
        <li>Identificador de Centro de costo: Asignado al Centro de Costo correspondiente al momento de su creación</li>
        <li>Número de orden de compra: Creado automáticamente por el sistema</li>
      </ol>
      <div class="noc">${noc}</div>
    <h5>Modificar una Orden de Compra</h5>
      <p>Una vez creada una Orden de Compra, es posible modificar, agregar o borrar sus ítems.</p>
      <p>Todos los usuarios pueden modificar Ítems en Órdenes de Compra que no han sido revisadas / autorizadas.</p> 
      <p>No es posible modificar Órdenes de Compra 'bloqueadas' ${lockClosed}</p>
      <p>Para modificar un ítem hay que hacer click en el botón <paper-icon-button icon="create"></paper-icon-button></p>         
      <p>Puede borrar un ítem al hacer click en el botón <paper-icon-button icon="delete-forever"></paper-icon-button></p>         
      <p>Para agregar un ítem, click en el botón ${ addToCartIcon }</p>         
      <p>Si necesita modificar los datos del proveedor, centro de costo o de la empresa es necesario <a @click="${()=> this.scrollTo('s26')}">anular</a> la orden de compra y crear una nueva con esos datos ya modificados.</p>
    <h5>Revisar / Autorizar una Orden de Compra</h5>
      <p>Los Administradores y Coordinadores pueden Revisar / Autorizar órdenes de compra</p>
      <p>Para confirmar este paso deben hacer click en el botón revisar, que aparece en la Orden de Compra correspondiente.</p>
      <p>Una vez revisada el ícono cambiará a ${revisado} y se activará la opción generar PDF en el botón <paper-icon-button icon="image:picture-as-pdf" style="display: inline-block;"></paper-icon-button></p>
      <p>Esta acción no se puede deshacer.</p>
      
    <h5 id="s25">Bloquear una Orden de Compra</h5>
      <p>Esta acción no se puede deshacer</p>
      <p>El ícono 'desbloqueado' ${lockOpen} pasará a 'bloqueado' ${lockClosed}</p>
      <p>No se podrán realizar modificaciones a la Orden de Compra y se agregará en el sistema como pendiente de pago.</p>
    <h5 id="s26">Anular una Orden de Compra</h5>
      <p>Sólo usuarios administradores o coordinadores.</p>
      <p>No se podrán anular órdenes de compra marcadas como ya pagadas en el sistema.</p>
      <p>Para anular una orden de compra debe hacer click en el botón 'anular' <paper-icon-button icon="cancel" style="display: inline-block;"></paper-icon-button></p> 
      <p>Ésto llevará su valor a cero, no afectando el presupuesto del Centro de Costo correspondiente y a su vez se eliminará de la sección pagos.</p>
      <p>Para Órdenes de Compra que hayan sido previamente bloqueadas.</p>
      <p>Esta acción no se puede deshacer.</p>
    <h5 id="s27">Flujograma</h5>
      <div class="diagrama">${diagrama}</div>
  </div>
  <h4 id="s3">Centros de Costo</h4>
  <div class="segmento">
    <h5 id="s31">Crear un Centro de Costo</h5>
      <p>Sólo Administradores.</p>
      <p>Se accede a esta opción a través del botón <mwc-fab mini id="newOC" icon="add" disabled></mwc-fab> en la parte superior derecha de la sección Centros de Costo.</p>
      <p>Debe completar todos los datos para poder guardar un nuevo Centro de Costo</p>
      <p>El identificador del Centro de Costo puede contener números y letras, desde 1 hasta 8 caracteres, y será parte del número de la Orden de Compra</p>
    <h5>Editar un Centro de Costo</h5>
      <p>Sólo administradores. Pueden editar:</p>
      <ul>
        <li>Nombre</li>
        <li>Identificador</li>
        <li>Ubicación</li>
        <li>Presupuesto</li>
      </ul>
      <p>Los cambios aplicarán sólo a las órdenes de compra futuras.</p>
    <h5>Completar un Centro de Costo</h5>
      <p>No se podrán agregar nuevas órdenes de compra a éste.</p>
      <p>Esta acción no se puede deshacer</p>      
  </div>
  <h4 id="s4">Proveedores</h4>
  <div class="segmento">
    <h5 id="s41">Crear un Proveedor</h5>
      <p>Se accede al menú para crearla al presionar el botón <mwc-fab mini id="newOC" icon="add" disabled></mwc-fab> ubicado en la región superior derecha de la página Proveedores.</p>
      <p>Recuerde completar todos los datos del proveedor antes de crear su orden de compra.</p>
    <h5>Modificar un Proveedor</h5>
      <p>Los cambios al proveedor sólo se aplicarán a las órdenes de compra futuras.</p>
      <p>Una vez creado, no se puede borrar un proveedor</p>
  </div>
  <h4 id="s5">Pagos</h4>
  <div class="segmento">
    <p>Sólo usuarios administradores o coordinadores.</p> 
    <h5>Filtrar Órdenes de Compra</h5>
      <p>El sistema permite filtrar las órdenes de compra según los siguientes criterios:</p>
      <ol>
        <li>Proveedor (seleccionado / todos)</li>
        <li>Estado de Pago (pagada / pendiente / todos)</li>
        <li>Fecha (inicio - fin)</li>
        <li>Texto en la de órden de compra (por ejemplo: Nº OC, Nº factura asociada al pago, etc)</li>
      </ol>
      <p>Por defecto se muestran todas las órdenes de compra.</p> 
      <p>Los filtros se pueden utilizar por separado o en cualquier combinación necesaria.</p>
      <p>El monto se actualiza automáticamente, mostrando la suma de las órdenes de compra seleccionadas.</p>
    <h5>Asignar Pago</h5>
      <p>Esta acción no se puede deshacer.</p>
      <p>Al hacer click en el ícono asignar pago ${error} se despliega el mensaje que permite confirmar el pago de la Orden de Compra correspondiente y agregar el Número de Factura asociado al pago.</p>
      <p>Las órdenes de compra pagadas ya no podrán ser anuladas desde la sección 'Órdenes de Compra'</p>
      <p>Una vez asignado el estado de "pagada", la Orden de Compra mostrará el ícono ${checkCircle}</p>            
  </div>
  <h4 id="s6">Configuración</h4>
    <p>Sólo usuarios administradores o coordinadores</p> 
  <div class="segmento">
    <h5 id="s61">Agregar o Modificar Datos</h5>
      <p>Todos los datos deben estar completos para poder generar las órdenes de compra.</p>
      <p>Las modificaciones de los datos en esta sección se aplican a las órdenes de compras futuras.</p>
      <p>No es posible realizar cambios retroactivos.</p>
    <h5>Cambiar <a @click="${()=> this.scrollTo('s7')}">Roles de Usuario</a></h5>
      <p>En el listado de usuarios ubicado en la última sección de la configuración es posible cambiar el rol de los usuarios de su empresa que han ingresado al sistema.</p>
      <p>Los cambios que se apliquen tardan hasta un minuto en actualizarse, si no es así el usuario puede intentar recargar la página para poder ingresar al sistema con el nuevo rol.</p>
  </div>
  <h4 id="s7">Roles de usuario</h4>
    <p>Los únicos usuarios que pueden realizar cambios en los roles de los usuarios del sistema son los administradores.</p>
    <p>Para ingresar como usuario del sistema es necesario contar con correo con dominio propio de la empresa '@tuempresa.cl'. Sólo los usuarios con correo del mismo dominio, que hayan ingresado al sistema, aparecerán en el listado.</p>
    <div class="segmento">
    <h5>Usuario Bloqueado</h5>

      <p>Asignado automáticamente a los nuevos usuarios del sistema OC</p>
      <p>No pueden acceder a menos que su rol sea cambiado a Usuario Común / Coordinador / Administrador</p>
    <h5>Usuario Común ${id}</h5>
      
      <p>Es el rol predeterminado para los usuarios recién ingresados al sistema.</p>
      <p>Pueden crear órdenes de compra y editar sus contenidos (items) hasta el momento de ser autorizada.</p>
      <p>No pueden autorizar órdenes de compra, pero pueden acceder a los PDF de las órdenes de compra autorizadas.</p>
      <p>Pueden crear y editar proveedores</p>
    <h5>Coordinador ${superuser}</h5>
      
      <p>Las funciones del usuario común.</p>
      <p>Puede editar las órdenes de compra luego de ser autorizada, hasta el momento de ser bloqueada.</p>
      <p>Puede <a @click="${()=> this.scrollTo('s25')}">bloquear</a> órdenes de compra. Esto permite confirmar su generación, evitar nuevas modificaciones y agregarla como pendiente para pago.</p>           
    <h5>Administrador ${supervisor}</h5>
      <p>Asignado automáticamente al primer usuario registrado de la empresa correspondiente en nuestro sistema</p>        
      <p>Todas las funciones del Coordinador</p> 
      <p>Puede crear y acceder a Centros de Costo</p>
      <p>Puede asignar roles y cargo a los usuarios de la aplicación.</p>
    </div>
  <h4 id="s8">Solución de problemas / contacto</h4>
  <div class="segmento"> 
    <p>Esta aplicación está optimizada para su uso con la última versión del navegador <a style="text-decoration: none" href="https://www.google.com/intl/es-419/chrome/" target="_blank" rel="noopener">Google Chrome</a>, en dispositivos Windows, Mac, Android e iOS.</p>
    <p>No se garantiza su uso en otros navegadores.</p>
    <p>Con cada actualización aparecerá un mensaje indicando recagar la página para tener la última versión disponible cargada en su dipositivo</p>       
    <p>Si encuentra problemas puede forzar la actualización de la página haciendo click con el boton derecho del mouse en el botón de recarga del navegador chrome seleccionando la opción 'vaciar caché y volver a cargar de manera forzada'.</p>       
    <p>Para consultas, sugerencias o solución de problemas puede contactarnos vía <a style="text-decoration: none" href="mailto:contacto@quetru.cl?Subject=Contacto%20OC" target="_top">email</a>.</p>
  </div>
  <h4 id="s9">Seguridad de los Datos y Confidencialidad</h4>
  <div class="segmento">
    <p>No compartiremos sus datos con otras empresas. Sin embargo sus datos serán alojados en nuestros servidores, proveídos como servicio por Google.</p>
    <p>Todas las comunicaciones con el servidor se hacen de forma segura vía <a href="https://es.wikipedia.org/wiki/Protocolo_seguro_de_transferencia_de_hipertexto" target="_blank" rel="noopener">https</a>.</p>
    <p>Nuestra dirección es <strong>https://ordendecompra.cl</strong>, siempre revise que corresponda con la barra de navegación de Chrome y que la barra de dirección tenga el ícono ${lock}.</p>
    <p>Nunca le enviaremos correos con links.</p>
    <p>Nunca le pediremos claves de correo. No la comparta, la seguridad de sus datos y los de su empresa dependen de que usted mantenga la seguridad de su contraseña.</p>
    <p>Aplicamos los estándares reconocidos por la industria para asegurar cualquier información personal en nuestra posesión, y para asegurarla de accesos no autorizados y forzados. Sin perjuicio de esto, te recordamos que como en todas las acciones online, es posible que terceros puedan ilegalmente interceptar trasmisiones de información, u otros usuarios del sitio puedan usar erróneamente o abusar de la información que puedan recolectar desde el Sitio.</p>
    <p>Para más detalles puedes revisar nuestra 
      <ul>
        <li><a href="https://ordendecompra.github.io/Terminos-y-Condiciones/PRIVACIDAD.html" target="_blank" rel="noopener">Política de Privacidad</a></li>
        <li><a href="https://ordendecompra.github.io/Terminos-y-Condiciones/" target="_blank" rel="noopener">Términos y Condiciones</a></li>
      </ul>
  </div>
  <h4 id="s10">Planes</h4>
  <div class="segmento">
    <h5>Plan Prueba</h5>
    <h5>Plan Pyme</h5>
    <h5>Plan Pro<h5>
  </div>
  <h4 id="s11">Preguntas Frecuentes</h4>
  <div class="segmento">
    <h5>Creé una Orden de Compra con el Centro de Costo / Proveedor equivocado ¿Puedo cambiarla?</h5>
    <p>No, y no la cambiaremos por usted. Por motivos de seguridad deberá anular la orden con los datos erróneos y crear una nueva.</p>
    <h5>Bloqueé una Orden de Compra. ¿Pueden desbloquearla por mí?</h5>
    <p>Sólo desbloquearemos OC si lo solicita el titular de una empresa con Cuenta PYME o PRO.</p>
  </div>
  <h4 id="s12">CHANGELOG</h4>
  <p>Registro de cambios importantes en actualizaciones</p>
  <div class="segmento changelog">
    <button class="accordion" id="b9" @click="${()=> this.accordion({b: 'b9', p: 'p9'})}">[0.1.5RC] 06 de Septiembre, 2019</button>    
    <div class="panel" id="p9">
      <h6>Agregado</h6>
      <ul>
        <li>CC: detalle de productos y servicios agregados al centro de costo (pagados y por pagar)</li>
        <li>CC: Es posible exportar detalle a excel</li>
        <li>Productos y Servicios: en construcción</li>
        <li>Pagos: detalle OC</li>
        <li>Proveedor: se agrega persona de contacto, que autorrellena el campo 'Atención' para OC</li>
        <li>Back End: respaldo diario automático de base de datos en servidor</li>
      </ul>
      <h6>Cambiado</h6>
      <ul>
        <li>Ligero cambio general de privilegios acceso</li>
        <li>PDF de OC no aprobada con sello de agua 'BORRADOR'</li>
        <li>Aspecto: listas en Desktop, tarjetas en Mobile, consistentes en todas las secciones de la app</li>
        <li>Versión RC: funciones casi completas, base de datos estable</li>
      </ul>
      <h6>Corregido</h6>
      <ul>
        <li>Múltiples Bugs menores</li>
      </ul>
    </div>
    <button class="accordion" id="b8" @click="${()=> this.accordion({b: 'b8', p: 'p8'})}">[0.1.4b] 16 de Agosto, 2019</button>    
    <div class="panel" id="p8">
      <h6>Agregado</h6>
      <ul>
        <li>OC: listadas en tabla en pantallas grandes</li>
        <li>OC: Nuevo menú filtrar OC</li>
        <li>OC: Nuevo menú para crear OC</li>
        <li>Menú crear OC: es posible agregar datos de cotizacion</li>
        <li>OC: Nuevo menú para editar OC</li>
        <li>Menú editar OC: es posible agregar y/o editar datos de cotizacion</li>
        <li>PDF: cotización</li>
        <li>Spinner Configuración Medio de Pago</li>
      </ul>
      <h6>Cambiado</h6>
      <ul>
        <li>Aspecto general sección OC</li>
      </ul>
      <h6>Corregido</h6>
      <ul>
        <li>Fecha OC en PDF</li>
      </ul>
    </div>
    <button class="accordion" id="b7" @click="${()=> this.accordion({b: 'b7', p: 'p7'})}">[0.1.3b] 29 de Julio, 2019</button>    
    <div class="panel" id="p7">
      <h6>Agregado</h6>
      <ul>
        <li>Servidor: Hooks QVO y Transbank</li>
        <li>Servidor: inscripción tarjeta crédito para pago</li>
        <li>Servidor: confirmación tarjeta crédito para pago</li>
        <li>Servidor: eliminación tarjeta crédito para pago</li>
        <li>Configuración Medio de Pago</li>
      </ul>
    </div> 
    <button class="accordion" id="b6" @click="${()=> this.accordion({b: 'b6', p: 'p6'})}">[0.1.2.1.5b] 26 de Julio, 2019</button>    
    <div class="panel" id="p6">
      <h6>Corregido</h6>
      <ul>
        <li>Conflicto ID Centro de Costo cuando comienza por número</li>
        <li>CC ordenados por fecha</li>
      </ul>
    </div>
    <button class="accordion" id="b5" @click="${()=> this.accordion({b: 'b5', p: 'p5'})}">[0.1.2.1.4b] 23 de Julio, 2019</button>    
    <div class="panel" id="p5">
      <h6>Agregado</h6>
      <ul>
        <li>Notificación al inicio: Número de OC por revisar</li>
        <li>Notificación al inicio: Número de OC por confirmar</li>
      </ul>
      <h6>Cambiado</h6>
      <ul>
        <li>Aspecto general, paleta de colores</li>
      </ul>
      <h6>Corregido</h6>
      <ul>
        <li>Presupuesto en Centro de Costo</li>
      </ul>
    </div>
    <button class="accordion" id="b4" @click="${()=> this.accordion({b: 'b4', p: 'p4'})}">[0.1.2.1.3b] 22 de Julio, 2019</button>    
    <div class="panel" id="p4">
      <h6>Agregado</h6>
      <ul>
        <li>Opciones de búsqueda de OC, por estado, proveedor, centro de costo y/o texto</li>
      </ul>
      <h6>Corregido</h6>
      <ul>
        <li>Valores con IVA en presupuestos de Centros de Costo</li>
      </ul>
    </div>
    <button class="accordion" id="b3" @click="${()=> this.accordion({b: 'b3', p: 'p3'})}">[0.1.2.1.2b] 21 de Julio, 2019</button>
    <div class="panel" id="p3">
      <h6>Unreleased</h6>
      <ul>
        <li>Back End para límites planes</li>
      </ul>
      <h6>Agregado</h6>
      <ul>
        <li>Datos pueden ser leídos y modificados offline</li>
        <li>Planes</li>
        <li>Gráfico presupuesto de Centro de Costo</li>
        <li>Centro de costo muestra presupuesto, monto de órdenes de compra (gastado) y monto ya pagado</li>
      </ul>
      <h6>Corregido</h6>
      <ul>
        <li>Centro de costo ordenado por fecha, no por número</li>
      </ul>
    </div>
    <button class="accordion" id="b2" @click="${()=> this.accordion({b: 'b2', p: 'p2'})}">[0.1.2.1.1b] 16 de Julio, 2019</button>    
    <div class="panel" id="p2">
      <h6>Agregado</h6>
      <ul>
        <li>Términos y Condiciones</li>
        <li>Política de Privacidad</li>
        <li>Preguntas Frecuentes</li>
      </ul>
      <h6>Corregido</h6>
      <ul>
        <li>Número de Orden de Compra en PDF</li>
      </ul>
    </div>
    <button class="accordion" id="b1" @click="${()=> this.accordion({b: 'b1', p: 'p1'})}">[0.1.2.1b] 15 de Julio, 2019</button>
    <div class="panel" id="p1">
      <h6>Agregado</h6>
      <ul>
        <li>Es posible crear identificadores únicos arbitrarios para CC</li>
        <li>Identificadores únicos de CC como parte de Nº OC</li>
        <li>Se crea el CHANGELOG como parte del Manual</li>
        <li>Se crea el perfil de usuario 'bloqueado'</li>
      </ul>
      <h6>Cambiado</h6>
      <ul>
        <li>ID de centro de costo precede a Nº OC</li>
        <li>Numeración de OC por unidades, independiente de CC</li>
      </ul>
      <h6>Eliminado</h6>
      <ul>
        <li>Se elimina numeración automática de CC</li>
      </ul>
      <h6>Seguridad</h6>
      <ul>
        <li>Primer usuario que ingresa a Sistema OC es administrador</li>
        <li>Nuevos usuarios que ingresan a Sistema OC bloqueados hasta que administradores los autoricen</li>
        <li>Implementación completa de ingeso con Email y Password</li>
      </ul>
    </div>
  </div>
</div>

<script>
	scrollTo(e){
	  const element = this.shadowRoot.querySelector(`#${e}`);
	  const yCoordinate = element.getBoundingClientRect().top + window.pageYOffset;
	  const yOffset = -85; 

	  window.scrollTo({
	      top: yCoordinate + yOffset,
	      behavior: 'smooth'
	  });
	}
</script>