<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ページを読み込んでいます...</title>
  <style>
    html, body {
      margin: 0; padding: 0;
      width: 100%; height: 100%;
      display: flex; flex-direction: column;
      justify-content: center; align-items: center;
      background: #fff;
      font-family: 'Noto Sans JP', Arial, sans-serif;
      color: #333; text-align: center;
    }
    .spinner {
      width: 40px; height: 40px;
      border: 4px solid #ddd;
      border-top: 4px solid #4653A1;
      border-radius: 50%;
      animation: spin 1s linear infinite;
      margin-bottom: 16px;
    }
    @keyframes spin {
      from { transform: rotate(0deg); }
      to { transform: rotate(360deg); }
    }
    p { font-size: 15px; line-height: 1.5; }
  </style>
</head>
<body>
  <div class="spinner"></div>
  <p>ページを読み込んでいます...<br>しばらくお待ちください。</p>
  <script>
    const url = new URL(window.location.href);
    const target = url.searchParams.get("to") || "https://diodigital.co.jp";
    setTimeout(() => {
      window.location.href = target;
    }, 800);
  </script>
</body>
</html>
