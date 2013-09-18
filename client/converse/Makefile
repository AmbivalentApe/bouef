
CONVERSE_VERSION=0.6.3


deps: npm_dep grunt_dep

npm_dep:
	cd converse.js-${CONVERSE_VERSION} && npm install;

grunt_dep:
	cd converse.js-${CONVERSE_VERSION} && grunt fetch;

minimise_css: deps
	cd converse.js-${CONVERSE_VERSION} && grunt cssmin;
	
minimise_js: deps
	cd converse.js-${CONVERSE_VERSION} && make release;

build: minimise_js minimise_css
	mkdir deploy && cp converse.js-${CONVERSE_VERSION}/converse.min.js deploy && cp converse.js-${CONVERSE_VERSION}/converse.min.css deploy
