---
title: Parametri della riga di comando
description: Parametri della riga di comando
ms.assetid: c4af8a03-2cab-4ecd-bbd8-c83869822901
keywords:
- Media Player di Windows, parametri
- Windows Media Player, parametri della riga di comando
- Windows Media Player, wmplayer
- Windows Media Player, Wmpconfig
- Windows Media Player, WMPNSCFG
- parametri da riga di comando
- Wmplayer
- Wmpconfig
- WMPNSCFG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa65b686f8a746111a62bd6afcc3df280191c65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298716"
---
# <a name="command-line-parameters"></a>Parametri della riga di comando

## <a name="command-line-parameters-for-wmplayer"></a>Parametri della riga di comando per wmplayer

Windows Media Player supporta un set di parametri della riga di comando che specificano il comportamento del lettore all'avvio. Nella tabella seguente vengono illustrati in dettaglio i parametri e i relativi comportamenti.



| Sintassi                                                                                                              | Comportamento                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "*path \\ filename*" (ad esempio: `wmplayer "c:\filename.wma"` )<br/>                                            | Avviare il lettore e riprodurre il file.                                                                                                                                                                                                                                                                                                        |
| "*path \\ filename*"/fullscreen (ad esempio: `wmplayer "c:\filename.wmv" /fullscreen` )<br/>                    | Riprodurre il file specificato in modalità schermo intero. È necessario specificare il percorso e il nome file del contenuto da riprodurre.<br/>                                                                                                                                                                                                                     |
| /Device: {DVD \| AudioCD} (ad esempio: `wmplayer /device:audio CD` )<br/>                                         | Riprodurre un DVD o un CD audio.                                                                                                                                                                                                                                                                                                                    |
| "*percorso \\ filename*? WMPSkin =*nome interfaccia*", ad esempio: `wmplayer "c:\filename.wma?wmpskin=headspace"`<br/>        | Aprire il lettore, applicando l'interfaccia specificata.                                                                                                                                                                                                                                                                                              |
| /Service:*nome* della pagina                                                                                                  | Aprire il lettore che mostra lo Store online specificato da *nome* di chiavi. Richiede Windows Media Player 10 o versione successiva.<br/>                                                                                                                                                                                                                      |
| NowPlaying/Task                                                                                                    | Aprire il lettore nella funzionalità **ora di riproduzione** .                                                                                                                                                                                                                                                                                            |
| MediaGuide/Task                                                                                                    | Aprire il lettore nella funzionalità **Media Guide** (Current Active Online Store in Windows Media Player 10 o versione successiva).                                                                                                                                                                                                                          |
| CDAudio/Task                                                                                                       | Aprire il lettore nella funzionalità **copia da CD** (funzionalità **Rip** in Windows Media Player 10 o Windows Media Player 11). Questo parametro non è supportato in Windows Media Player 12.                                                                                                                                                       |
| CDWrite/Task                                                                                                       | Aprire il lettore nella funzionalità **Burn** . Richiede Windows Media Player 10.<br/>                                                                                                                                                                                                                                                       |
| MediaLibrary/Task                                                                                                  | Aprire il lettore nella funzionalità della **libreria** .                                                                                                                                                                                                                                                                                                |
| /Task RadioTuner                                                                                                    | Aprire il lettore nella funzionalità **Radio Tuner** (Current Active Online Store in Windows Media Player 10 o versione successiva).                                                                                                                                                                                                                          |
| PortableDevice/Task                                                                                                | Aprire il lettore nella funzionalità **copia su CD o dispositivo** (funzionalità di **sincronizzazione** in Windows Media Player 10 o versione successiva).                                                                                                                                                                                                                            |
| Servizi/Task/Service *ServiceName*                                                                               | Aprire il lettore nella funzionalità **Servizi Premium** , mostrando il servizio specificato dal parametro *ServiceName* . Questo valore è il nome univoco per il servizio. Se il servizio specificato non è stato visualizzato in precedenza, il parametro *ServiceName* viene ignorato. (Apre l'archivio online specificato in Windows Media Player 10 o versione successiva). |
| /Task ServiceTask *X*                                                                                                | Aprire il lettore nel riquadro attività del servizio online Store specificato da *X*. Ad esempio,/Task ServiceTask1 apre il lettore nel primo riquadro attività del servizio di archiviazione online.                                                                                                                                                                      |
| SkinViewer/Task                                                                                                    | Aprire il lettore nella funzionalità **selezione interfaccia** .                                                                                                                                                                                                                                                                                           |
| /Playlist *playlistname*                                                                                            | Aprire il lettore e riprodurre la playlist specificata.                                                                                                                                                                                                                                                                                           |
| /Schema: {Music \| Pictures \| video \| TV \| other}, ad esempio: `wmplayer /Schema:Pictures /Task:PortableDevice`<br/> | Aprire il lettore, mostrando la categoria di supporti specificata. Richiede Windows Media Player 11.                                                                                                                                                                                                                                                   |



 

## <a name="command-line-parameters-for-wmpconfig"></a>Parametri della riga di comando per Wmpconfig

Wmpconfig.exe viene usato per eseguire alcuni comandi in Windows Media Player che richiedono l'autorizzazione di amministratore. Gli esempi includono l'avvio e l'arresto dei servizi di esplorazione e condivisione e l'abilitazione delle eccezioni nel Windows Firewall. Nella tabella seguente vengono descritti i valori possibili per i parametri della riga di comando.



| Sintassi                                                                                    | Comportamento                                                                   |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| *Mac* DisableHMEDevice                                                                    | Disabilita il dispositivo specificato da un identificatore MAC (Media Access Control).  |
| Esempio di HMEOff:<br/> wmpconfig HMEOff<br/>                                    | Disabilita l'Servizio di condivisione in rete Windows Media Player.                 |
| Esempio di HMEOn:<br/> wmpconfig HMEOn<br/>                                      | Consente la condivisione, l'esplorazione e l'eccezione del firewall.                     |
| *Mac* RemoveHMEDevice                                                                     | Rimuove il dispositivo specificato da un identificatore MAC.                          |
| *Mac* RestoreHMEDevice                                                                    | Ripristina il dispositivo specificato da un identificatore MAC.                         |
| Esempio di *livello* SetDVDParentalLevel:<br/> wmpconfig SetDVDParentalLevel 3<br/> | Imposta il livello di controllo parentale DVD. Il livello viene specificato come valore integer. |



 

## <a name="command-line-parameters-for-wmpnscfg"></a>Parametri della riga di comando per WMPNSCFG

Microsoft Windows usa wmpnscfg.exe per avvisare gli utenti quando i dispositivi per il rendering multimediale si trovano nella rete. WMPNSCFG avvia il Servizio di condivisione in rete Windows Media Player (NSS) e quindi attende le notifiche dal servizio. Quando WMPNSCFG riceve la notifica che un nuovo dispositivo multimediale è disponibile nella rete, Visualizza un popup nella barra delle applicazioni che informa l'utente sulla disponibilità del nuovo dispositivo. Se l'utente fa clic sul popup, WMPNSCFG avvia Windows Media Player, che visualizza una finestra di dialogo in cui viene chiesto all'utente di consentire o negare la condivisione con il nuovo dispositivo.

In genere, Windows chiama WMPNSCFG senza parametri della riga di comando. Tuttavia, è disponibile un parametro, descritto nella tabella seguente.



| Parametro | Comportamento                         |
|-----------|----------------------------------|
| /Close    | Chiudere tutte le istanze di wmpnscfg. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 





