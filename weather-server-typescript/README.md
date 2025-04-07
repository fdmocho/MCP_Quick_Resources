# A Simple MCP weather Server written in TypeScript

See the [Quickstart](https://modelcontextprotocol.io/quickstart) tutorial for more information.


## Weather client

_add mcp index.js build to your mcpserver folder_ 

```bash
./weather-server-typescript/weather/build/index.js
```
### **Example** for Claude Desktop:

```json
{
    "mcpServers": {
        "weather": {
            "command": "node",
            "args": [
                "C:\\PATH\\TO\\PARENT\\FOLDER\\weather\\build\\index.js"
            ]
        }
    }
}
```


**Tools**
- get-alerts
- get-forecast

**Build**

- _windows_
```bash
npm run buildwin
```
- _linux_
```bash
npm run build
```


### **HOW TO**:


```bash
# Create a new directory for our project
md weather
cd weather

# Initialize a new npm project
npm init -y

# Install dependencies
npm install @modelcontextprotocol/sdk zod
npm install -D @types/node typescript

# Create our files
md src
new-item src\index.ts
```

**package.json**
```JSON
{
  "type": "module",
  "bin": {
    "weather": "./build/index.js"
  },
  "scripts": {
    "build": "tsc && chmod 755 build/index.js"
  },
  "files": [
    "build"
  ],
}
```

**tsconfig.json**

```JSON
{
  "compilerOptions": {
    "target": "ES2022",
    "module": "Node16",
    "moduleResolution": "Node16",
    "outDir": "./build",
    "rootDir": "./src",
    "strict": true,
    "esModuleInterop": true,
    "skipLibCheck": true,
    "forceConsistentCasingInFileNames": true
  },
  "include": ["src/**/*"],
  "exclude": ["node_modules"]
}
```