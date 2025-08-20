# Legacy Docker Compose for Windows

The toolkit primarily uses shell scripts to orchestrate multiple Compose
fragments. On Windows, running these scripts can be inconvenient, so a
stand‑alone `docker-compose.legacy.yml` is provided as a simple alternative.

## Usage

1. Ensure Docker and Docker Compose v2 are installed.
2. Create `config/variables.env` with the desired settings.
3. Start the services:

   ```sh
   docker compose -f docker-compose.legacy.yml up -d
   ```

The containers store their data under the local `data/` directory. Feel free
to adjust paths and other environment variables via the `.env` file or the
`config/variables.env` file.

This compose file is intended for legacy deployments and is not actively
developed. For production deployments, prefer the toolkit shell scripts.
