![alt tag](http://i.imgur.com/zUZfkhM.png)


####instalando Grunt no diretório do Projeto: 

```
npm install -g grunt-cli
```

####Criando o package.json no diretório: 

```
npm init
```

####Instalando Grunt localmente no diretório projeto:

```
npm install grunt --save-dev 
```

####Criando o arquivo Gruntfile.js:

	module.exports = function(grunt) {
	  "use strict";

	  var config;
	  config = {

	    imagemin: {
	      dynamic: {
	        files: [{
	          expand: true,
	          cwd: 'assets/img/',
	          src: ['**/*.{png,jpg,gif}'],
	          dest: 'images/'
	        }]
	      }
	    }
	  };

	  // Load the plugin that provides the "uglify" task.
	  grunt.initConfig(config);

	  // load tasks
	  grunt.loadNpmTasks('grunt-contrib-imagemin');
	  // grunt.loadNpmTasks('grunt-contrib-concat');
	  // grunt.loadNpmTasks('grunt-contrib-cssmin');

	  // Default task(s).
	  grunt.registerTask('tiny', ["imagemin"]);
	  // grunt.registerTask('mincss', ["cssmin"]);
	  // grunt.registerTask('conc', ["concat"]);
	  // grunt.registerTask('default', ['imagemin', 'concat', 'cssmin']);
	}; 


####Instalando a dependência imagemin
```
npm install grunt-contrib-imagemin --save-dev
```
----

Obs: o diretório 'node-modules' não precisa ser trackeado.