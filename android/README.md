# Android / Visualizador IO

Esta carpeta contiene el payload reproducible del proyecto Android **Visualizador IO v1.2.0**.

## Compilación automática

El workflow `.github/workflows/build-apk.yml`:

1. Une `source.b64.001` ... `source.b64.017`.
2. Decodifica el archivo `tar.xz`.
3. Verifica SHA-256:
   `b2f685e32c168560aed64733ff8deb22bf3bff8684322b7bb21365c7c5685b7c`.
4. Reconstruye `VisualizadorIO_Android/`.
5. Compila con JDK 17, Gradle 8.9 y Android API 35.
6. Publica `VisualizadorIO-v1.2.0-debug.apk` como artifact de GitHub Actions.

El APK debug es instalable directamente y contiene tanto **Visualizador IO** como el módulo offline **Ing. Industrial**.

## Reconstrucción local del código

```bash
cat source.b64.[0-9][0-9][0-9] | tr -d '\r\n ' | base64 --decode > VisualizadorIO_v1_2_0.tar.xz
echo "b2f685e32c168560aed64733ff8deb22bf3bff8684322b7bb21365c7c5685b7c  VisualizadorIO_v1_2_0.tar.xz" | sha256sum -c -
tar -xJf VisualizadorIO_v1_2_0.tar.xz
```

Después puede abrirse `VisualizadorIO_Android` en Android Studio.
