---
title: Parametri della riga di comando
description: Parametri della riga di comando
ms.assetid: c4af8a03-2cab-4ecd-bbd8-c83869822901
keywords:
- Windows Media Player,parameters
- Windows Media Player,parametri della riga di comando
- Windows Media Player,Wmplayer
- Windows Media Player,Wmpconfig
- Windows Media Player,Wmpnscfg
- parametri da riga di comando
- Wmplayer
- Wmpconfig
- Wmpnscfg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2240040453bc60a7a03ca56f205643f97202eb840a501fd13aa417b86aef060d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341951"
---
# <a name="command-line-parameters"></a>Parametri della riga di comando

## <a name="command-line-parameters-for-wmplayer"></a>Parametri della riga di comando per Wmplayer

Windows Media Player supporta un set di parametri della riga di comando che specificano il comportamento di Player all'avvio. Nella tabella seguente sono riportati in dettaglio i parametri e i relativi comportamenti.



| Sintassi                                                                                                              | Comportamento                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "*path \\ filename*"(Ad esempio: `wmplayer "c:\filename.wma"` )<br/>                                            | Avviare Player e riprodurre il file.                                                                                                                                                                                                                                                                                                        |
| "*path \\ filename*" /fullscreen(Ad esempio: `wmplayer "c:\filename.wmv" /fullscreen` )<br/>                    | Riprodurre il file specificato in modalità schermo intero. È necessario specificare il percorso e il nome file del contenuto da riprodurre.<br/>                                                                                                                                                                                                                     |
| /Device:{DVD \| AudioCD}(Ad esempio: `wmplayer /device:audio CD` )<br/>                                         | Riprodurre un CD DVD o audio.                                                                                                                                                                                                                                                                                                                    |
| "*path \\ filename*? WMPSkin=*nome dell'interfaccia*"Ad esempio: `wmplayer "c:\filename.wma?wmpskin=headspace"`<br/>        | Aprire player, applicando l'interfaccia specificata.                                                                                                                                                                                                                                                                                              |
| /Service:*keyname*                                                                                                  | Aprire il lettore che mostra il negozio online specificato da *keyname*. Richiede Windows Media Player 10 o versione successiva.<br/>                                                                                                                                                                                                                      |
| /Task NowPlaying                                                                                                    | Aprire il lettore nella **funzionalità In** riproduzione.                                                                                                                                                                                                                                                                                            |
| /Task MediaGuide                                                                                                    | Aprire il lettore nella **funzionalità Guida** multimediale (negozio online attivo corrente in Windows Media Player 10 o versione successiva).                                                                                                                                                                                                                          |
| /Task CDAudio                                                                                                       | Aprire il lettore nella **funzionalità Copia** da CD (**rip** in Windows Media Player 10 o Windows Media Player 11). Questo parametro non è supportato in Windows Media Player 12.                                                                                                                                                       |
| /Task CDWrite                                                                                                       | Aprire il lettore nella **funzionalità Di** masterizzazione. Richiede Windows Media Player 10.<br/>                                                                                                                                                                                                                                                       |
| /Task MediaLibrary                                                                                                  | Aprire il lettore nella **funzionalità Libreria.**                                                                                                                                                                                                                                                                                                |
| /Task RadioTuner                                                                                                    | Aprire il lettore nella **funzionalità Siner radio** (negozio online attivo corrente in Windows Media Player 10 o versione successiva).                                                                                                                                                                                                                          |
| /Task PortableDevice                                                                                                | Aprire il lettore nella **funzionalità Copia su CD o** Dispositivo (funzionalità di sincronizzazione in Windows Media Player 10 o versioni successive).                                                                                                                                                                                                                            |
| /Task Services /Service *servicename*                                                                               | Aprire Player nella funzionalità **Premium Services,** che mostra il servizio specificato dal *parametro servicename.* Questo valore è il nome univoco per il servizio. Se il servizio specificato non è stato visualizzato in precedenza, il *parametro servicename* viene ignorato. Apre il negozio online specificato in Windows Media Player 10 o versione successiva. |
| /Task ServiceTask *X*                                                                                                | Aprire Il lettore nel riquadro attività del servizio negozio online specificato da *X*. Ad esempio, /Task ServiceTask1 apre Player nel primo riquadro attività del servizio negozio online.                                                                                                                                                                      |
| /Task SkinViewer                                                                                                    | Aprire Il lettore nella **funzionalità Scelta interfaccia.**                                                                                                                                                                                                                                                                                           |
| /Playlist *PlaylistName*                                                                                            | Aprire il lettore e riprodurre la playlist specificata.                                                                                                                                                                                                                                                                                           |
| /Schema:{Musica Pictures \| \| Video \| TV \| Other}Ad esempio:`wmplayer /Schema:Pictures /Task:PortableDevice`<br/> | Aprire Il lettore, che mostra la categoria di supporti specificata. Richiede Windows Media Player 11.                                                                                                                                                                                                                                                   |



 

## <a name="command-line-parameters-for-wmpconfig"></a>Parametri della riga di comando per Wmpconfig

Wmpconfig.exe viene usato per eseguire determinati comandi in Windows Media Player che richiedono l'autorizzazione di amministratore. Ad esempio, l'avvio e l'arresto dell'esplorazione e della condivisione dei servizi e l'abilitazione delle eccezioni nel firewall Windows. Nella tabella seguente vengono descritti i valori possibili per i parametri della riga di comando.



| Sintassi                                                                                    | Comportamento                                                                   |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| DisableHMEDevice *MAC*                                                                    | Disabilita il dispositivo specificato da un identificatore MAC (Media Access Control).  |
| Esempio HMEOff:<br/> wmpconfig HMEOff<br/>                                    | Disabilita l'Windows Media Player di condivisione di rete.                 |
| Esempio HMEOn:<br/> wmpconfig HMEOn<br/>                                      | Abilita la condivisione, l'esplorazione e l'eccezione del firewall.                     |
| RemoveHMEDevice *MAC*                                                                     | Rimuove il dispositivo specificato da un identificatore MAC.                          |
| RestoreHMEDevice *MAC*                                                                    | Ripristina il dispositivo specificato da un identificatore MAC.                         |
| Esempio di livello SetDVDParentalLevel: <br/> wmpconfig SetDVDParentalLevel 3<br/> | Imposta il livello di controllo genitori dvd. Il livello viene specificato come integer. |



 

## <a name="command-line-parameters-for-wmpnscfg"></a>Parametri della riga di comando per Wmpnscfg

Microsoft Windows usa wmpnscfg.exe per avvisare gli utenti quando i dispositivi di rendering dei contenuti multimediali vengono trovati in rete. Wmpnscfg avvia il Windows Media Player di condivisione di rete (NSS) e quindi attende le notifiche dal servizio. Quando wmpnscfg viene notificato che un nuovo dispositivo multimediale è disponibile in rete, nella barra delle applicazioni viene visualizzata una finestra popup che informa l'utente della disponibilità del nuovo dispositivo. Se l'utente fa clic sul popup, wmpnscfg avvia Windows Media Player, che visualizza una finestra di dialogo che chiede all'utente di consentire o negare la condivisione con il nuovo dispositivo.

In genere, Windows chiama wmpnscfg senza parametri della riga di comando. Tuttavia, è disponibile un parametro, descritto nella tabella seguente.



| Parametro | Comportamento                         |
|-----------|----------------------------------|
| /Close    | Chiudere tutte le istanze di wmpnscfg. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 





