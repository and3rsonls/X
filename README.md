#![X](https://github.com/shellscriptx/X/blob/master/logo.png)

# Sobre

**A letra `X` possuí uma longa história de referências matemáticas, questões filosóficas entre outras; um caractere utilizado para preencher lacunas e representar a presença de algo. Por isso à escolhi para preceder o nome de cada script criado para resolver questões e problemas diários de uma forma simples ou até mesmo para diversão. :D**

## Scripts


> * <a href="#xsenha_complexa">xsenha_complexa.sh<a/>
> * <a href="#xcpf">xcpf.sh<a/>
> * <a href="#xchostname">xchostname.sh<a/>
> * <a href="#xconta_arquivo">xconta_arquivo.sh<a/>
> * <a href="#xcriar_atalho">xcriar_atalho.sh<a/>
> * <a href="#xdescanso_tela">xdescanso_tela.sh<a/>
> * <a href="#xfeliznatal">xfeliznatal.sh<a/>
> * <a href="#xget_termwin_size">xget_termwin_size.sh<a/>

<a name="xsenha_complexa"><a/> 
## 1. [xsenha_complexa.sh](https://github.com/shellscriptx/X/blob/master/xsenha_complexa.sh)

## Descrição
 
O xsenha_complexa.sh utiliza uma expressão regular em perl para testar o nível de uma senha na entrada padrão. Nenhuma máscara é aplicada para ocultar a senha, pois o procedimento constitui apenas em validá-la.

A senha deverá atenter os seguintes critérios de complexidade:

| Requerimentos mínimos|
|---------------------------------|
|8 caracteres|
|1 caractere minúsculo|
|1 caractere maiúsculo|
|1 dígito de 0 à 9|
|1 caractere especial|

## Instruções

Após a conclusão do download, vá até o diretório onde o script foi salvo e aplique a permissão para execução:

```
chmod +x xsenha_complexa.sh
```

Para verificar o nível de complexidade basta redirecionar a senha para entrada padrão do script.

#### Exemplo:

```
echo "senha" | ./xsenha_complexa.sh
```
_O script irá verificar os critérios de complexidades descritos na regex em perl e irá retornar uma mensagem de erro ou sucesso._

**Código de retorno**

Código|Descrição
---------|-------------
0| Sucesso
1| Erro

## Desenvolvido por
> Juliano Santos [SHAMAN]

## Bugs
> Reporte possíveis erros enviando email para <shellscriptx@gmail.com>

---

<a name="xcpf"></a>
## 2. [xcpf.sh](https://github.com/shellscriptx/X/blob/master/xcpf.sh)

## Descrição

O script verifica se o número do CPF informado é veradeiro ou falso, aplicando uma matemática simples que utiliza os dois últimos dígitos como validador.

**Código de retorno:**

Código|Descrição
---------|-------------
0|CPF válido
1|CPF inválido
2|O formato do CPF é inválido

## Instruções

Após a conclusão do download, vá até o diretório onde o script foi salvo e aplique a permissão para execução:
```
chmod +x xcpf.sh
```

Envie o número do CPF para entrada padrão do script.

**Exemplo:**

Considere o número hipotético abaixo:

```
echo '143.389.234-53' | ./xcpf.sh
```
_O formato da mascára do CPF deverá respeitar o seguinte critério: **xxx.xxx.xxx-xx**_

## Desenvolvido por
> Juliano Santos [SHAMAN]

## Bugs
> Reporte possíveis erros enviando email para <shellscriptx@gmail.com>
***

<a name="xchostname"><a/>
## 3. [xchostname.sh](https://github.com/shellscriptx/X/blob/master/xchostname.sh)

## Descrição
O script realiza alteração do nome da máquina sem requerer a reinicialização do sistema para que as alterações tenham efeito.

**Arquivos alterados:**

- [x] /etc/hostname
- [x] /etc/hosts
- [x] /proc/sys/kernel/hostname

## Instruções

Após a conclusão do download, vá até o diretório onde o script foi salvo e aplique a permissão para execução:
```
chmod +x xchostname.sh
```

#### Exemplo:

Para alterar o nome da máquina basta executar o comando a seguir:
```
sudo ./xchostname.sh novo_nome
```
_É necessário executar o scritpt com privilégios administrativos._
## Desenvolvido por
> Juliano Santos [SHAMAN]

## Bugs
> Reporte possíveis erros enviando email para <shellscriptx@gmail.com>
***

<a name="xconta_arquivo"><a/>
## 4. [xconta_arquivo.sh](https://github.com/shellscriptx/X/blob/master/xconta_arquivo.sh)

## Descrição
Lista a quantidade de arquivos do diretório informando, separando-os por extensão.

## Instruções

Após a conclusão do download, vá até o diretório onde o script foi salvo e aplique a permissão para execução:
```
chmod +x xconta_arquivo.sh
```

#### Sintaxe
```
./xconta_arquivo.sh [diretório]
```

Para calcular o total de arquivos de um determinado diretório, execute o script passando como argumento o diretório desejado.

#### Exemplo
Calculando os arquivos do diretório `/etc`
```
 ./xconta_arquivo.sh /etc
Calculando ...
 Extensão      Total
       pem          1
    evince          3
      defs          1
     alias          2
       key          1
     convs          1
       crt          1
    bashrc          2
bash_logout          1
     theme          4
     order          1
      stop          1
      opts          1
       cfg          6
    Debian          1
      pptp          1
  defaults          1
         O          1
  override          1
      name          1
       tti         32
   firefox          2
        el          3
     start          1
  ippusbxd          3
      init          3
       ini          2
  rsyslogd          2
      list          3
   desktop         35
      boot          1
       txt         17
     cupsd          3
    config          1
       ttb         86
   tcpdump          3
     types          2
       inc         28
       cat          2
       icd          1
       acm          1
       vga          1
    action          1
     cache          1
      dbus          1
        gz          2
        sh         29
      conf        434
     allow          1
      deny          1
   profile          1
       old          2
       atb          3
       gpg          2
  dhclient          3
        py          2
       net          1
      tiny          1
   options          1
       xsm          1
        js          3
     rules          6
       gen          1
      save          1
   default          1
      mime          1
    ubuntu          1
        pa          2
       cnf          1
       xml         19
  original          1
       ctb         29
       kti         90
     scale          1
placeholder          6
     local          5
 blacklist          3
       org          1
  features          1
      lock          1
      menu          3
       ktb        114
       cti          3

Diretório base: /etc
Total de arquivos: 1045
```
_É retornado uma lista de extensões seguido da sua quantidade e a quantidade total._

## Desenvolvido por
> Juliano Santos [SHAMAN]

## Bugs
> Reporte possíveis erros enviando email para <shellscriptx@gmail.com>
***

<a name="xcriar_atalho"><a/>
## 5. [xcriar_atalho.sh](https://github.com/shellscriptx/X/blob/master/xcriar_atalho.sh)

## Descrição
Cria atalhos para aplicações na área de trabalho.

## Instruções

Após a conclusão do download, vá até o diretório onde o script foi salvo e aplique a permissão para execução:
```
chmod +x xcriar_atalho.sh
```

#### Sintaxe:

```
./xcriar_atalho.sh [aplicativo]...
```

#### Exemplo:

Criando atalho do `virtualbox`.

```
./xcriar_atalho.sh virtualbox
```


O caminho completo do aplicativo é opcional, exceto se estiver localizada em um diretório não registrado na variável `$PATH`.  Por padrão o atalho é criado na área de trabalho, em caso de falha assume o `HOME` do usuário como local padrão.

O script suporta vários argumentos, permitindo a criação de multiplos atalhos em uma única instância. Os nomes precisam estar separados por um `espaço`

Exemplo: `./xcriar_atalho.sh aplicativo1 aplicativo2 aplicativo3...`

## Desenvolvido por
> Juliano Santos [SHAMAN]

## Bugs
> Reporte possíveis erros enviando email para <shellscriptx@gmail.com>
***

<a name ="xdescanso_tela"><a/>
## 6. [xdescanso_tela.sh](https://github.com/shellscriptx/X/blob/master/xdescanso_tela.sh)

## Descrição

Simula uma proteção de tela para terminal, que move um determinado texto em posições geometricamente direcionadas. 

## Instruções

Após a conclusão do download, vá até o diretório onde o script foi salvo e aplique a permissão para execução:
```
chmod +x xdescanso_tela.sh
```

#### Sintaxe:

```
./xdescanso_tela.sh [TEXTO] 
```

#### Exemplo:

Definindo a palavra `SHELL SCRIPT X` como descanso de tela.

```
./xdescanso_tela.sh "SHELL SCRIPT X"
```

Acesse a postagem referente em nosso blog e visualize o vídeo demonstrativo [clicando aqui](http://shellscriptx.blogspot.com.br/2016/12/descanso-de-tela-para-terminal.html)

## Desenvolvido por
> Juliano Santos [SHAMAN]

## Bugs
> Reporte possíveis erros enviando email para <shellscriptx@gmail.com>
***

<a name="xfeliznatal"><a/>
## 7. [xfeliznatal.sh](https://github.com/shellscriptx/X/blob/master/xfeliznatal.sh)

## Descrição

Para não deixar a data `25 de dezembro` em branco, resolvi fazer uma homenagem ao estilo `SHELL SCRIPT X`. 

O script exibe uma mensagem de boas festas simulando um letreiro digital.

**Pacote requerido:**

- [x] pv.1.6.0-1 ou superior

## Instruções

Após a conclusão do download, vá até o diretório onde o script foi salvo e aplique a permissão para execução:
```
chmod +x xfeliznatal.sh
```

#### Sintaxe:

```
./xfeliznatal.sh
```

O script não requer argumentos.

## Desenvolvido por
> Juliano Santos [SHAMAN]

## Bugs
> Reporte possíveis erros enviando email para <shellscriptx@gmail.com>
***

<a name="xget_termwin_size"><a/>
## 8. [xget_termwin_size.sh](https://github.com/shellscriptx/X/blob/master/xget_termwin_size.sh)

## Descrição

Cria uma trap que monitora o `SIGNAL WINCH` associado as alterações de dimensão do terminal atual. A função `ver_dimensao` lê os dados retornados na entrada padrão sempre que há alteração e imprime as dimensões no centro do terminal.

## Instruções

Após a conclusão do download, vá até o diretório onde o script foi salvo e aplique a permissão para execução:
```
chmod +x xget_termwin_size.sh
```

#### Uso:

```
./xget_termwin_size.sh
```

**Observação:** O script não requer argumentos.

#### Nota: 

Após a execução redimensione a janela do terminal para visualizar as dimensões atuais.

## Desenvolvido por
> Juliano Santos [SHAMAN]

## Bugs
> Reporte possíveis erros enviando email para <shellscriptx@gmail.com>
***

