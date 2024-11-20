# Migrasi Database Mysql Ke PostgreSQL
1. Remove pgloader:
      ```sh
      apt remove pgloader -y
      ```
2. Clone the pgloader repository:
      ```sh
      git clone https://github.com/dimitri/pgloader.git
      ```
3. Install the necessary dependencies:
      ```sh
      sudo apt-get install sbcl unzip libsqlite3-dev make curl gawk freetds-dev libzip-dev
      ```
4. Navigate to the pgloader directory:
      ```sh
      cd /path/to/pgloader
      ```
5. Build pgloader:
      ```sh
      make pgloader
      ```
6. Verify the installation:
      ```sh
      ./build/bin/pgloader --help
      ```
7. Run pgloader to migrate from MySQL to PostgreSQL:
      ```sh
      ./build/bin/pgloader mysql://root:password@host:3307/database postgresql://postgres:password@host:5432/database
      ```

**Note:**

- Run these commands in the Ubuntu terminal. If you do not have the Ubuntu terminal on Windows, download it from the Microsoft Store using the keyword: "terminal Ubuntu 22.04.5 LTS".