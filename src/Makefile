#-------------------------------------------------------------------------------

#PLUGINJAR=/usr/lib/jvm/java-6-sun-1.6.0.26/jre/lib/plugin.jar
PLUGINJAR=/usr/share/icedtea-web/plugin.jar

.PHONY: all run classes clean

#-------------------------------------------------------------------------------

all: circuit.jar

clean:
	rm -f *.class circuit.jar

run: circuit.jar
	java Circuit

classes:
	javac -classpath $(PLUGINJAR):. *.java

#-------------------------------------------------------------------------------

circuit.jar: classes
	jar cfm circuit.jar Manifest.txt *.class *.txt circuits/
	-rm ../circuit.jar
	cp circuit.jar ../circuit.jar

#-------------------------------------------------------------------------------
