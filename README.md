# PyTorch CUDA DevContainer Template

<a href="https://github.com/mabryuk/miniCUDA/generate">
  <img src="https://img.shields.io/badge/use%20this-template-blue?logo=github">
</a>

This repository provides a template for setting up a development container (DevContainer) for working with PyTorch on CUDA. This setup ensures a consistent development environment, making it easier to manage dependencies and configurations.

## Features

- [**MiniForge3**](https://hub.docker.com/r/condaforge/miniforge3/tags): A minimal distribution with miniforge3, same as anaconda but with conda-forge as the default channel.

## Getting Started

### Prerequisites

- **Docker**: Ensure Docker is installed and running on your machine [from here](https://docs.docker.com/engine/install/) or [here](https://docs.docker.com/desktop/).
- **Visual Studio Code**: Install [Visual Studio Code](https://code.visualstudio.com/Download) then the [Remote Development extension pack](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack) for VS Code.

### Setup

1. **Open** `.devcontainer/devcontainer.json`

2. **Rename the container**:
    ```json
    "name": "YOUR_CONTAINER_NAME"
    ```

3. **Choose python version**:
    ```json
    "containerEnv": { 
		"PYTHON_VERSION": "3.11"
	}
    ```

4. **Reopen in Container**:
    - Press `F1` and select `Remote-Containers: Reopen in Container`.
    - VS Code will build the container and open the workspace inside it.

### Usage

1. **Activate Conda Environment**:
    ```bash
    conda activate base
    ```
2. **Test PyTorch Installation**:

    `main.py`:
    ```python
    import torch
    print(torch.__version__)
    print(torch.cuda.is_available())
    ```
    Run the script:
    ```bash
    python main.py
    ```
3. **Run export script to save the installed modules**:
    
    ```bash
    .devcontainer/scripts/export.sh
    ```

## Contributing

Feel free to submit issues or pull requests if you have suggestions for improvements or find any bugs.

## License

This project is licensed under the MIT License.