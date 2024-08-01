# carplugins {
    id 'java'
    id 'eclipse'
    id 'maven-publish'
}

group = 'com.example'
version = '1.0'
sourceCompatibility = '1.8'

repositories {
    maven {
        url = 'https://files.minecraftforge.net/maven'
    }
    mavenCentral()
}

dependencies {
    minecraft 'net.minecraftforge:forge:1.16.5-36.2.0'
}

minecraft {
    mappings channel: 'official', version: '1.16.5'
    runs {
        client {
            workingDirectory project.file('run')
        }
        server {
            workingDirectory project.file('run')
        }
    }
}
