<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Ghi chú bí mật</title>
</head>
<body>
  <h2>✍️ Ghi chú của tôi</h2>
  <textarea id="note" style="width:100%;height:200px;"></textarea>

  <script>
    const note = document.getElementById("note");

    // Lấy dữ liệu đã lưu trong LocalStorage
    note.value = localStorage.getItem("mySecretNote") || "";

    // Tự động lưu khi gõ
    note.addEventListener("input", () => {
      localStorage.setItem("mySecretNote", note.value);
    });
  </script>
</body>
</html>
