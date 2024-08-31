## How Create a ZIP File for Your AWS Lambda Layer

1. Set up your environment:

    ```
    python -m venv lambda-env
    source lambda-env/bin/activate
    ```

2. Install Spotipy:

    `pip install spotipy`

3. Create the ZIP package:

    ```
    mkdir -p python
    cp -r lambda-env/lib/python3.*/site-packages/* python/
    zip -r spotipy-layer.zip python
    ```

4. Upload to AWS Lambda and configure!