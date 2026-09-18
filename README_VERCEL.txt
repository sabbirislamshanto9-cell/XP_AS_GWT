# Vercel deployment

Upload these files to the same GitHub repository:

- `app.py`
- `MajoRLoGinrEs_pb2.py`  <-- required by app.py
- `requirements.txt`
- `vercel.json`
- `ob_version.txt` (optional; if omitted, the app uses OB55)

Vercel uses `app` from `app.py` as the Flask WSGI application.

Important:
`app.py` imports `MajoRLoGinrEs_pb2` (see the import near the top), so that file must be present in the repository or the deployment will fail with `ModuleNotFoundError`.

Deploy command is not required for Vercel's Git integration; connect the GitHub repo and deploy.
