# Bugs and solutions

## init error
1. Open your terminal.
2. Run the command:
   ```sh
   source /home/username/anaconda3/etc/profile.d/conda.sh
   ```
   This command tell the terminal to source the `conda.sh` file in the `etc/profile.d` directory of your Conda installation.
   Of note, replace `/home/username/anaconda3` with your own path of conda.
   To get that, you can run:
   ```sh
   which conda
   ```
    If the output is `/home/username/anaconda3/bin/conda`, then the root path should be `/home/username/anaconda3`.
3. Verify by activating an environment:
   ```sh
   conda activate myenv
    ```
   Replace `myenv` with the name of your environment.
   If the environment is activated successfully, then the issue is resolved.
   
If you want this setup to be persistent across all your terminal sessions, you can add the `source` command to your shell's startup file (`.bashrc`, `.zshrc`, etc.):

```sh
echo "source /home/username/anaconda3/etc/profile.d/conda.sh" >> ~/.bashrc
```

This ensures that every time you open a new terminal, the Conda environment is set up automatically.