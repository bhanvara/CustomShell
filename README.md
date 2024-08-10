# CustomShell

- This shell is designed to work on Unix-based systems only.
- To run it, use the following commands:
    ```shell
    git clone https://github.com/bhanvara/CustomShell
    cd CustomShell
    gcc CustomShell.c -o CustomShell.out
    ./CustomShell.out
    ```

## Commands Usage

1. **`myinfo`**: Displays the username, OS name, and machine architecture.
2. **`cd <path>`**: Changes the current directory to the specified path (either relative or absolute). If no path is provided, it defaults to the home directory.
3. **`history`**: Lists the last 10 commands executed.
4. **`exit`**: Exits the shell.
5. **Complex Commands**: Supports commands with any valid number and combination of pipes, as well as input and output redirection.
    - **Note**: 
        - (i) For input/output redirection, the file names must follow the command arguments.
            - Example: `grep needle < haystack.txt`  ->  **VALID**
            - `grep < haystack.txt needle`  ->  **INVALID** (haystack.txt precedes needle argument)
        - (ii) Commands should be separated by spaces.
6. **Background Processes**: Execute commands in the background by appending `&` at the end. Example: `sleep 10 &`.
    - **Note**: 
        - (i) View the status of background processes with the `jobs` command.
        - (ii) Bring a background process to the foreground with `fg <job_id>`.
        - (iii) You cannot background a running foreground process.
7. **Standard UNIX Commands**: All other commands available in the standard UNIX shell are supported.

