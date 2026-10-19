# Segurança — Knox Safehouse

## Reportar uma vulnerabilidade
Se encontrares um problema de segurança, **não o publiques** num sítio público. Envia uma mensagem privada ao autor do projeto (pelo GitHub do projeto: https://github.com/PzLauncher/knox-safehouse) com:
- a versão (e o SHA-256 do `.exe`),
- os passos para reproduzir,
- o impacto que esperas.

Respondemos assim que possível e combinamos a divulgação depois de haver correção.

## O que a app promete — e o que não promete
- **Sem telemetria**, sem analítica, sem servidores nossos. Destinos de rede: ver o README.
- **Não abre portas de escuta.** O servidor de Project Zomboid abre as portas dele (UDP 16261/16262); a app só as configura.
- **Segredos** (passwords do servidor e de admin, chave da Steam Web API) ficam no **Gestor de Credenciais do Windows** (DPAPI). Nunca em ficheiros da app nem em registos. Exceção inevitável: a password do servidor tem de estar no `.ini` do servidor, porque é de lá que o jogo a lê.
- **Tudo o que vem de fora é tratado como não confiável** (respostas da Steam, `mod.info`, `.ini`, perfis importados, links de coleções, saída do servidor): esquemas estritos, limites de tamanho, sem execução de nada.
- **Processos**: só `steamcmd.exe` (assinatura da Valve verificada) e o `java.exe` do servidor, por caminho absoluto e com lista de argumentos (sem shell, sem `.bat`). O único passo com administrador é a regra da firewall, com parâmetros fixos e validados.
- **A app não é "inhackeável"** e não consegue garantir que um mod é seguro: os mods são código de terceiros que corre no servidor.

## Verificar uma versão
Cada versão publica o SHA-256 do `KnoxSafehouse.exe`. No PowerShell:
```
Get-FileHash .\KnoxSafehouse.exe -Algorithm SHA256
```
As versões ainda **não têm assinatura de código** (o Windows SmartScreen pode avisar).

| Versão | SHA-256 |
|---|---|
| 0.1.0 (Marco 4 + correções, build de teste) | `5557562A24996728D6728A2AA0E8629FC594F0BF19806B80F2E3C9E6A946AC05` |
| 0.2.0 (build de teste) | `428F27C5DA50A976D22389B67043A5CD56CDD65F2B9C2E3776D89E37E6CAE0DF` |
| 0.2.1 (build de teste, correções de segurança) | `6DF5074E5231AB92612199321005517155D232ABF78A191A922618B996B109F4` |

## Bloqueio da app
O bloqueio com o Windows Hello chega no Marco 6. Quando existir, protege contra alguém que use o teu PC já desbloqueado; **não** protege contra malware nem contra quem tenha a tua conta do Windows.
