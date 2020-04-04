# Creating a builder

As an example, let's create a builder that executes a shell command. To create a builder, use the createBuilder() CLI Builder function, and return a Promise<BuilderOutput> object. Logic will be listed in the command/index.ts (builder skeleton)

# A Builder project structure

```

 FILES	                      PURPOSE
src/index.ts	        Main source file for the builder definition.
src/index.spec.ts	    Source file for tests.
src/schema.json	        Definition of builder input options.
builders.json	        Which has implementation and schema definition 
package.json	        Dependencies. See https://docs.npmjs.com/files/package.json.
tsconfig.json	        TypeScript configuration. 

```
