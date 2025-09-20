<?php
include 'libs/lib.php';

// Xóa toàn bộ dữ liệu trong bảng
$result = $conn->query("DELETE FROM `$tabela`");

if ($result === TRUE) {
    $_SESSION['thanhcong'] = "Done";
    $_SESSION['icon'] = "success";
    $_SESSION['chu'] = "Đã xóa toàn bộ dữ liệu trong bảng!";
    header("Location: index.php");
    exit();
}
?>
