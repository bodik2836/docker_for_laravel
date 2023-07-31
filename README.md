## Instruction

### Step 1

Create your project directory and go to it from console. \
Example: \
mkdir proj_name \
cd proj_name

### Step 2

Clone docker repository. \
git clone git@github.com:bodik2836/docker_for_laravel.git .

### Step 3

Remove .git directory and run "git init" if you need. \
rm -rf .git \
rm www/.gitkeep

### Step 4

Replace all occurrences "proj_name" of the word with "yourproj" in nginx/conf.d/default.conf file.

### Step 5

Do same from step 4 for .env file. \
In .env file uncomment necessary versions of services.

### Step 6

docker-compose -f docker-compose.yml -p proj_name up -d \
docker-compose -f docker-compose.yml -p proj_name down (command for stop containers)

### Step 7

Go to container and create your project. \
docker exec -it proj_name_php sh
