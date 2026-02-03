
![on-push](../../actions/workflows/on-push.yaml/badge.svg)
![on-pull-request](../../actions/workflows/on-pull-request.yaml/badge.svg)
![on-schedule](../../actions/workflows/on-schedule.yaml/badge.svg)

# yujiaen1999's Website

- **Website:** [yujiaen1999.github.io/ddl-lab](https://yujiaen1999.github.io/ddl-lab)
- **Built with:** [Lab Website Template](https://greene-lab.gitbook.io/lab-website-template-docs)

## Preview Locally

### Prerequisites

- **Docker Desktop** installed and running
  - Download from [docker.com](https://www.docker.com/products/docker-desktop)
  - Verify Docker is running before proceeding

### Run the Preview

```bash
./.docker/run.sh
```

- **First run:** Takes ~2 minutes to build the Docker image
- **Subsequent runs:** Nearly instant (uses cached image)
- **Access:** Open `http://localhost:4000` in your browser

### Development Features

- **Auto-reload:** File changes automatically refresh the preview
- **Config changes:** Modifications to `_config.yaml` require manual browser refresh
- **Citations:** Auto-regenerate when source files change

### Troubleshooting

**If you encounter build errors or the site doesn't update:**

1. **Clear Docker cache and rebuild:**
   ```bash
   docker rmi lab-website-renderer:latest
   ./.docker/run.sh
   ```

2. **Stop running containers:**
   ```bash
   docker stop lab-website-renderer
   ./.docker/run.sh
   ```

3. **Full Docker cleanup** (if issues persist):
   ```bash
   docker system prune -a
   ./.docker/run.sh
   ```

### Manual Setup (Without Docker)

<details>
<summary>Click to expand manual setup instructions</summary>

**Build the site:**
1. Install Ruby 3+
2. Run `gem install bundler`
3. Run `bundle install`
4. Start server: `bundle exec jekyll serve --open-url --livereload --trace`
5. Access at `http://localhost:4000`

**Run citation process:**
1. Install Python 3 with pip
2. Run `python -m pip install --upgrade --requirement ./_cite/requirements.txt`
3. Generate citations: `python ./_cite/cite.py`

Note: Rerun Jekyll if you add new plugins or modify `_config.yaml`

</details>

---

For more details, see the [Lab Website Template documentation](https://greene-lab.gitbook.io/lab-website-template-docs/getting-started/preview-your-site).
