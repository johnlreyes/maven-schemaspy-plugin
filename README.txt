fork of https://github.com/wakaleo/maven-schemaspy-plugin

added support for excluding tables and graphviz folder installation

for usage instruction, see:
https://github.com/wakaleo/maven-schemaspy-plugin/blob/master/src/site/apt/usage.apt

for this fork, you can:

	<groupId>com.wakaleo.schemaspy</groupId>
	<artifactId>maven-schemaspy-plugin</artifactId>
	<version>5.0.4-SNAPSHOT</version>
	<configuration>
		...
		<graphvizDir>C:/Program Files/Graphviz 2.28/</graphvizDir>
		<excludeTableNamesRegex>(databasechangelog)|(databasechangeloglock)</excludeTableNamesRegex>                                
	</configuration>

and

	<pluginRepositories>
		<pluginRepository>
			<id>maven-schema-spy-fork-repo</id>
			<url>https://github.com/johnlreyes/maven-schemaspy-plugin/raw/master/maven-repository/snapshots</url>   
		</pluginRepository>
	</pluginRepositories>

well that was the motivation in forking, i wanted to exclude liquibase generated table and specify absolute path of graphviz