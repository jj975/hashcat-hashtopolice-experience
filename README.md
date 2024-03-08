# hashcat-hashtopolice-experience

### hashtopolis Docker Installation Guide:

1. **Clone the hashtopolis Repository:**
   ```bash
   git clone https://github.com/hashtopolis/server.git
   cd server
   ```

2. **Configure hashtopolis:**
   Update the configuration file (`config.php`) with your desired settings.

3. **Build and Run hashtopolis Docker Containers:**
   ```bash
   docker-compose up -d
   ```

4. **Access hashtopolis Web Interface:**
   Open a web browser and navigate to `http://localhost:80` (or your specified port) to access the hashtopolis web interface.

### Adding Agents:

1. **Download Agent Files:**
   On the hashtopolis web interface, go to "Agent" -> "Downloads" and download the agent files.

2. **Deploy Agent:**
   Extract the downloaded agent files on the machine you want to use as an agent. Follow the instructions in the agent's README for your specific operating system.

3. **Configure Agent:**
   Edit the agent's configuration file to specify the hashtopolis server's address and port.

4. **Run Agent:**
   Execute the agent binary on the machine.

### hashcat Installation:

1. **Install hashcat:**
   Follow the official hashcat installation guide: [hashcat Installation](https://hashcat.net/wiki/doku.php?id=hashcat)

2. **Verify hashcat Installation:**
   Ensure hashcat is correctly installed by running:
   ```bash
   hashcat --version
   ```

### Using hashtopolis with hashcat:

1. **Configure hashtopolis for hashcat:**
   On the hashtopolis web interface, go to "Settings" -> "Hashcat" and set the path to your hashcat binary.

2. **Create a Task:**
   - Go to "Tasks" -> "New Task" on the hashtopolis web interface.
   - Set the hash type and specify the target hash file.

3. **Add Agents to Task:**
   - Select the agents you want to assign to the task.
   - Configure other task settings as needed.

4. **Start Task:**
   Click on "Start" to begin the password cracking task.

### Example Commands:

- Running hashcat manually:
  ```bash
  hashcat -m <hash_mode> -a <attack_mode> <hash_file> <wordlist>
  ```

- Check hashtopolis server logs:
  ```bash
  docker-compose logs -f
  ```
