# Demo Application for BOSH Release

	$> cd ~/x-boshrelease
	$~/x-bosh-release> git submodule add https://github.com/making/hello-spring-boot src/demo
	$~/x-boshrelease> git submodule update --init --recursive
	$~/x-boshrelease> cd src/demo
	$~/x-boshrelease/src/demo> git checkout <tagname>
	$~/x-boshrelease/src/demo> ./mvnw clean package -Dmaven.test.skip=true
	$~/x-boshrelease/src/demo> cd ../..
	$~/x-boshrelease> bosh add blob src/demo/target/demo-0.0.1.RELEASE demo
