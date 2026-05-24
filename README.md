# Create the base directory - First
sudo mkdir -p /opt/grouperContainer

# Create the config overlay directory
# (This mirrors the path inside the container)
mkdir -p /opt/grouperContainer/slashRoot/opt/grouper/grouperWebapp/WEB-INF/classes

# Create log directories for each service
mkdir -p /opt/grouperContainer/logs/grouper-ui-logs
mkdir -p /opt/grouperContainer/logs/grouper-ws-logs
mkdir -p /opt/grouperContainer/logs/grouper-daemon-logs

# Move into the working directory
cd /opt/grouperContainer


This the Tree :

/opt/grouperContainer/
├── compose.yaml                         ← orchestration file
├── logs/
│   ├── grouper-ui-logs/
│   ├── grouper-ws-logs/
│   └── grouper-daemon-logs/
└── slashRoot/
    └── opt/grouper/grouperWebapp/WEB-INF/classes/
        ├── grouper.properties            ← Grouper main config ( in my dev enviroment I do not have this one)
        ├── morphine.properties           ← Needed for encryption ( I will add my example)
        ├── grouper.hibernate.properties  ← Database connection
        └── subject.properties            ← Subject sources (LDAP etc.)


I am running Podman. Make the proper changes for your enviroment. This is a dev build.
