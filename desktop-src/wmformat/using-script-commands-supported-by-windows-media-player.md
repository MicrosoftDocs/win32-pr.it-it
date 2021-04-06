---
title: Uso di comandi script supportati da Windows Media Player
description: Uso di comandi script supportati da Windows Media Player
ms.assetid: 7054ce49-c000-4978-891e-825a83bfda5c
keywords:
- Windows Media Format SDK, comandi script
- Windows Media Format SDK, Windows Media Player
- ASF (Advanced Systems Format), comandi script
- ASF (Advanced Systems Format), comandi script
- ASF (Advanced Systems Format), Windows Media Player
- ASF (formato avanzato dei sistemi), Windows Media Player
- script, comandi
- script, Windows Media Player
- Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25302b5f5b6789be0d9e18b0a93e1e781a9dc06b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044798"
---
# <a name="using-script-commands-supported-by-windows-media-player"></a>Uso di comandi script supportati da Windows Media Player

Windows Media Format SDK non fornisce supporto nativo per l'analisi e la risposta ai comandi di script. È necessario includere qualsiasi logica relativa ai comandi di script nell'applicazione. Anche i tipi di script usati devono essere definiti nell'applicazione.

È possibile includere codice per gestire gli stessi comandi script supportati da Windows Media Player. La gestione della compatibilità con Windows Media Player rende i file più universali che se si incorporano comandi script personalizzati.

Nella tabella seguente sono elencati i tipi di script supportati da Windows Media Player.



| Tipo di script | Descrizione                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| URL         | Il lettore invia l'URL specificato al browser per la visualizzazione all'utente. Se viene usato un controllo Player incorporato, è possibile aggiungere un riferimento al frame specifico all'URL usando la sintassi &&*FrameName* .                                                                             |
| FILENAME    | URL di un altro file multimediale da riprodurre.                                                                                                                                                                                                                                                |
| CAPTION     | Una stringa di testo visualizzata nell'area didascalie di Windows Media Player. Questo tipo supporta la formattazione HTML standard, quindi il testo può essere formattato nel modo desiderato. Un esempio di utilizzo è la didascalia closed.                                                                             |
| EVENTO       | Nome di un evento che deve verificarsi. Il tipo di evento supporta la personalizzazione per usi personalizzati. Il codice per l'evento specificato deve essere definito nel metafile di Windows Media per il flusso affinché il lettore esegua l'evento specificato. Un esempio d'uso è l'inserimento di annunci. |
| OPENEVENT   | Questo script precede l'evento effettivo. Il OPENEVENT consente al lettore di pre-memorizzare il contenuto nel buffer in modo che, quando si verifica l'evento, il passaggio tra i flussi risulti trasparente.                                                                                                       |
| TEXT        | Una stringa di testo visualizzata nell'area didascalie di Windows Media Player. Può essere testo normale, SAMI o testo formattato HTML.                                                                                                                                                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso di comandi script**](using-script-commands.md)
</dt> </dl>

 

 




