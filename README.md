<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ИнструментАренда Курган — аренда строительного инструмента</title>
<meta name="description" content="Аренда строительного инструмента в Кургане. Перфораторы, пилы, генераторы, леса. Доставка по городу за 2 часа.">
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }
  body {
    font-family: 'Segoe UI', Arial, sans-serif;
    color: #1a1a1a;
    line-height: 1.6;
    background: #f5f6f8;
  }
  .container { max-width: 1200px; margin: 0 auto; padding: 0 20px; }

  /* Шапка */
  header {
    background: #1f2937;
    color: #fff;
    padding: 16px 0;
    position: sticky;
    top: 0;
    z-index: 100;
    box-shadow: 0 2px 10px rgba(0,0,0,0.2);
  }
  .header-inner {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 12px;
  }
  .logo { font-size: 22px; font-weight: 700; color: #fbbf24; }
  .logo span { color: #fff; }
  .logo small { display: block; font-size: 11px; color: #9ca3af; font-weight: 400; }
  nav a {
    color: #e5e7eb;
    text-decoration: none;
    margin-left: 22px;
    font-size: 15px;
    transition: color .2s;
  }
  nav a:hover { color: #fbbf24; }
  .phone { font-weight: 600; color: #fbbf24; }

  /* Герой */
  .hero {
    background: linear-gradient(135deg, #1f2937 0%, #374151 100%);
    color: #fff;
    padding: 70px 0;
    text-align: center;
  }
  .hero h1 { font-size: 42px; margin-bottom: 18px; line-height: 1.2; }
  .hero h1 span { color: #fbbf24; }
  .hero p { font-size: 18px; color: #d1d5db; max-width: 700px; margin: 0 auto 30px; }
  .btn {
    display: inline-block;
    background: #fbbf24;
    color: #1f2937;
    padding: 14px 32px;
    border-radius: 8px;
    text-decoration: none;
    font-weight: 700;
    font-size: 16px;
    border: none;
    cursor: pointer;
    transition: transform .2s, background .2s;
  }
  .btn:hover { background: #f59e0b; transform: translateY(-2px); }
  .btn-outline {
    background: transparent;
    border: 2px solid #fbbf24;
    color: #fbbf24;
    margin-left: 12px;
  }
  .btn-outline:hover { background: #fbbf24; color: #1f2937; }

  /* Преимущества */
  .features { padding: 60px 0; }
  .section-title {
    text-align: center;
    font-size: 32px;
    margin-bottom: 12px;
  }
  .section-sub {
    text-align: center;
    color: #6b7280;
    margin-bottom: 40px;
  }
  .features-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 24px;
  }
  .feature {
    background: #fff;
    padding: 28px 22px;
    border-radius: 12px;
    box-shadow: 0 4px 16px rgba(0,0,0,0.06);
    text-align: center;
  }
  .feature .icon { font-size: 36px; margin-bottom: 12px; }
  .feature h3 { font-size: 18px; margin-bottom: 8px; }
  .feature p { font-size: 14px; color: #6b7280; }

  /* Каталог */
  .catalog { padding: 20px 0 60px; }
  .filters {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    justify-content: center;
    margin-bottom: 30px;
  }
  .filter-btn {
    padding: 10px 20px;
    border: 2px solid #e5e7eb;
    background: #fff;
    border-radius: 30px;
    cursor: pointer;
    font-size: 14px;
    font-weight: 600;
    color: #4b5563;
    transition: all .2s;
  }
  .filter-btn:hover { border-color: #fbbf24; }
  .filter-btn.active {
    background: #fbbf24;
    border-color: #fbbf24;
    color: #1f2937;
  }
  .cards {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
    gap: 24px;
  }
  .card {
    background: #fff;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 4px 16px rgba(0,0,0,0.07);
    display: flex;
    flex-direction: column;
    transition: transform .2s, box-shadow .2s;
  }
  .card:hover {
    transform: translateY(-4px);
    box-shadow: 0 10px 28px rgba(0,0,0,0.12);
  }
  .card-img {
    height: 160px;
    background: #e5e7eb;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 60px;
  }
  .card-body { padding: 18px; flex: 1; display: flex; flex-direction: column; }
  .card-tag {
    display: inline-block;
    font-size: 12px;
    background: #fef3c7;
    color: #92400e;
    padding: 3px 10px;
    border-radius: 20px;
    margin-bottom: 8px;
    align-self: flex-start;
  }
  .card h3 { font-size: 17px; margin-bottom: 6px; }
  .card .desc { font-size: 13px; color: #6b7280; margin-bottom: 14px; flex: 1; }
  .card-footer {
    display: flex;
    align-items: center;
    justify-content: space-between;
    border-top: 1px solid #f3f4f6;
    padding-top: 12px;
  }
  .price { font-size: 20px; font-weight: 700; color: #1f2937; }
  .price small { font-size: 12px; font-weight: 400; color: #6b7280; }
  .rent-btn {
    background: #1f2937;
    color: #fff;
    border: none;
    padding: 8px 16px;
    border-radius: 6px;
    cursor: pointer;
    font-size: 13px;
    font-weight: 600;
    transition: background .2s;
  }
  .rent-btn:hover { background: #fbbf24; color: #1f2937; }

  /* Форма */
  .order { background: #1f2937; color: #fff; padding: 60px 0; }
  .order .section-title { color: #fff; }
  .order .section-sub { color: #9ca3af; }
  .form-wrap { max-width: 600px; margin: 0 auto; }
  .form-row { margin-bottom: 18px; }
  .form-row label {
    display: block;
    font-size: 14px;
    margin-bottom: 6px;
    color: #d1d5db;
  }
  .form-row input, .form-row select, .form-row textarea {
    width: 100%;
    padding: 12px 14px;
    border-radius: 8px;
    border: 2px solid #374151;
    background: #111827;
    color: #fff;
    font-size: 15px;
    font-family: inherit;
    outline: none;
    transition: border-color .2s;
  }
  .form-row input:focus, .form-row select:focus, .form-row textarea:focus {
    border-color: #fbbf24;
  }
  .form-row textarea { resize: vertical; min-height: 80px; }
  .form-wrap .btn { width: 100%; margin-top: 8px; }

  /* Подвал */
  footer {
    background: #111827;
    color: #9ca3af;
    padding: 40px 0 20px;
    font-size: 14px;
  }
  .footer-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 30px;
    margin-bottom: 30px;
  }
  .footer-grid h4 { color: #fff; margin-bottom: 12px; font-size: 16px; }
  .footer-grid p, .footer-grid a {
    color: #9ca3af;
    text-decoration: none;
    display: block;
    margin-bottom: 6px;
  }
  .footer-grid a:hover { color: #fbbf24; }
  .copy {
    text-align: center;
    border-top: 1px solid #1f2937;
    padding-top: 20px;
    font-size: 13px;
  }

  /* Уведомление */
  .toast {
    position: fixed;
    bottom: 30px;
    right: 30px;
    background: #10b981;
    color: #fff;
    padding: 16px 24px;
    border-radius: 10px;
    box-shadow: 0 8px 24px rgba(0,0,0,0.2);
    transform: translateY(150%);
    transition: transform .4s;
    z-index: 999;
    font-weight: 600;
  }
  .toast.show { transform: translateY(0); }

  @media (max-width: 640px) {
    .hero h1 { font-size: 30px; }
    nav { display: none; }
    .btn-outline { margin-left: 0; margin-top: 12px; }
  }
</style>
</head>
<body>

<header>
  <div class="container header-inner">
    <div class="logo">Инструмент<span>Аренда</span><small>г. Курган</small></div>
    <nav>
      <a href="#features">Преимущества</a>
      <a href="#catalog">Каталог</a>
      <a href="#order">Заявка</a>
    </nav>
    <div class="phone">📞 +7 (3522) 45-67-89</div>
  </div>
</header>

<section class="hero">
  <div class="container">
    <h1>Аренда строительного инструмента <span>в Кургане</span></h1>
    <p>Профессиональный инструмент от ведущих брендов. Выгоднее покупки — платите только за время работы. Доставка по Кургану и области.</p>
    <a href="#catalog" class="btn">Смотреть каталог</a>
    <a href="#order" class="btn btn-outline">Оставить заявку</a>
  </div>
</section>

<section class="features" id="features">
  <div class="container">
    <h2 class="section-title">Почему выбирают нас</h2>
    <p class="section-sub">Более 500 единиц инструмента в наличии в Кургане</p>
    <div class="features-grid">
      <div class="feature">
        <div class="icon">🚚</div>
        <h3>Доставка за 2 часа</h3>
        <p>Привезём инструмент прямо на объект в любом районе Кургана.</p>
      </div>
      <div class="feature">
        <div class="icon">🛠️</div>
        <h3>Проверенное качество</h3>
        <p>Инструмент Bosch, Makita, DeWalt проходит регулярное ТО.</p>
      </div>
      <div class="feature">
        <div class="icon">💳</div>
        <h3>Гибкая оплата</h3>
        <p>Аренда от суток. Скидки при заказе от 7 дней.</p>
      </div>
      <div class="feature">
        <div class="icon">📞</div>
        <h3>Поддержка 24/7</h3>
        <p>Поможем подобрать инструмент под вашу задачу.</p>
      </div>
    </div>
  </div>
</section>

<section class="catalog" id="catalog">
  <div class="container">
    <h2 class="section-title">Каталог инструмента</h2>
    <p class="section-sub">Цены указаны за сутки аренды, самовывоз в Кургане</p>

    <div class="filters">
      <button class="filter-btn active" data-filter="all">Все</button>
      <button class="filter-btn" data-filter="electric">Электроинструмент</button>
      <button class="filter-btn" data-filter="power">Силовая техника</button>
      <button class="filter-btn" data-filter="measure">Измерительный</button>
      <button class="filter-btn" data-filter="other">Прочее</button>
    </div>

    <div class="cards" id="cards">

      <div class="card" data-category="electric">
        <div class="card-img">🔩</div>
        <div class="card-body">
          <span class="card-tag">Электроинструмент</span>
          <h3>Перфоратор Bosch GBH 2-26</h3>
          <p class="desc">Мощность 800 Вт. Для бетона, кирпича и камня. В комплекте буры.</p>
          <div class="card-footer">
            <div class="price">800 ₽ <small>/ сутки</small></div>
            <button class="rent-btn" data-tool="Перфоратор Bosch GBH 2-26">Арендовать</button>
          </div>
        </div>
      </div>

      <div class="card" data-category="electric">
        <div class="card-img">🪚</div>
        <div class="card-body">
          <span class="card-tag">Электроинструмент</span>
          <h3>Циркулярная пила Makita</h3>
          <p class="desc">Диск 190 мм, плавная регулировка глубины пропила. Для дерева.</p>
          <div class="card-footer">
            <div class="price">700 ₽ <small>/ сутки</small></div>
            <button class="rent-btn" data-tool="Циркулярная пила Makita">Арендовать</button>
          </div>
        </div>
      </div>

      <div class="card" data-category="electric">
        <div class="card-img">🔧</div>
        <div class="card-body">
          <span class="card-tag">Электроинструмент</span>
          <h3>УШМ (болгарка) DeWalt 125</h3>
          <p class="desc">Мощность 1400 Вт, диаметр диска 125 мм. Резка металла и камня.</p>
          <div class="card-footer">
            <div class="price">450 ₽ <small>/ сутки</small></div>
            <button class="rent-btn" data-tool="УШМ DeWalt 125">Арендовать</button>
          </div>
        </div>
      </div>

      <div class="card" data-category="power">
        <div class="card-img">⚡</div>
        <div class="card-body">
          <span class="card-tag">Силовая техника</span>
          <h3>Бензогенератор 5 кВт</h3>
          <p class="desc">Автономное электроснабжение на объекте. Расход топлива 2,5 л/ч.</p>
          <div class="card-footer">
            <div class="price">1500 ₽ <small>/ сутки</small></div>
            <button class="rent-btn" data-tool="Бензогенератор 5 кВт">Арендовать</button>
          </div>
        </div>
      </div>

      <div class="card" data-category="power">
        <div class="card-img">🔨</div>
        <div class="card-body">
          <span class="card-tag">Силовая техника</span>
          <h3>Отбойный молоток Bosch</h3>
          <p class="desc">Электрический, 1500 Вт. Для демонтажных работ и сноса.</p>
          <div class="card-footer">
            <div class="price">1200 ₽ <small>/ сутки</small></div>
            <button class="rent-btn" data-tool="Отбойный молоток Bosch">Арендовать</button>
          </div>
        </div>
      </div>

      <div class="card" data-category="measure">
        <div class="card-img">📏</div>
        <div class="card-body">
          <span class="card-tag">Измерительный</span>
          <h3>Лазерный нивелир</h3>
          <p class="desc">Построение горизонтальных и вертикальных плоскостей. Дальность 30 м.</p>
          <div class="card-footer">
            <div class="price">600 ₽ <small>/ сутки</small></div>
            <button class="rent-btn" data-tool="Лазерный нивелир">Арендовать</button>
          </div>
        </div>
      </div>

      <div class="card" data-category="measure">
        <div class="card-img">🌡️</div>
        <div class="card-body">
          <span class="card-tag">Измерительный</span>
          <h3>Тепловизор</h3>
          <p class="desc">Поиск утечек тепла, диагностика электрики. Разрешение 220×160.</p>
          <div class="card-footer">
            <div class="price">1000 ₽ <small>/ сутки</small></div>
            <button class="rent-btn" data-tool="Тепловизор">Арендовать</button>
          </div>
        </div>
      </div>

      <div class="card" data-category="other">
        <div class="card-img">🪜</div>
        <div class="card-body">
          <span class="card-tag">Прочее</span>
          <h3>Строительные леса</h3>
          <p class="desc">Комплект 2×6 м с настилом. Оцинкованная сталь, устойчивые.</p>
          <div class="card-footer">
            <div class="price">900 ₽ <small>/ сутки</small></div>
            <button class="rent-btn" data-tool="Строительные леса">Арендовать</button>
          </div>
        </div>
      </div>

      <div class="card" data-category="other">
        <div class="card-img">🛞</div>
        <div class="card-body">
          <span class="card-tag">Прочее</span>
          <h3>Виброплита бензиновая</h3>
          <p class="desc">Уплотнение грунта и асфальта. Вес 80 кг, двигатель 5,5 л.с.</p>
          <div class="card-footer">
            <div class="price">1100 ₽ <small>/ сутки</small></div>
            <button class="rent-btn" data-tool="Виброплита бензиновая">Арендовать</button>
          </div>
        </div>
      </div>

    </div>
  </div>
</section>

<section class="order" id="order">
  <div class="container">
    <h2 class="section-title">Оставить заявку</h2>
    <p class="section-sub">Перезвоним в течение 15 минут и уточним детали</p>
    <div class="form-wrap">
      <form id="orderForm">
        <div class="form-row">
          <label for="name">Ваше имя *</label>
          <input type="text" id="name" required placeholder="Иван">
        </div>
        <div class="form-row">
          <label for="phone">Телефон *</label>
          <input type="tel" id="phone" required placeholder="+7 (3522) ___-__-__">
        </div>
        <div class="form-row">
          <label for="tool">Инструмент</label>
          <input type="text" id="tool" placeholder="Например: Перфоратор Bosch">
        </div>
        <div class="form-row">
          <label for="period">Срок аренды</label>
          <select id="period">
            <option>1 сутки</option>
            <option>2–3 суток</option>
            <option>до 7 суток</option>
            <option>более 7 суток</option>
          </select>
        </div>
        <div class="form-row">
          <label for="comment">Комментарий</label>
          <textarea id="comment" placeholder="Адрес доставки в Кургане, пожелания..."></textarea>
        </div>
        <button type="submit" class="btn">Отправить заявку</button>
      </form>
    </div>
  </div>
</section>

<footer>
  <div class="container">
    <div class="footer-grid">
      <div>
        <h4>ИнструментАренда Курган</h4>
        <p>Профессиональный инструмент в аренду с доставкой по Кургану и Курганской области.</p>
      </div>
      <div>
        <h4>Контакты</h4>
        <p>📞 +7 (3522) 45-67-89</p>
        <p>✉️ info@instrument-rent45.ru</p>
        <p>📍 г. Курган, ул. Куйбышева, 25</p>
      </div>
      <div>
        <h4>Режим работы</h4>
        <p>Пн–Пт: 8:00 – 20:00</p>
        <p>Сб–Вс: 9:00 – 18:00</p>
        <p>Выдача инструмента — ежедневно</p>
      </div>
    </div>
    <div class="copy">© 2026 ИнструментАренда Курган. Все права защищены.</div>
  </div>
</footer>

<div class="toast" id="toast">Заявка отправлена! Мы вам перезвоним.</div>

<script>
  // Фильтрация каталога
  const filterBtns = document.querySelectorAll('.filter-btn');
  const cards = document.querySelectorAll('.card');

  filterBtns.forEach(btn => {
    btn.addEventListener('click', () => {
      filterBtns.forEach(b => b.classList.remove('active'));
      btn.classList.add('active');
      const filter = btn.dataset.filter;
      cards.forEach(card => {
        if (filter === 'all' || card.dataset.category === filter) {
          card.style.display = 'flex';
        } else {
          card.style.display = 'none';
        }
      });
    });
  });

  // Кнопка "Арендовать" — подставляет инструмент в форму
  const toolInput = document.getElementById('tool');
  document.querySelectorAll('.rent-btn').forEach(btn => {
    btn.addEventListener('click', () => {
      toolInput.value = btn.dataset.tool;
      document.getElementById('order').scrollIntoView({ behavior: 'smooth' });
      document.getElementById('name').focus();
    });
  });

  // Отправка формы
  const toast = document.getElementById('toast');
  document.getElementById('orderForm').addEventListener('submit', e => {
    e.preventDefault();
    toast.classList.add('show');
    setTimeout(() => toast.classList.remove('show'), 4000);
    e.target.reset();
  });
</script>

</body>
</html>
