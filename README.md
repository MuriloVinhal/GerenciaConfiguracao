# 🚀 Gerência de Configuração de Software

Este repositório demonstra a aplicação de conceitos de Gerência de Configuração de Software (GCS), incluindo controle de versão, uso de branches e commits. O projeto contém um código simples em Java e segue boas práticas no uso do Git.

---

## 📝 Histórico de Versões

- **Versão 1**: Código inicial do HelloWorld.
- **Versão 2**: Melhorada a saída do HelloWorld.
- **Nova funcionalidade**: Criada em uma branch separada.

---

## 🛠️ **Passos Realizados**

### 🔹 1. Inicialização do Repositório e Configuração Remota
Inicializamos um repositório Git localmente e o vinculamos ao GitHub:

```sh
git init
git remote add origin git@github.com:MuriloVinhal/GerenciaConfiguracao.git
```

Verificamos a branch principal e ajustamos, se necessário:

```sh
git branch -M main
```

---

### 🔹 2. Criando o Código Inicial e Primeiro Commit

Criamos o arquivo `HelloWorld.java`:

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, Git Repository!");
    }
}
```

Adicionamos e realizamos o primeiro commit:

```sh
git add HelloWorld.java
git commit -m "Versão 1: Código inicial do HelloWorld"
git push origin main
```

---

### 🔹 3. Modificando o Código e Criando a Segunda Versão

Editamos o `HelloWorld.java` para melhorar a saída:

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, Git Repository! Versão 2 com melhorias.");
    }
}
```

Realizamos o commit e enviamos as mudanças:

```sh
git add HelloWorld.java
git commit -m "Versão 2: Melhorando a saída do HelloWorld"
git push origin main
```

---

### 🔹 4. Criando uma Nova Branch para uma Nova Funcionalidade

Criamos e mudamos para uma nova branch chamada `nova-feature`:

```sh
git checkout -b nova-feature
```

Criamos um novo arquivo `Feature.java` com uma funcionalidade adicional:

```java
public class Feature {
    public static void printFeature() {
        System.out.println("Nova funcionalidade adicionada!");
    }
}
```

Fizemos o commit e enviamos para a branch `nova-feature`:

```sh
git add Feature.java
git commit -m "Nova funcionalidade: Adiciona classe Feature"
git push origin nova-feature
```

---

### 🔹 5. Criando o Arquivo de Documentação `README.md`

Criamos e adicionamos um `README.md` para documentar o projeto:

```sh
echo "# HelloWorld - Gerência de Configuração

## Histórico de versões:
- **Versão 1**: Código inicial do HelloWorld.
- **Versão 2**: Melhorada a saída do HelloWorld.
- **Nova funcionalidade**: Criada em uma branch separada.

## Como executar o projeto:
```sh
javac HelloWorld.java && java HelloWorld
```

## Como testar a nova funcionalidade:
```sh
javac Feature.java && java Feature
```
" > README.md
```

Realizamos o commit e enviamos:

```sh
git add README.md
git commit -m "Documenta o processo no README"
git push origin main
```

---

## ⚙️ **Como Clonar e Utilizar o Repositório**

1. Clone o repositório:

```sh
git clone git@github.com:MuriloVinhal/GerenciaConfiguracao.git
cd GerenciaConfiguracao
```

2. Execute a versão principal do código:

```sh
javac HelloWorld.java && java HelloWorld
```

3. Para testar a nova funcionalidade (caso esteja na branch `nova-feature`):

```sh
javac Feature.java && java Feature
```

4. Caso queira trazer as alterações da branch `nova-feature` para a `main`:

```sh
git checkout main
git merge nova-feature
git push origin main
```

---

## 🔍 **Resolvendo Possíveis Problemas**

### 🚨 1. Erro "src refspec main does not match any"
Se ao fazer `git push origin main` você receber esse erro, pode ser que sua branch local ainda esteja `master`. Para corrigir:

```sh
git branch -M main
git push origin main
```

---

### 🚨 2. Erro "Permission denied (publickey)"
Se você receber este erro ao tentar fazer `git push`, significa que sua chave SSH não está configurada corretamente. Para corrigir:

1. Gere uma chave SSH (caso ainda não tenha):

```sh
ssh-keygen -t ed25519 -C "seu-email@gmail.com"
```

2. Adicione a chave ao SSH Agent:

```sh
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

3. Copie e adicione a chave ao GitHub:

```sh
cat ~/.ssh/id_ed25519.pub
```

No GitHub, vá em **Configurações → SSH Keys → New SSH Key** e cole a chave.

4. Teste a conexão:

```sh
ssh -T git@github.com
```

Agora, tente novamente o `git push`.

---

## 📌 **Conclusão**

Este projeto demonstrou a aplicação de **Gerência de Configuração de Software**, incluindo:

✅ **Uso de commits para diferentes versões**  
✅ **Criação e merge de branches**  
✅ **Documentação detalhada com README.md**  
✅ **Resolução de erros comuns no Git**  


