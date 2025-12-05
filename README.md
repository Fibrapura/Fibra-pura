<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SuperPizza - ¡La mejor pizza a domicilio! | Pedidos online</title>
    <style>
        /* Estilo inspirado en Telepizza: colores rojo/naranja, tipografías sans-serif modernas, responsive, hero grande con ofertas */
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Arial', sans-serif; line-height: 1.6; color: #333; background: #f8f8f8; }
        
        /* Header fijo con logo, login y carrito */
        header { position: fixed; top: 0; width: 100%; background: linear-gradient(135deg, #ff6b35, #f7931e); color: white; z-index: 1000; box-shadow: 0 2px 10px rgba(0,0,0,0.1); }
        .header-container { max-width: 1200px; margin: 0 auto; display: flex; justify-content: space-between; align-items: center; padding: 1rem 2rem; }
        .logo { font-size: 1.8rem; font-weight: bold; }
        .header-actions { display: flex; gap: 1rem; align-items: center; }
        .login-btn, .carrito-btn { background: rgba(255,255,255,0.2); border: none; color: white; padding: 0.5rem 1rem; border-radius: 20px; cursor: pointer; transition: background 0.3s; }
        .login-btn:hover, .carrito-btn:hover { background: rgba(255,255,255,0.3); }
        
        /* Hero section grande con ofertas */
        .hero { background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1513104890138-7c749659a591?ixlib=rb-4.0.3&auto=format&fit=crop&w=2070&q=80') center/cover; height: 100vh; display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; color: white; margin-top: 70px; }
        .hero h1 { font-size: 3.5rem; margin-bottom: 1rem; text-shadow: 2px 2px 4px rgba(0,0,0,0.5); }
        .hero p { font-size: 1.3rem; margin-bottom: 2rem; }
        .cta-btn { background: #ff6b35; color: white; padding: 1rem 2.5rem; font-size: 1.2rem; border: none; border-radius: 30px; cursor: pointer; transition: transform 0.3s, box-shadow 0.3s; text-decoration: none; display: inline-block; }
        .cta-btn:hover { transform: scale(1.05); box-shadow: 0 10px 20px rgba(255,107,53,0.4); }
        
        /* Sección ofertas destacadas */
        .ofertas { max-width: 1200px; margin: 4rem auto; padding: 0 2rem; }
        .section-title { text-align: center; font-size: 2.5rem; color: #ff6b35; margin-bottom: 3rem; }
        .ofertas-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(350px, 1fr)); gap: 2rem; }
        .oferta-card { background: white; border-radius: 15px; overflow: hidden; box-shadow: 0 10px 30px rgba(0,0,0,0.1); transition: transform 0.3s; }
        .oferta-card:hover { transform: translateY(-10px); }
        .oferta-img { height: 200px; background: linear-gradient(45deg, #ff6b35, #f7931e); display: flex; align-items: center; justify-content: center; font-size: 2rem; color: white; }
        .oferta-content { padding: 1.5rem; }
        .precio { font-size: 2rem; color: #ff6b35; font-weight: bold; }
        .descuento { color: #28a745; font-weight: bold; }
        
        /* Navegación menú */
        nav { background: rgba(255,255,255,0.95); backdrop-filter: blur(10px); padding: 1rem 0; margin-top: 1rem; }
        .nav-container { max-width: 1200px; margin: 0 auto; display: flex; justify-content: center; gap: 3rem; }
        .nav-link { color: #333; text-decoration: none; font-weight: 500; padding: 0.5rem 1rem; border-radius: 20px; transition: background 0.3s; }
        .nav-link:hover { background: #ff6b35; color: white; }
        
        /* Ubicación y pedido */
        .ubicacion { background: #fff; padding: 3rem 2rem; text-align: center; }
        .ubicacion-input { max-width: 500px; margin: 0 auto; padding: 1rem; font-size: 1.1rem; border: 2px solid #ddd; border-radius: 10px; width: 100%; }
        
        /* Footer */
        footer { background: #333; color: white; text-align: center; padding: 2rem; }
        
        /* Responsive */
        @media (max-width: 768px) {
            .header-container { padding: 1rem; flex-direction: column; gap: 1rem; }
            .hero h1 { font-size: 2.5rem; }
            .nav-container { flex-wrap: wrap; gap: 1rem; }
            .ofertas-grid { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>
    <!-- Header fijo -->
    <header>
        <div class="header-container">
            <div class="logo">🍕 SuperPizza</div>
            <div class="header-actions">
                <button class="login-btn">Inicia sesión</button>
                <button class="carrito-btn">🛒 0€</button>
            </div>
        </div>
    </header>
    
    <!-- Hero principal -->
    <section class="hero">
        <h1>¡La mejor pizza a domicilio!</h1>
        <p>Pedidos online rápidos · Ofertas increíbles · Entrega en menos de 30 min</p>
        <a href="#pedir" class="cta-btn">¡Pide ahora!</a>
    </section>
    
    <!-- Navegación -->
    <nav>
        <div class="nav-container">
            <a href="#inicio" class="nav-link">Inicio</a>
            <a href="#menus" class="nav-link">Menús</a>
            <a href="#pizzas" class="nav-link">Pizzas</a>
            <a href="#ofertas" class="nav-link">Ofertas</a>
            <a href="#contacto" class="nav-link">Contacto</a>
        </div>
    </nav>
    
    <!-- Ofertas destacadas como en Telepizza -->
    <section id="ofertas" class="ofertas">
        <h2 class="section-title">🌟 Ofertas SuperCalientes</h2>
        <div class="ofertas-grid">
            <div class="oferta-card">
                <div class="oferta-img">🍕 TelepiBox Pizza</div>
                <div class="oferta-content">
                    <h3>Pizza (2 ing) + Entrante</h3>
                    <p class="precio">desde <span>5€</span></p>
                    <p class="descuento">+1,95€ pizza 5 ing o clásica</p>
                </div>
            </div>
            <div class="oferta-card">
                <div class="oferta-img">🍔 TelepiBox Burger</div>
                <div class="oferta-content">
                    <h3>Hamburguesa + Patatas + Bebida</h3>
                    <p class="precio"><span>10,95€</span></p>
                </div>
            </div>
            <div class="oferta-card">
                <div class="oferta-img">👨‍👩‍👧 Menú para 2</div>
                <div class="oferta-content">
                    <h3>Pizza mediana + 2 Entrantes + 2 Bebidas</h3>
                    <p class="precio"><span>18€</span></p>
                </div>
            </div>
            <div class="oferta-card">
                <div class="oferta-img">🍨 Menú Helado</div>
                <div class="oferta-content">
                    <h3>Pizza mediana + Häagen-Dazs 460ml</h3>
                    <p class="precio"><span>19,95€</span></p>
                </div>
            </div>
            <div class="oferta-card">
                <div class="oferta-img">👦 Menú Kids</div>
                <div class="oferta-content">
                    <h3>Pizza infantil + Bebida + Postre + Regalo</h3>
                    <p class="precio"><span>4,95€</span></p>
                </div>
            </div>
            <div class="oferta-card">
                <div class="oferta-img">🥪 Menú Sándwich</div>
                <div class="oferta-content">
                    <h3>Top Sándwich + Entrante + Bebida</h3>
                    <p class="precio"><span>9,95€</span></p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Sección ubicación/pedido -->
    <section class="ubicacion">
        <h2 style="color: #ff6b35; margin-bottom: 1rem;">📍 Introduce tu dirección</h2>
        <p style="margin-bottom: 1rem;">Encuentra las tiendas más cercanas y empieza a pedir</p>
        <input type="text" class="ubicacion-input" placeholder="Calle, número, piso, ciudad... o usa mi ubicación" id="pedir">
    </section>
    
    <!-- Footer -->
    <footer>
        <p>&copy; 2025 SuperPizza. ¡Pizza fresca todos los días! MiTelepi: acumula puntos y ahorra. [web:45][web:36]</p>
    </footer>
    
    <script>
        // Funcionalidad básica interactiva
        document.querySelector('.login-btn').onclick = () => alert('¡Bienvenido a MiTelepi! Acumula puntos con tus pedidos.');
        document.querySelector('.carrito-btn').onclick = () => alert('🛒 Carrito vacío. ¡Empieza a pedir!');
        document.getElementById('pedir').onkeypress = (e) => { if (e.key === 'Enter') alert('¡Buscando tiendas cercanas!'); };
        // Smooth scroll
        document.querySelector('.cta-btn').onclick = (e) => { e.preventDefault(); document.querySelector('.ubicacion').scrollIntoView({behavior: 'smooth'}); };
    </script>
</body>
</html>
