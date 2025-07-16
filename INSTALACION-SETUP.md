# 🔧 INSTALACIÓN Y SETUP - Framework Revolution v5.0

## 🚀 PREREQUISITOS

### Sistemas Compatibles
- **macOS**: 10.15+ (Recomendado)
- **Linux**: Ubuntu 20.04+, CentOS 8+
- **Windows**: 10/11 con WSL2

### Herramientas Requeridas
- **Node.js**: v16+ 
- **npm**: v8+
- **Git**: v2.30+
- **Claude API Key**: Anthropic

## 📦 INSTALACIÓN CLAUDE CLI

### Método 1: Instalación Oficial (Recomendado)

```bash
# Instalar Claude CLI oficial
npm install -g @anthropic-ai/claude-cli

# Verificar instalación
claude --version

# Autenticación
claude auth login
```

### Método 2: Wrapper Alternativo

```bash
# Crear directorio local
mkdir -p ~/.local/bin

# Instalar paquete alternativo
npm install -g claude-ai

# Crear wrapper script
cat > ~/.local/bin/claude << 'EOF'
#!/bin/bash
node $(npm root -g)/claude-ai/index.js "$@"
EOF

# Permisos ejecutable
chmod +x ~/.local/bin/claude

# Añadir al PATH
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

## 🔑 CONFIGURACIÓN API

### Variables Entorno

```bash
# Para Bash
echo 'export ANTHROPIC_API_KEY="your-api-key-here"' >> ~/.bashrc
source ~/.bashrc

# Para Zsh
echo 'export ANTHROPIC_API_KEY="your-api-key-here"' >> ~/.zshrc
source ~/.zshrc

# Verificar configuración
echo $ANTHROPIC_API_KEY
```

---

**Framework Revolution v5.0** - Instalación y Setup Completo
*Token-Optimized Superintelligence System*
*Implementación Enterprise Ready - Julio 2025*