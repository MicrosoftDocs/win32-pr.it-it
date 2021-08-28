---
title: Uso di comandi script supportati da Windows Media Player
description: Uso di comandi script supportati da Windows Media Player
ms.assetid: 7054ce49-c000-4978-891e-825a83bfda5c
keywords:
- Windows MEDIA Format SDK, comandi script
- Windows Media Format SDK,Windows Media Player
- Advanced Systems Format (ASF), comandi script
- ASF (Advanced Systems Format),comandi script
- Advanced Systems Format (ASF), Windows Media Player
- ASF (Advanced Systems Format), Windows Media Player
- script, comandi
- script, Windows Media Player
- Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58709af99cb4ebcb4eaba64fa6bb167b0ca80acb3fcb21b34efe4a55e2bacf12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110071"
---
# <a name="using-script-commands-supported-by-windows-media-player"></a>Uso di comandi script supportati da Windows Media Player

L Windows Media Format SDK non fornisce supporto nativo per l'analisi e la risposta ai comandi script. È necessario includere nell'applicazione qualsiasi logica correlata ai comandi script. Anche i tipi di script utilizzati devono essere definiti nell'applicazione.

È possibile includere codice per gestire gli stessi comandi script supportati da Windows Media Player. Mantenere la compatibilità con Windows Media Player rende i file più universali rispetto all'incorporamento di comandi script personalizzati.

Nella tabella seguente sono elencati i tipi di script supportati da Windows Media Player.



| Tipo di script | Descrizione                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| URL         | Il lettore invia l'URL specificato al browser per la visualizzazione all'utente. Se viene usato un controllo lettore incorporato, è possibile aggiungere un riferimento al frame specifico all'URL usando la sintassi &&*nome frame.*                                                                             |
| Filename    | URL di un altro file multimediale da riprodurre.                                                                                                                                                                                                                                                |
| CAPTION     | Stringa di testo visualizzata nell'area delle didascalie di Windows Media Player. Questo tipo supporta la formattazione HTML standard, quindi il testo può essere formattato nel modo desiderato. Un esempio d'uso è la codifica codificata.                                                                             |
| Evento       | Nome di un evento che deve verificarsi. Il tipo EVENT supporta la personalizzazione per usi personalizzati. Il codice per l'evento specificato deve essere definito nel metafile Windows Media per il flusso per consentire al lettore di eseguire l'evento specificato. Un esempio d'uso è l'inserimento di annunci. |
| OPENEVENT   | Questo script precede l'evento effettivo. OPENEVENT consente al lettore di eseguire il pre-buffer del contenuto in modo che, quando si verifica l'EVENTO, il passaggio tra i flussi sia trasparente.                                                                                                       |
| TEXT        | Stringa TEXT visualizzata nell'area delle didascalie di Windows Media Player. Può essere testo normale, SAMI o testo in formato HTML.                                                                                                                                                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso di comandi script**](using-script-commands.md)
</dt> </dl>

 

 




