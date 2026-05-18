Platica UAM

Configurar ventana de contexto
Los Modelfile de cada modelo ya están en el repositorio. Solo ejecuta los siguientes comandos para crear los modelos con una ventana de contexto de ~32k tokens:
bashollama create gemma4-e4b-32k -f Modelfile.gemma4-e4b
ollama create gemma4-26b-32k -f Modelfile.gemma4-26b
ollama create qwen3-27b-32k -f Modelfile.qwen3-27b




Evaluar velocidad de modelos
Ejecuta cualquiera de los siguientes comandos para medir el rendimiento de cada modelo:
bashollama run gemma4:e4b --verbose
ollama run gemma4:26b --verbose
ollama run qwen3:27b --verbose

Nota: Comparte el output completo de cada modelo. El resultado tendrá una forma similar a esta:

total duration:       29.956521233s
load duration:        526.192846ms
prompt eval count:    39 token(s)
prompt eval duration: 203.146953ms
prompt eval rate:     191.98 tokens/s
eval count:           762 token(s)
eval duration:        27.789827825s
eval rate:            27.42 tokens/s

Configurar OpenCode
Instalación
bashcurl -fsSL https://opencode.ai/install | bash
Configuración
Después de instalar, edita el archivo ~/.config/opencode/opencode.json y reemplaza su contenido con el del archivo opencode.json que se encuentra en este repositorio.

Probar OpenCode
1. En una terminal, inicia uno de los modelos de Ollama:
bashollama run <nombre-del-modelo>
2. En una segunda terminal, crea un directorio de prueba y lanza OpenCode:
bashcd ~/Documents
mkdir test_opencode
cd test_opencode
opencode
3. Dentro de la sesión de OpenCode:

Escribe /models y presiona Enter.
Se abrirá una lista de modelos disponibles selecciona el modelo de Ollama que está corriendo.
Ingresa el siguiente prompt:

Crea el código en Python para abrir un archivo CSV y devolver una lista
con el contenido de la primera columna. Asegúrate de crear un archivo
main.py el cual contiene únicamente la función.

Nota: Compartir si el modelo termino la tarea y escribio el archivo.
