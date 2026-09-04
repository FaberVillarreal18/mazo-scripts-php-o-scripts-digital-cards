### 2. `docs/sanitizer.md`
```markdown
# Script para Sanitizar (Sanitizer)

## Propósito
Limpia y filtra los datos de entrada recibidos por formularios (métodos `POST` o `GET`) para prevenir ataques de inyección de código como **XSS** y **SQL Injection**.

## Código Fuente / Implementación
```php
class Sanitizer {
    public static function clean(string $data): string {
        $data = trim($data);
        $data = stripslashes($data);
        $data = htmlspecialchars($data, ENT_QUOTES, 'UTF-8');
        return $data;
    }
}
