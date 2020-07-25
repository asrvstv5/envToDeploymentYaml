# envToDeploymentYaml
Python Script to convert .env files to a deployment yaml

## How to Install

With the latest version of pip installed, simply perform the following : <br>
`pip install envyamlconverter=0.1 `

## How to Use 

### Pre-requisites
<ul>
  <li>You need a .env file with the environment variables you wish to use for your k8s deployment</li>
  <li>You need python installed</li>
</ul>

### Code
In your code do the following : <br>
Step 1 : `import envyamlconverter` <br>
Step 2: `converter = envyamlconverter.envYamlConverter(<k8s app name>, <k8s namespace>, <k8s secrets file name>, <file path to .env file>, <image pull secrets name>, <dockerImagePath>)` <br>
Step 3: `converter.convertEnv(<list of env vars that have secrets as values>)` <br>
<hr>
 e.g. <br>

`import envyamlconverter`<br>
`converter = envyamlconverter.envYamlConverter('myapp', 'mynamespace', 'mysecrets', 'my.env', 'foo', 'http://imageUrl:1.3')`<br>
`converter.convertEnv(['DUMMY_ENV_NAME_1', 'DUMMY_ENV_NAME_2'])`<br>
