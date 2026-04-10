# First Workflow

```yml
name: First Workflow
on:
  workflow_dispatch:

jobs:
  job-print-hello-world:
    runs-on: ubuntu-latest
    steps:
      - name: Print Hello World
        run: echo "Hello, World!"
```

1. Workflow Name

   ```yml
   name: First Workflow
   ```

2. Trigger (on)

   ```yml
   on:
     workflow_dispatch:
   ```

   - `on:` defines when workflow runs.
   - `workflow_dispatch` means you trigger it manually from GitHub UI.
   - It will not run automatically

3. Job Section

   ```yml
   jobs:
     job-print-hello-world:
   ```

   - `jobs:` Section where you define all of your jobs/work you do.
   - `job-print-hello-world` this is one of the job you defined. You can define multiple jobs.

4. Runner Environment

   ```yml
   runs-on: ubuntu-latest
   ```

   - This specifies the virtual environment where job will actually executes
   - GitHub provides managed runners like: Ubuntu, Windows, macOS

5. Steps
   ```yml
   steps:
     - name: Print Hello World
       run: echo "Hello, World!"
   ```
   - Sequence of commands that get's executed
   - `- name: Print Hello World`: Labelling the step
   - `run: echo "Hello, World!"`: Actual shell command that runs

## How it Works

- You go to your repository's Actions tab on GitHub
- Select "First Workflow" from the left sidebar
- Click the "Run workflow" button
- GitHub spins up a fresh Ubuntu virtual machine
- The VM executes echo "Hello, World!" in the terminal
- You see the output in the workflow logs
