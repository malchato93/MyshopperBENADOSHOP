# MyBENADOSHOP
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Benadoshop | Tienda Oficial</title>
    <style>
        /* --- ESTILOS GENERALES Y MODERNOS --- */
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; }
        body { background-color: #f7f9fc; color: #333; padding-bottom: 60px; }
        
        header { background: linear-gradient(135deg, #0056b3, #0088ff); color: white; padding: 30px 15px; text-align: center; box-shadow: 0 4px 12px rgba(0,0,0,0.1); }
        header h1 { font-size: 2.2rem; font-weight: bold; letter-spacing: 1px; }
        header p { font-size: 1rem; margin-top: 5px; opacity: 0.9; }

        .section-title { text-align: center; margin: 30px 0 10px; font-size: 1.5rem; color: #0056b3; position: relative; }
        .section-title::after { content: ''; display: block; width: 50px; height: 3px; background: #ffc107; margin: 8px auto 0; border-radius: 2px; }

        .container { max-width: 1200px; margin: 0 auto; padding: 15px; display: flex; flex-wrap: wrap; justify-content: center; gap: 20px; }

        /* --- TARJETAS DE PRODUCTOS --- */
        .product-card { background: white; border-radius: 12px; width: 280px; padding: 15px; box-shadow: 0 6px 15px rgba(0,0,0,0.05); display: flex; flex-direction: column; justify-content: space-between; transition: transform 0.2s; position: relative; border: 1px solid #eef2f7; }
        .product-card:hover { transform: translateY(-5px); }
        
        /* Contenedor de foto temporal (aquí encriptarás/colocarás las rutas de tus imágenes reales) */
        .img-placeholder { width: 100%; height: 180px; background-color: #eaeff5; border-radius: 8px; display: flex; align-items: center; justify-content: center; color: #7c8ba1; font-size: 0.9rem; margin-bottom: 12px; font-weight: 500; text-align: center; padding: 10px; }
        
        .product-card h3 { font-size: 1.1rem; color: #222; margin-bottom: 6px; min-height: 44px; display: flex; align-items: center; }
        .badge { align-self: flex-start; background: #e3f2fd; color: #0d47a1; padding: 4px 8px; border-radius: 6px; font-size: 0.75rem; font-weight: bold; margin-bottom: 10px; text-transform: uppercase; }
        .badge.personal { background: #f3e5f5; color: #4a148c; }
        
        .price-box { display: flex; justify-content: space-between; align-items: center; margin: 12px 0; }
        .price { font-size: 1.3rem; color: #2e7d32; font-weight: bold; }
        
        .btn-info { background: none; border: none; color: #0088ff; cursor: pointer; font-size: 0.85rem; font-weight: 600; text-decoration: underline; }
        .btn-add { background-color: #0056b3; color: white; border: none; padding: 10px; font-weight: bold; border-radius: 8px; cursor: pointer; width: 100%; transition: background 0.2s; }
        .btn-add:hover { background-color: #003d82; }

        /* --- VENTANAS DE INFORMACIÓN (MODALES) --- */
        .modal { display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.5); justify-content: center; align-items: center; z-index: 1000; padding: 20px; }
        .modal-content { background: white; padding: 25px; border-radius: 12px; max-width: 450px; width: 100%; box-shadow: 0 10px 25px rgba(0,0,0,0.2); position: relative; }
        .close-modal { position: absolute; top: 12px; right: 15px; font-size: 1.5rem; cursor: pointer; color: #aaa; }
        .modal-content h4 { font-size: 1.3rem; margin-bottom: 10px; color: #0056b3; }
        .modal-content p { font-size: 0.95rem; line-height: 1.5; color: #555; margin-bottom: 8px; }

        /* --- APARTADO DEL CARRITO Y PAGO --- */
        .checkout-section { max-width: 600px; margin: 40px auto; background: white; padding: 25px; border-radius: 12px; box-shadow: 0 6px 20px rgba(0,0,0,0.08); border: 1px solid #eef2f7; }
        .cart-item { display: flex; justify-content: space-between; align-items: center; padding: 10px 0; border-bottom: 1px dashed #e2e8f0; font-size: 0.95rem; }
        .cart-item button { background: #ffdde2; color: #c53030; border: none; padding: 2px 8px; border-radius: 4px; cursor: pointer; font-size: 0.8rem; }
        .cart-empty { text-align: center; color: #888; padding: 20px 0; font-style: italic; }
        
        .total-box { display: flex; justify-content: space-between; font-size: 1.3rem; font-weight: bold; margin: 20px 0; padding-top: 15px; border-top: 2px solid #0056b3; color: #2e7d32; }
        
        .payment-methods { margin-bottom: 25px; background: #f8fafc; padding: 15px; border-radius: 8px; border: 1px solid #e2e8f0; }
        .payment-methods h4 { font-size: 1rem; margin-bottom: 10px; color: #475569; }
        .payment-option { display: flex; align-items: center; gap: 10px; margin-bottom: 8px; font-size: 0.9rem; cursor: pointer; }
        
        .btn-whatsapp { display: flex; align-items: center; justify-content: center; gap: 10px; background-color: #25d366; color: white; border: none; padding: 14px; font-size: 1.1rem; font-weight: bold; border-radius: 8px; cursor: pointer; width: 100%; transition: background 0.2s; box-shadow: 0 4px 10px rgba(37,211,102,0.3); }
        .btn-whatsapp:hover { background-color: #1ebd59; }
    </style>
</head>
<body>

    <header>
        <h1>Benadoshop</h1>
        <p>Tu Ventana Comercial de Limpieza y Cuidado Personal 100% Ecuatoriano</p>
    </header>

    <!-- ================= CATALOGO DE PRODUCTOS ================= -->
    <div class="section-title">Insumos de Limpieza para el Hogar</div>
    <div class="container" id="hogar-container"></div>

    <div class="section-title">Línea Natural de Aseo Personal</div>
    <div class="container" id="personal-container"></div>

    <!-- ================= APARTADO DEL CARRITO ================= -->
    <div class="section-title">Tu Pedido Virtual</div>
    <div class="checkout-section">
        <div id="cart-items-container">
            <!-- Los productos agregados aparecerán aquí dinámicamente -->
        </div>
        
        <div class="total-box">
            <span>Suma Total:</span>
            <span id="cart-total">$0.00</span>
        </div>

        <!-- Opciones de Pago Requeridas -->
        <div class="payment-methods">
            <h4>Selecciona tu método de pago preferido:</h4>
            <label class="payment-option">
                <input type="radio" name="payment" value="Banco Guayaquil / Internacional" checked>
                <span><strong>Transferencia Bancaria</strong> (Banco Guayaquil o Banco Internacional)</span>
            </label>
            <label class="payment-option">
                <input type="radio" name="payment" value="Tarjeta mediante PLUX">
                <span><strong>Pago con Tarjeta</strong> (Procesado mediante la App PLUX)</span>
            </label>
        </div>

        <!-- Botón de Envío Directo a tu WhatsApp -->
        <button class="btn-whatsapp" onclick="enviarPedidoWhatsApp()">
            ➔ Enviar Pedido por WhatsApp
        </button>
    </div>

    <!-- ================= VENTANA DE INFORMACIÓN (MODAL) ================= -->
    <div class="modal" id="info-modal">
        <div class="modal-content">
            <span class="close-modal" onclick="cerrarModal()">&times;</span>
            <h4 id="modal-title">Título del Producto</h4>
            <p id="modal-desc">Descripción...</p>
            <p><strong>Registro Sanitario:</strong> <span id="modal-sanitario">N/A</span></p>
        </div>
    </div>

    <!-- ================= LÓGICA EN JAVASCRIPT ================= -->
    <script>
        // Listado exclusivo de los productos más vendidos y solicitados
        const productos = [
            // --- HOGAR ---
            { id: 'H01', tipo: 'hogar', nombre: 'Lavavajillas Arranca Grasa', precio: 3.25, sanitario: '7891-MAN-0626', desc: 'Fórmula ultra concentrada diseñada para eliminar la grasa más difícil de platos y ollas al instante sin maltratar tus manos.' },
            { id: 'H02', tipo: 'hogar', nombre: 'Ultrajarro Destapador de Caños', precio: 4.50, sanitario: '1123-MAN-0626', desc: 'Poderoso removedor químico de obstrucciones orgánicas, grasas y residuos acumulados en tuberías y cañerías.' },
            { id: 'H03', tipo: 'hogar', nombre: 'Cloro Líquido Tradicional', precio: 1.50, sanitario: '4556-MAN-0626', desc: 'Desinfectante y blanqueador multiusos de alta pureza, ideal para pisos, baños y desinfección profunda del hogar.' },
            { id: 'H04', tipo: 'hogar', nombre: 'Cloro en Gel de Alta Densidad', precio: 2.80, sanitario: '9982-MAN-0626', desc: 'Fórmula en gel que se adhiere a las superficies verticales del baño y cocina garantizando una desinfección prolongada sin salpicaduras.' },
            { id: 'H05', tipo: 'hogar', nombre: 'Quita Manchas Textil Potente', precio: 3.90, sanitario: '3344-MAN-0626', desc: 'Removedor activo de manchas difíciles (café, grasa, vino) ideal para aplicar directo en cuellos, puños y prendas delicadas antes del lavado.' },
            { id: 'H06', tipo: 'hogar', nombre: 'Detergente Líquido Ropa Oscura', precio: 4.20, sanitario: '5566-MAN-0626', desc: 'Protege el color original de tus prendas negras y oscuras evitando el desgaste prematuro de las fibras y dejando un aroma fresco.' },
            { id: 'H07', tipo: 'hogar', nombre: 'Trapeador Versátil Ergonómico', precio: 6.50, sanitario: 'No Requiere (Accesorio)', desc: 'Diseño super absorbente y de alta durabilidad, ideal para todo tipo de pisos (baldosa, flotante, madera) con mango ergonómico.' },
            // --- PERSONAL ---
            { id: 'P01', tipo: 'personal', nombre: 'Shampoo de Cebolla (Natural)', precio: 7.50, sanitario: '0012-COS-0626', desc: 'Línea Estefanía Hidalgo. Estimula el crecimiento acelerado del cabello, frena la caída y aporta un brillo espectacular de raíz a puntas sin dejar olor a cebolla.' },
            { id: 'P02', tipo: 'personal', nombre: 'Champú de Romero (Cuerpo y Brillo)', precio: 7.50, sanitario: '0015-COS-0626', desc: 'Línea Estefanía Hidalgo. Nutrición herbal profunda que fortalece el folículo capilar, purifica el cuero cabelludo y regula la grasa natural.' }
        ];

        let carrito = {};

        // Renderizar dinámicamente los productos en sus respectivos bloques
        function cargarCatalogo() {
            const hogarCont = document.getElementById('hogar-container');
            const personalCont = document.getElementById('personal-container');
            
            productos.forEach(prod => {
                const card = document.createElement('div');
                card.className = 'product-card';
                card.innerHTML = `
                    <div>
                        <div class="badge ${prod.type === 'personal' ? 'personal' : ''}">${prod.tipo === 'hogar' ? 'Hogar' : 'Aseo Personal'}</div>
                        <!-- Aquí se encriptarán/vincularán tus fotos físicas en el futuro -->
                        <div class="img-placeholder">📸 Foto de ${prod.nombre}</div>
                        <h3>${prod.nombre}</h3>
                    </div>
                    <div>
                        <div class="price-box">
                            <span class="price">$${prod.precio.toFixed(2)}</span>
                            <button class="btn-info" onclick="verInfo('${prod.id}')">Saber más</button>
                        </div>
                        <button class="btn-add" onclick="agregarAlCarrito('${prod.id}')">Añadir al carrito</button>
                    </div>
                `;
                if(prod.tipo === 'hogar') hogarCont.appendChild(card);
                else personalCont.appendChild(card);
            });
            actualizarInterfazCarrito();
        }

        // Controlar la "Nube" del Carrito de Compras
        function agregarAlCarrito(id) {
            if (carrito[id]) {
                carrito[id].cantidad += 1;
            } else {
                const prodOriginal = productos.find(p => p.id === id);
                carrito[id] = { ...prodOriginal, cantidad: 1 };
            }
            actualizarInterfazCarrito();
        }

        function removerDelCarrito(id) {
            delete carrito[id];
            actualizarInterfazCarrito();
        }

        function actualizarInterfazCarrito() {
            const container = document.getElementById('cart-items-container');
            const totalElement = document.getElementById('cart-total');
            container.innerHTML = '';
            
            let llaves = Object.keys(carrito);
            if (llaves.length === 0) {
                container.innerHTML = '<p class="cart-empty">Tu carrito está vacío. Agrega productos de limpieza o aseo arriba.</p>';
                totalElement.innerText = '$0.00';
                return;
            }

            let sumaTotal = 0;
            llaves.forEach(id => {
                const item = carrito[id];
                const subtotal = item.precio * item.cantidad;
                sumaTotal += subtotal;

                const row = document.createElement('div');
                row.className = 'cart-item';
                row.innerHTML = `
                    <span><strong>${item.cantidad}x</strong> ${item.nombre} ($${subtotal.toFixed(2)})</span>
                    <button onclick="removerDelCarrito('${id}')">Quitar</button>
                `;
                container.appendChild(row);
            });

            totalElement.innerText = `$${sumaTotal.toFixed(2)}`;
        }

        // Controladores de las Ventanas Emergentes de Información
        function verInfo(id) {
            const prod = productos.find(p => p.id === id);
            document.getElementById('modal-title').innerText = prod.nombre;
            document.getElementById('modal-desc').innerText = prod.desc;
            document.getElementById('modal-sanitario').innerText = prod.sanitario;
            document.getElementById('info-modal').style.display = 'flex';
        }

        function cerrarModal() {
            document.getElementById('info-modal').style.display = 'none';
        }

        // Enlace Dinámico Final y Procesamiento de Pedido
        function enviarPedidoWhatsApp() {
            let llaves = Object.keys(carrito);
            if (llaves.length === 0) {
                alert('Por favor, añade al menos un producto a tu pedido virtual antes de enviar.');
                return;
            }

            const metodoPagoSeleccionado = document.querySelector('input[name="payment"]:checked').value;
            
            // Construcción del texto formateado de forma limpia para tu lectura comercial
            let mensaje = `*NUEVO PEDIDO - BENADOSHOP*\n\n`;
            let sumaTotal = 0;
            
            llaves.forEach(id => {
                const item = carrito[id];
                const subtotal = item.precio * item.cantidad;
                sumaTotal += subtotal;
                mensaje += `• ${item.cantidad}x ${item.nombre} -> $${subtotal.toFixed(2)}\n`;
            });

            mensaje += `\n*TOTAL A PAGAR:* $${sumaTotal.toFixed(2)}\n`;
            mensaje += `*MÉTODO DE PAGO:* ${metodoPagoSeleccionado}\n`;
            
            // Tu enlace QR convertido a link directo de envío con texto precargado
            const baseWhatsAppUrl = "https://wa.me/qr/6A3SEFKKE25XN1";
            // Usamos la API estándar de texto para que el mensaje viaje enlazado
            const finalUrl = `https://wa.me/593992523825?text=${encodeURIComponent(mensaje)}`; 
            
            // Redirige al cliente al chat directo con su carrito armado
            window.open(finalUrl, '_blank');
        }

        // Iniciar todo al cargar la página
        window.onload = cargarCatalogo;
    </script>
</body>
</html>
