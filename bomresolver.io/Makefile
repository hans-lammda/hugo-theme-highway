SITE=bomres

init: 
	hugo new site $(SITE)  
	( cd $(SITE) && git init )
	( cd $(SITE) && git submodule add  https://github.com/hans-lammda/hugo-theme-highway.git  themes/hugo-theme-highway  )


example: 
	( cd $(SITE)/themes/hugo-theme-highway/exampleSite && tar cvf - * | ( cd ../../.. && tar xvf - ))  
	cp config/config.toml $(SITE)/config.toml

build: 
	( cd $(SITE) && hugo  ) 

serv: 
	 ( cd $(SITE) &&  hugo server  )  

cycle: clean init example build 

clean: 
	rm -rf $(SITE)

