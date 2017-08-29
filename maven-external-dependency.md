	<dependencies>
		<dependency>
			<groupId>junit</groupId>
			<artifactId>junit</artifactId>
			<version>3.8.1</version>
			<scope>test</scope>
		</dependency>
		<dependency>
			<artifactId>demotest</artifactId>
			<groupId>test.mvndep</groupId>
			<version>0.0.1</version>
		</dependency>
	</dependencies>
	<build>
		<finalName>demo</finalName>

		<plugins>

			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-war-plugin</artifactId>
				<version>2.4</version>
				<configuration>
					<webResources>
						<resource>
							<directory>repo</directory>
							<targetPath>WEB-INF/lib</targetPath>
							<filtering>true</filtering>
							<includes>
								<include>**/*.jar</include>
							</includes>
						</resource>
					</webResources>
				</configuration>
			</plugin>
		</plugins>

	</build>
	<repositories>
		<repository>
			<id>repo</id>
			<url>${project.basedir}/repo</url>
		</repository>
	</repositories>
  
  
  
  
  	 mvn3 install:install-file -DlocalRepositoryPath=repo
	 * -DcreateChecksum=true -Dpackaging=jar -Dfile=repo/testmavendependency.jar
	 * -DgroupId=test.mvndep -DartifactId=demotest -Dversion=0.0.1
	 * 
	 * 
	 */
}
