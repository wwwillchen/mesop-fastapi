# Mesop FastAPI Example

This example shows you how to use Mesop and FastAPI together.

The example has an HTTP endpoint `/hello` with FastAPI and a Mesop web component which fetches from the endpoint and displays the results in the UI.

## How to run

This project uses `uv` so you will need to [install it](https://docs.astral.sh/uv/#getting-started).

### Development mode

You can run it like this:

```sh
DEBUG_MODE=true uv run main.py
```

But if you're developing locally, you will most likely want to enable [auto-reloading](https://www.uvicorn.org/settings/#development) with `uvicorn`.

### Production mode

You can run it in production mode using the standard [`fastapi run`](https://fastapi.tiangolo.com/fastapi-cli/#fastapi-run) CLI command:

```sh
uv run fastapi run
```

> Note: `uv run` is just a wrapper to use the fastapi command with the uv virtual environment.

### Limitations

Right now Mesop hot reload doesn't work when running with the commands above. You can use the regular Mesop CLI command `mesop main.py` which supports hot reloading, but then the fastapi server isn't running. If you'd like this supported, please upvote: https://github.com/google/mesop/issues/894.