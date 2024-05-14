# Printer Spooler Project

This is the project of our CSE 3707 Operating Systems course that implements a printer spooler system using shared memory and semaphores in C. It consists of two main components: a printer process (`printer.c`) and client processes (`client.c`).

## Printer Process (`printer.c`)

The printer process is responsible for managing printing jobs from clients. It operates as follows:

- It initializes shared memory and semaphores for communication with clients.
- Monitors the shared buffer for incoming print requests.
- Processes print requests from clients:
  - Prints the requested number of pages.
  - Logs printing activities to a file (`log.txt`).
- Sleeps when the buffer is empty.

## Client Process (`client.c`)

The client process represents users submitting printing jobs to the printer. Key features include:

- Accepts command-line arguments specifying client ID and number of pages to print.
- Communicates with the printer through shared memory and semaphores.
- Waits for an available spot in the buffer to submit print requests.
- Logs client actions and printing requests to `log.txt`.

## Compilation and Execution

This project includes a Makefile (`Makefile`) for easy compilation. Ensure you have `gcc` installed on your system.

### Using Makefile

To compile the project, navigate to the project directory and run the following command:
make


