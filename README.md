# EduTrack API

API REST desarrollada con Flask y scikit-learn para la inferencia del modelo predictivo del proyecto **EduTrack**, entrenado con datos del DANE.

## 📋 Requisitos
- Python 3.9+
- Dependencias especificadas en `requirements.txt`

## 🚀 Instalación y Ejecución Local

1. **Crear y activar un entorno virtual**:
   ```bash
   python -m venv venv
   # En Windows:
   venv\Scripts\activate
   # En Linux/macOS:
   source venv/bin/activate
   ```

2. **Instalar dependencias**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Ejecutar la API**:
   ```bash
   python app.py
   ```
   El servidor estará disponible en `http://localhost:5000`.

## 📡 Endpoints

### `POST /predecir`
Recibe los datos y características de la institución educativa y calcula la probabilidad predicha por el modelo.

#### Body (JSON)
```json
{
  "matricula": 500,
  "docentes": 25,
  "orientadores": 2,
  "niveles": 3,
  "jornadas": 1,
  "zona": "rural",
  "bilingue": "no",
  "etno": "no"
}
```

#### Respuesta (JSON)
```json
{
  "probabilidad": 0.42
}
```
