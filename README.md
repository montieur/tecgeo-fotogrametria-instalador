<div align="center">

<img src="logo.png" alt="tecgeo" height="60">

# TECGEO Fotogrametria — instalador

**Processamento de voos de drone com OpenDroneMap nativo no Windows, passo a passo.**

### [⬇ Baixar a última versão](https://github.com/montieur/tecgeo-fotogrametria-instalador/releases/latest)

</div>

Este repositório contém **apenas os instaladores** do TECGEO Fotogrametria, ferramenta de uso interno da TECGEO.
O código-fonte e a documentação técnica ficam em repositório privado.

## Instalação

1. Em [Releases](https://github.com/montieur/tecgeo-fotogrametria-instalador/releases/latest), baixe
   **`TECGEO-Fotogrametria-Setup-<versão>.exe`** e dê dois cliques.
2. No assistente:
   - escolha a **pasta dos projetos** — o instalador sugere o disco com mais espaço livre (cada voo ocupa de 30 a 100 GB);
   - deixe marcado **"Baixar e instalar o OpenDroneMap agora"** (~234 MB do GitHub oficial do OpenDroneMap, com conferência
     de SHA-256 e assinatura digital; o Windows pede permissão de administrador só nesta parte).
3. Ao concluir, o programa abre no navegador, pronto para usar.

> O instalador não tem assinatura de código. Se o Windows mostrar **"O Windows protegeu o computador"**,
> clique em **Mais informações → Executar assim mesmo**.

**Atualizar:** rode o instalador da versão nova por cima — projetos, configuração e OpenDroneMap são mantidos.
O programa avisa no topo da tela quando há versão nova.

**Desinstalar:** *Configurações → Aplicativos → TECGEO Fotogrametria*. Remove o programa e o OpenDroneMap e **mantém a pasta dos projetos**.

**Instalação silenciosa** (TI):

```bat
TECGEO-Fotogrametria-Setup-<versão>.exe /VERYSILENT /PROJETOS="D:\TECGEO-Projetos" /TASKS="odm,atalho"
```

## Requisitos

| Item | Mínimo | Recomendado |
|---|---|---|
| Sistema | Windows 10/11 64 bits | Windows 11 |
| Processador | 4 núcleos | 8 núcleos / 16 threads |
| Memória | 16 GB | 32 GB |
| Placa de vídeo | opcional | NVIDIA (acelera a nuvem de pontos densa) |
| Disco | ~3 GB para o programa + 30–100 GB por voo | SSD com bastante espaço livre |

Nenhuma outra instalação é necessária: o programa usa o Python que vem dentro do OpenDroneMap e o .NET Framework do Windows.

## Arquivos de cada versão

| Arquivo | Para quê |
|---|---|
| `TECGEO-Fotogrametria-Setup-<versão>.exe` | instalador (recomendado) |
| `TECGEO-Fotogrametria-v<versão>.zip` | pacote portátil: extrair e abrir `TECGEO Fotogrametria.exe` |

O SHA-256 de cada arquivo está nas notas da versão e na página da Release.

---

TECGEO · uso interno · motor de processamento: [OpenDroneMap](https://github.com/OpenDroneMap/ODM) (AGPL-3.0), instalado à parte.
