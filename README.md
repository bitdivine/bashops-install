# bashops-install
Simple bash installers for devops

 * Write FAST installers
 * Make the installers _idenpotent_, which means that you can re-run them over and over again
 


## Analysis of an installer:

	. bashops/install  <-------------------------- Load the 'install' function.
	. bashops/install/node

	my_installer(){
	(  <------------------------------------------ The installer should run in an isolated subshell
		check(){ is my thing installed? }  <-- Make a small, fast check
		get(){ install it }  <---------------- Make this robust.
		install "my thing"   <---------------- Fire off the installation
	)
	}

