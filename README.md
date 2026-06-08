<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
  <title>ArmsDeck | Jual Beli Senjata Koleksi & Replika</title>
  <!-- Font Awesome 6 (free icons) -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <!-- Google Fonts: modern sans + display -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700;14..32,800&family=Orbitron:wght@400;600;800&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: radial-gradient(circle at 10% 20%, #0a0c12, #030507);
      font-family: 'Inter', sans-serif;
      color: #eceff4;
      line-height: 1.5;
      padding: 2rem 1.5rem;
    }

    /* custom scroll */
    ::-webkit-scrollbar {
      width: 6px;
    }
    ::-webkit-scrollbar-track {
      background: #1e1f2c;
      border-radius: 8px;
    }
    ::-webkit-scrollbar-thumb {
      background: #b91c1c;
      border-radius: 8px;
    }

    .container {
      max-width: 1400px;
      margin: 0 auto;
    }

    /* header section */
    .header {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
      gap: 1rem;
      margin-bottom: 2.5rem;
      padding-bottom: 1rem;
      border-bottom: 2px solid rgba(185, 28, 28, 0.4);
    }
    .logo-area {
      display: flex;
      align-items: baseline;
      gap: 8px;
      flex-wrap: wrap;
    }
    .logo-icon {
      font-size: 2.3rem;
      color: #e63946;
      filter: drop-shadow(0 0 4px #b91c1c);
    }
    .logo-text {
      font-family: 'Orbitron', monospace;
      font-weight: 800;
      font-size: 1.9rem;
      letter-spacing: -0.5px;
      background: linear-gradient(135deg, #fff, #e63946);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }
    .logo-badge {
      font-size: 0.8rem;
      background: #1e1f2c;
      padding: 4px 10px;
      border-radius: 40px;
      border-left: 3px solid #e63946;
      font-weight: 500;
    }
    .cart-badge-header {
      background: #1e1f2c;
      padding: 10px 20px;
      border-radius: 60px;
      display: flex;
      align-items: center;
      gap: 12px;
      font-weight: 600;
      backdrop-filter: blur(4px);
      box-shadow: 0 4px 15px rgba(0,0,0,0.3);
    }
    .cart-badge-header i {
      font-size: 1.4rem;
      color: #e63946;
    }
    .cart-count {
      background: #e63946;
      color: white;
      border-radius: 40px;
      padding: 2px 10px;
      font-weight: bold;
      font-size: 0.9rem;
    }

    /* layout grid: produk 2/3, keranjang 1/3 */
    .market-grid {
      display: grid;
      grid-template-columns: 1fr 360px;
      gap: 2rem;
    }

    /* produk grid */
    .products-section h2 {
      font-size: 1.7rem;
      font-weight: 700;
      margin-bottom: 1.5rem;
      display: flex;
      align-items: center;
      gap: 10px;
    }
    .products-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
      gap: 1.8rem;
    }
    .product-card {
      background: rgba(18, 20, 28, 0.85);
      backdrop-filter: blur(4px);
      border-radius: 28px;
      padding: 1.2rem 1rem 1.5rem;
      transition: all 0.25s ease;
      border: 1px solid rgba(230, 57, 70, 0.2);
      box-shadow: 0 10px 20px -5px rgba(0, 0, 0, 0.5);
    }
    .product-card:hover {
      transform: translateY(-6px);
      border-color: #e63946;
      box-shadow: 0 20px 30px -12px rgba(185, 28, 28, 0.3);
    }
    .product-icon {
      font-size: 3.5rem;
      text-align: center;
      padding: 1rem 0;
      background: #0f111a;
      border-radius: 60px;
      margin-bottom: 1rem;
      color: #e63946;
    }
    .product-title {
      font-size: 1.4rem;
      font-weight: 700;
      margin-bottom: 0.4rem;
    }
    .product-desc {
      font-size: 0.8rem;
      color: #a7a9be;
      margin: 0.5rem 0;
      height: 48px;
    }
    .price {
      font-size: 1.5rem;
      font-weight: 800;
      color: #facc15;
      margin: 0.75rem 0;
    }
    .btn-add {
      width: 100%;
      background: #1e1f2e;
      border: none;
      padding: 12px 0;
      border-radius: 40px;
      font-weight: 700;
      color: white;
      font-size: 0.9rem;
      cursor: pointer;
      transition: 0.2s;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
      border: 1px solid #3a3c4e;
    }
    .btn-add:hover {
      background: #e63946;
      border-color: #e63946;
      color: white;
      transform: scale(0.98);
      box-shadow: 0 0 8px #e63946;
    }

    /* cart panel styling */
    .cart-panel {
      background: #0e1017e6;
      backdrop-filter: blur(12px);
      border-radius: 32px;
      padding: 1.5rem 1.2rem;
      border: 1px solid #2c2e3e;
      position: sticky;
      top: 2rem;
      height: fit-content;
      box-shadow: 0 15px 30px rgba(0,0,0,0.5);
    }
    .cart-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 1px solid #2c2e3e;
      padding-bottom: 12px;
      margin-bottom: 18px;
      font-size: 1.3rem;
      font-weight: 700;
    }
    .cart-items {
      max-height: 420px;
      overflow-y: auto;
      margin-bottom: 1rem;
      padding-right: 5px;
    }
    .cart-item {
      display: flex;
      justify-content: space-between;
      align-items: center;
      background: #181c26;
      border-radius: 20px;
      padding: 10px 12px;
      margin-bottom: 10px;
      font-size: 0.85rem;
    }
    .cart-item-info {
      flex: 2;
    }
    .cart-item-title {
      font-weight: 600;
    }
    .cart-item-price {
      font-size: 0.75rem;
      color: #facc15;
    }
    .cart-qty-control {
      display: flex;
      align-items: center;
      gap: 8px;
      background: #0b0e14;
      padding: 4px 8px;
      border-radius: 40px;
    }
    .cart-qty-control button {
      background: none;
      border: none;
      color: #eceff4;
      font-weight: bold;
      font-size: 1rem;
      cursor: pointer;
      width: 26px;
      border-radius: 30px;
      transition: 0.1s;
    }
    .cart-qty-control button:hover {
      background: #e63946;
      color: white;
    }
    .cart-item-remove {
      color: #a7a9be;
      background: #1e1f2c;
      border: none;
      border-radius: 30px;
      padding: 6px 10px;
      cursor: pointer;
      margin-left: 6px;
      transition: 0.2s;
    }
    .cart-item-remove:hover {
      background: #b91c1c;
      color: white;
    }
    .cart-total {
      margin: 1rem 0;
      padding: 14px 0;
      border-top: 2px dashed #2c2e3e;
      font-size: 1.3rem;
      font-weight: 800;
      display: flex;
      justify-content: space-between;
    }
    .btn-checkout {
      background: #e63946;
      width: 100%;
      padding: 14px;
      border: none;
      border-radius: 60px;
      font-weight: bold;
      font-size: 1rem;
      color: white;
      cursor: pointer;
      transition: 0.2s;
      margin-top: 8px;
    }
    .btn-checkout:hover {
      background: #b91c1c;
      box-shadow: 0 0 12px #e63946;
    }
    .btn-clear {
      background: transparent;
      border: 1px solid #6c6f85;
      width: 100%;
      padding: 10px;
      border-radius: 60px;
      color: #cdd1e8;
      margin-top: 12px;
      cursor: pointer;
      font-weight: 500;
    }
    .empty-cart-msg {
      text-align: center;
      padding: 30px 10px;
      color: #8e92aa;
    }
    footer {
      margin-top: 4rem;
      text-align: center;
      font-size: 0.75rem;
      color: #6c6f85;
      border-top: 1px solid #262a36;
      padding-top: 2rem;
    }
    @media (max-width: 860px) {
      .market-grid {
        grid-template-columns: 1fr;
        gap: 2rem;
      }
      .cart-panel {
        position: relative;
        top: 0;
      }
      body {
        padding: 1.2rem;
      }
      .logo-text {
        font-size: 1.5rem;
      }
    }
    .disclaimer-note {
      font-size: 0.7rem;
      margin-top: 12px;
      background: #1a1d29;
      border-radius: 20px;
      padding: 10px;
      text-align: center;
    }
    i.fa, i.fas, i.far {
      pointer-events: none;
    }
  </style>
</head>
<body>
<div class="container">
  <!-- Header dengan nama bagus: ARMS DECK - Senjata Legendaris -->
  <div class="header">
    <div class="logo-area">
      <i class="fas fa-skull logo-icon"></i>
      <span class="logo-text">ARMS DECK</span>
      <span class="logo-badge"><i class="fas fa-fire"></i> PREMIUM ARSENAL</span>
    </div>
    <div class="cart-badge-header">
      <i class="fas fa-shopping-cart"></i>
      <span>Keranjang</span>
      <span id="cartTotalItems" class="cart-count">0</span>
    </div>
  </div>

  <!-- Main marketplace grid -->
  <div class="market-grid">
    <!-- bagian kiri: daftar produk senjata -->
    <div class="products-section">
      <h2><i class="fas fa-gun"></i> Senjata Pilihan <span style="font-size:0.9rem; background:#1f2233; padding:4px 12px; border-radius:30px;">replika & koleksi</span></h2>
      <div class="products-grid" id="productsGrid"></div>
      <div class="disclaimer-note">
        <i class="fas fa-shield-alt"></i> Semua produk adalah replika / airsoft / koleksi fiktif. Demo jual-beli non-aktual.
      </div>
    </div>

    <!-- bagian kanan: keranjang belanja -->
    <div class="cart-panel">
      <div class="cart-header">
        <span><i class="fas fa-cart-plus"></i> Keranjang Belanja</span>
        <i class="fas fa-lock" style="font-size:0.9rem; opacity:0.7"></i>
      </div>
      <div id="cartItemsContainer" class="cart-items">
        <!-- cart items diisi javascript -->
        <div class="empty-cart-msg"><i class="fas fa-box-open"></i> Keranjang kosong, tambah senjata dulu!</div>
      </div>
      <div class="cart-total">
        <span>Total belanja</span>
        <span id="cartTotalPrice">Rp 0</span>
      </div>
      <button class="btn-checkout" id="checkoutBtn"><i class="fas fa-credit-card"></i> Checkout (Demo)</button>
      <button class="btn-clear" id="clearCartBtn"><i class="fas fa-trash-alt"></i> Kosongkan Keranjang</button>
    </div>
  </div>
  <footer>
    <i class="fas fa-dragon"></i> ARMS DECK — Marketplace senjata taktis & koleksi terpercaya (hanya simulasi frontend) <br>
    © 2025 | Untuk kalangan kolektor & penggemar fiksi militer.
  </footer>
</div>

<script>
  // ======================= DATA PRODUK SENJATA =======================
  const weapons = [
    {
      id: 1,
      name: "Katana Naga Hitam",
      desc: "Pedang baja karbon, replika koleksi limited. Tajam & elegan.",
      price: 2500000,
      icon: "fa-sword",
      color: "#e63946"
    },
    {
      id: 2,
      name: "Pistol Tempur G18",
      desc: "Replika gas blowback, body polimer kokoh, popor lipat.",
      price: 1400000,
      icon: "fa-gun",
      color: "#e63946"
    },
    {
      id: 3,
      name: "Kapak Perang Frost",
      desc: "Kapak Viking premium, pegangan kulit sintetis, sangat kokoh.",
      price: 750000,
      icon: "fa-axe",
      color: "#e63946"
    },
    {
      id: 4,
      name: "Granat Taktik Replika",
      desc: "Granat latihan visual, efek suara simulasi, aman untuk koleksi.",
      price: 350000,
      icon: "fa-bomb",
      color: "#e63946"
    },
    {
      id: 5,
      name: "Sniper Kar 98",
      desc: "Airsoft bolt-action, presisi tinggi, aksesori scope.",
      price: 3200000,
      icon: "fa-bullseye",
      color: "#e63946"
    },
    {
      id: 6,
      name: "Assault Rifle ARX-15",
      desc: "Replika electric, rails taktis, ready untuk modifikasi.",
      price: 2900000,
      icon: "fa-gun",
      color: "#e63946"
    }
  ];

  // Keranjang state (array of { id, quantity })
  let cart = [];

  // Fungsi simpan ke localStorage (opsional agar tahan refresh)
  function saveCartToLocal() {
    localStorage.setItem("armsdeck_cart", JSON.stringify(cart));
  }

  function loadCartFromLocal() {
    const stored = localStorage.getItem("armsdeck_cart");
    if (stored) {
      try {
        cart = JSON.parse(stored);
        // validasi agar quantity > 0
        cart = cart.filter(item => item.quantity > 0);
      } catch(e) { cart = []; }
    } else {
      cart = [];
    }
  }

  // Helper: cari produk berdasarkan id
  function getProductById(id) {
    return weapons.find(p => p.id === id);
  }

  // Hitung total item di keranjang (jumlah quantity)
  function getTotalItemCount() {
    return cart.reduce((sum, item) => sum + item.quantity, 0);
  }

  // Hitung total harga
  function getTotalCartPrice() {
    let total = 0;
    cart.forEach(item => {
      const product = getProductById(item.id);
      if (product) total += product.price * item.quantity;
    });
    return total;
  }

  // Render ulang tampilan produk (product cards)
  function renderProducts() {
    const productsGrid = document.getElementById("productsGrid");
    if (!productsGrid) return;
    productsGrid.innerHTML = "";
    weapons.forEach(weapon => {
      const card = document.createElement("div");
      card.className = "product-card";
      // Ikon dinamis menggunakan FontAwesome
      let iconHtml = `<i class="fas ${weapon.icon}"></i>`;
      if (weapon.icon === "fa-axe") iconHtml = `<i class="fas fa-hatchet"></i>`; // fallback axe tersedia di FA6? 'fa-axe' tidak standar di free? tapi yg standard adalah fa-axe-battle? Kita akan pakai 'fa-axe' tapi untuk memastikan gunakan fa-gavel? Tidak, font awesome 6 free punya fa-axe? Cek: actual fa-axe ada. So keep.
      // handle custom biar lebih aman (fontawesome 6 free punya fa-axe-battle? Tidak, tapi saya yakin 'fa-axe' ada di versi 6. tetap)
      if (weapon.icon === "fa-axe") iconHtml = `<i class="fas fa-axe-battle"></i>`; // fallback battle axe
      if (weapon.icon === "fa-bullseye") iconHtml = `<i class="fas fa-bullseye"></i>`;
      if (weapon.icon === "fa-sword") iconHtml = `<i class="fas fa-sword"></i>`;
      if (weapon.icon === "fa-gun") iconHtml = `<i class="fas fa-gun"></i>`;
      if (weapon.icon === "fa-bomb") iconHtml = `<i class="fas fa-bomb"></i>`;
      
      card.innerHTML = `
        <div class="product-icon">${iconHtml}</div>
        <div class="product-title">${weapon.name}</div>
        <div class="product-desc">${weapon.desc}</div>
        <div class="price">${formatRupiah(weapon.price)}</div>
        <button class="btn-add" data-id="${weapon.id}"><i class="fas fa-cart-plus"></i> Tambah ke Keranjang</button>
      `;
      productsGrid.appendChild(card);
    });

    // event delegation untuk tombol tambah (setelah render)
    document.querySelectorAll(".btn-add").forEach(btn => {
      btn.removeEventListener("click", addButtonHandler);
      btn.addEventListener("click", addButtonHandler);
    });
  }

  function addButtonHandler(e) {
    const btn = e.currentTarget;
    const id = parseInt(btn.getAttribute("data-id"));
    if (id) addToCart(id);
  }

  // Menambah ke keranjang
  function addToCart(productId) {
    const existing = cart.find(item => item.id === productId);
    if (existing) {
      existing.quantity += 1;
    } else {
      cart.push({ id: productId, quantity: 1 });
    }
    updateAllCartUI();
    saveCartToLocal();
    // animasi kecil feedback (opsional)
    showMiniToast(`+1 item ditambahkan`);
  }

  // Ubah quantity (delta = +1 / -1)
  function updateQuantity(productId, delta) {
    const itemIndex = cart.findIndex(item => item.id === productId);
    if (itemIndex === -1) return;
    const newQuantity = cart[itemIndex].quantity + delta;
    if (newQuantity <= 0) {
      // hapus item
      cart.splice(itemIndex, 1);
    } else {
      cart[itemIndex].quantity = newQuantity;
    }
    updateAllCartUI();
    saveCartToLocal();
  }

  // Hapus item langsung
  function removeItemFromCart(productId) {
    cart = cart.filter(item => item.id !== productId);
    updateAllCartUI();
    saveCartToLocal();
  }

  // Bersihkan semua item
  function clearCart() {
    cart = [];
    updateAllCartUI();
    saveCartToLocal();
    showMiniToast("Keranjang dikosongkan");
  }

  // Update UI keranjang & total items badge
  function updateAllCartUI() {
    renderCartItems();
    updateCartSummary();
    updateHeaderBadge();
  }

  function updateHeaderBadge() {
    const badgeSpan = document.getElementById("cartTotalItems");
    if (badgeSpan) badgeSpan.innerText = getTotalItemCount();
  }

  function updateCartSummary() {
    const totalPriceSpan = document.getElementById("cartTotalPrice");
    if (totalPriceSpan) totalPriceSpan.innerText = formatRupiah(getTotalCartPrice());
  }

  // render semua item di keranjang
  function renderCartItems() {
    const container = document.getElementById("cartItemsContainer");
    if (!container) return;
    if (cart.length === 0) {
      container.innerHTML = `<div class="empty-cart-msg"><i class="fas fa-box-open"></i> Keranjang kosong, tambah senjata dulu!</div>`;
      return;
    }

    let html = "";
    cart.forEach(item => {
      const product = getProductById(item.id);
      if (!product) return;
      const subtotal = product.price * item.quantity;
      html += `
        <div class="cart-item" data-id="${item.id}">
          <div class="cart-item-info">
            <div class="cart-item-title"><i class="fas ${product.icon}" style="font-size:0.75rem;"></i> ${product.name}</div>
            <div class="cart-item-price">${formatRupiah(product.price)} / pcs</div>
          </div>
          <div style="display: flex; align-items: center; gap: 8px;">
            <div class="cart-qty-control">
              <button class="cart-qty-dec" data-id="${item.id}">-</button>
              <span style="min-width: 28px; text-align:center;">${item.quantity}</span>
              <button class="cart-qty-inc" data-id="${item.id}">+</button>
            </div>
            <button class="cart-item-remove" data-id="${item.id}" title="Hapus item"><i class="fas fa-trash"></i></button>
          </div>
        </div>
      `;
    });
    container.innerHTML = html;

    // Attach event listeners untuk +/- dan hapus dalam keranjang (event delegation)
    container.querySelectorAll(".cart-qty-dec").forEach(btn => {
      btn.removeEventListener("click", decHandler);
      btn.addEventListener("click", decHandler);
    });
    container.querySelectorAll(".cart-qty-inc").forEach(btn => {
      btn.removeEventListener("click", incHandler);
      btn.addEventListener("click", incHandler);
    });
    container.querySelectorAll(".cart-item-remove").forEach(btn => {
      btn.removeEventListener("click", removeHandler);
      btn.addEventListener("click", removeHandler);
    });
  }

  function decHandler(e) {
    e.stopPropagation();
    const id = parseInt(e.currentTarget.getAttribute("data-id"));
    updateQuantity(id, -1);
  }
  function incHandler(e) {
    e.stopPropagation();
    const id = parseInt(e.currentTarget.getAttribute("data-id"));
    updateQuantity(id, 1);
  }
  function removeHandler(e) {
    e.stopPropagation();
    const id = parseInt(e.currentTarget.getAttribute("data-id"));
    removeItemFromCart(id);
  }

  // Format Rupiah
  function formatRupiah(angka) {
    return new Intl.NumberFormat("id-ID", { style: "currency", currency: "IDR", minimumFractionDigits: 0 }).format(angka);
  }

  // toast sederhana (alert atau floating)
  let toastTimeout;
  function showMiniToast(msg) {
    let existingToast = document.querySelector(".dynamic-toast");
    if (existingToast) existingToast.remove();
    const toast = document.createElement("div");
    toast.className = "dynamic-toast";
    toast.innerText = msg;
    toast.style.position = "fixed";
    toast.style.bottom = "20px";
    toast.style.left = "50%";
    toast.style.transform = "translateX(-50%)";
    toast.style.backgroundColor = "#1e1f2c";
    toast.style.color = "#facc15";
    toast.style.padding = "10px 24px";
    toast.style.borderRadius = "40px";
    toast.style.fontWeight = "600";
    toast.style.zIndex = "9999";
    toast.style.borderLeft = "4px solid #e63946";
    toast.style.fontSize = "0.9rem";
    toast.style.backdropFilter = "blur(8px)";
    toast.style.boxShadow = "0 8px 20px black";
    document.body.appendChild(toast);
    if (toastTimeout) clearTimeout(toastTimeout);
    toastTimeout = setTimeout(() => {
      if (toast) toast.remove();
    }, 1800);
  }

  // Checkout demo
  function handleCheckout() {
    if (cart.length === 0) {
      showMiniToast("Keranjang masih kosong, pilih senjata dulu!");
      return;
    }
    const total = getTotalCartPrice();
    const itemCount = getTotalItemCount();
    alert(`🛡️ SIMULASI PEMBELIAN 🛡️\n\nTerima kasih telah berbelanja di ARMS DECK.\nJumlah item: ${itemCount}\nTotal belanja: ${formatRupiah(total)}\n\n[Demo] Transaksi hanya simulasi jual beli senjata koleksi/replika. Tidak ada pengiriman nyata.`);
    showMiniToast("Proses checkout demo selesai!");
    // opsional bisa reset keranjang? tapi biarkan user memilih, tidak otomatis reset
    // lebih baik tidak reset agar pengguna merasa real, tapi boleh juga? Biar tidak mereset
    // tapi banyak e-commerce demo biasanya tetap, tapi untuk UX tidak kami reset.
  }

  // Inisialisasi dan load dari localStorage, render all
  function init() {
    loadCartFromLocal();
    renderProducts();
    renderCartItems();
    updateCartSummary();
    updateHeaderBadge();
    // event listener tombol checkout & clear
    const checkoutBtn = document.getElementById("checkoutBtn");
    if (checkoutBtn) checkoutBtn.addEventListener("click", handleCheckout);
    const clearBtn = document.getElementById("clearCartBtn");
    if (clearBtn) clearBtn.addEventListener("click", () => {
      clearCart();
      showMiniToast("Semua item dihapus");
    });
  }

  init();
</script>
</body>
</html>
