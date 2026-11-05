# agent-bench-dash

Data for the [agent-bench](https://github.com/Jayanaka-98/agent-bench) run dashboard.

Each machine running agent-bench writes one file under `machines/`: its runs, sealed with
AES-256-GCM under a key that only holders of the dashboard link have. File names are keyed
hashes of machine names. Nothing here is readable without that key; the dashboard page
decrypts in the browser, and the key (after `#` in the link) is never sent to a server.

Written by `agent-bench dash publish`. History is squashed periodically.
