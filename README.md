# MyshopperBENADOSHOP
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Benadoshop - Productos de Limpieza Ecuatorianos</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 0; padding: 0; background-color: #f4f6f9; }
        header { background-color: #0056b3; color: white; padding: 15px; text-align: center; }
        .container { max-width: 1200px; margin: 20px auto; padding: 10px; display: flex; flex-wrap: wrap; justify-content: space-around; }
        .product-card { background: white; border: 1px solid #ddd; border-radius: 8px; width: 300px; margin: 15px; padding: 20px; box-shadow: 0 4px 6px rgba(0,0,0,0.1); text-align: center; }
        .product-card h3 { color: #333; margin-bottom: 10px; }
        .price { font-size: 1.25em; color: #28a745; font-weight: bold; margin: 10px 0; }
        .badge { background-color: #17a2b8; color: white; padding: 5px 10px; border-radius: 4px; font-size: 0.85em; }
        .btn-buy { background-color: #ffc107; color: #212529; border: none; padding: 10px 15px; font-weight: bold; border-radius: 4px; cursor: pointer; width: 100%; margin-top: 10px; }
        .btn-buy:hover { background-color: #e0a800; }
    </style>
</head>
<body>

    <header>
        <h1>Benadoshop</h1>
        <p>Ventana Comercial de Insumos de Limpieza Nacionales</p>
    </header>

    <div class="container">
        <!-- Producto 1 -->
        <div class="product-card">
            <h3>Desinfectante Lavanda 1L</h3>
            <span class="badge">Registro Sanitario: OK</span>
            <p class="price">$2.50</p>
            <p>Stock disponible: 50 unidades</p>
            <button class="btn-buy">Añadir al Carrito</button>
        </div>

        <!-- Producto 2 -->
        <div class="product-card">
            <h3>Lavavajillas Líquido Limón</h3>
            <span class="badge">Registro Sanitario: OK</span>
            <p class="price">$3.10</p>
            <p>Stock disponible: 40 unidades</p>
            <button class="btn-buy">Añadir al Carrito</button>
        </div>

        <!-- Producto 3 -->
        <div class="product-card">
            <h3>Cloro Concentrado Galón</h3>
            <span class="badge">Registro Sanitario: OK</span>
            <p class="price">$1.80</p>
            <p>Stock disponible: 30 unidades</p>
            <button class="btn-buy">Añadir al Carrito</button>
        </div>
    </div>

</body>
</html>
