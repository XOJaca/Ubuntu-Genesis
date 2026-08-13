# 🚀 Ubuntu Genesis (Post-Install)

Automação do meu ambiente **Ubuntu 26.04 LTS (Resolute Raccoon)** logo após uma instalação limpa, deixando o sistema pronto para uso prático — com minhas configurações pessoais, programas essenciais e ajustes que costumo aplicar em toda nova instalação.

Um pequeno presente para um *"distro-hopper"* que gosta de testar sistemas, mas quer recuperar rapidamente o ambiente familiar. 🐧

---

## 📋 Objetivos

- Instalar pacotes essenciais do sistema
- Configurar suporte a Flatpak & programas
- Instalar aplicativos de desktop automaticamente
- Configurar ferramentas multimídia (Celluloid, Rhythmbox, VLC, yt-dlp)
- Preparar o ambiente para jogos (Proton/DXVK)
- Aplicar DNS da Cloudflare
- Instalar aplicativos oficiais externos (Chrome, Brave, Steam)
- ~~Ocultar rastros do Snap sem desinstalar nada [PLANEJADO PARA O PRÓXIMO RELEASE]~~
- Economizar tempo após formatações

---

## ✅ Requisitos

- Ubuntu instalado recentemente
- Conexão com a internet
- Usuário com permissões de administrador (`sudo`)
- Arquitetura `amd64`

---

# 🚀 Como utilizar

1. Baixe a versão mais recente do **Ubuntu Genesis** na seção **Releases** deste repositório.
2. Extraia o arquivo `.zip` em qualquer pasta de sua preferência.
3. Abra a pasta extraída.
4. Clique com o botão direito do mouse na pasta baixada e aperte em "Abrir no Terminal"

Execute então o seguinte código:

```bash
chmod +x setup.sh
./setup.sh
```

## 📦 Módulos

O Genesis é dividido em módulos independentes, executados em ordem pelo `setup.sh`:

| # | Módulo | Descrição |
|---|--------|-----------|
| 01 | `01-essential-packages.sh` | Instala ferramentas essenciais (git, curl, wget, build-essential, etc), corrige a tela de login no monitor atual e substitui o Firefox Snap pela versão Debian (oficial da Mozilla) |
| 02 | `02-flatpak.sh` | Configura o Flathub e instala aplicativos em Flatpak (Discord, VLC, qBittorrent, OnlyOffice, OBS, Kdenlive, Lutris, Heroic, entre outros) |
| 03 | `03-desktop-applications.sh` | Instala Google Chrome, Brave, Steam, Audacity e Rhythmbox; define Nautilus, Rhythmbox e VLC como aplicativos padrão para pastas, áudio e vídeo |
| 04 | `04-gaming-environment.sh` | Ajusta variáveis do DXVK para o ambiente de jogos via Proton |
| 05 | `05-mpv-config.sh` | Suporte a LSFG-VK + Legendas amarelas no MPV |
| 06 | `06-network-config.sh` | Configura o DNS da Cloudflare (1.1.1.1) em todas as conexões de rede |
| 07 | `07-yt-dlp.sh` | Instala o FFmpeg e a versão mais recente do yt-dlp, com download padrão em `~/Downloads` |

---

## ⚠️ Observações

- Algumas configurações aplicadas pelo Genesis podem exigir uma **reinicialização** para fazer efeito (principalmente as de jogos, da loja do Gnome e dos aplicativos em Flatpak).
- O script assume um ambiente **GNOME** (padrão do Ubuntu).
- Testado especificamente no Ubuntu 26.04 LTS; use em outras versões por sua conta e risco.

---

## 📝 Licença

Projeto de uso pessoal, sinta-se à vontade para adaptar aos seus próprios fluxos.
