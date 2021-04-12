---
title: Inizializzazione della pagina
description: Inizializzazione della pagina
ms.assetid: 66bd3810-01a3-4413-9dad-12cf71e72ed1
keywords:
- Windows Media Player Online Stores, Download Manager
- archivi online, gestione download
- digitare 2 archivi online, Download Manager
- Windows Media Player Online Stores, inizializzazione di pagine
- archivi online, inizializzazione di pagine
- digitare 2 archivi online, inizializzazione di pagine
- Windows Media Player, Download Manager
- Gestione download di Windows Media Player
- Gestione download
- inizializzazione di pagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1570d1b77abdc99ba2aee613ed8ddb88fc8097c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221732"
---
# <a name="initializing-the-page"></a>Inizializzazione della pagina

Quando viene caricata la pagina Web, viene eseguita la funzione **init** . Questo codice recupera prima tutti i dati archiviati in una sessione precedente. Per informazioni dettagliate, vedere [gestione delle informazioni sulla sessione](maintaining-session-information.md). Quindi crea l'oggetto **downloadmanager** e lo archivia nella variabile globale denominata g \_ oManager.


```C++
g_oManager = external.DownloadManager;

```



Successivamente, la funzione connette l'evento **OnColorChange** alla funzione denominata **OnAppColor** e quindi chiama direttamente la funzione per inizializzare il colore di sfondo. Vedere [corrispondenza dei colori di Windows Media Player](matching-the-windows-media-player-colors.md).

Infine, la funzione avvia un timer con un intervallo di un secondo e inizializza le caselle di riepilogo che visualizzano le raccolte di download in sospeso e gli elementi di download. Questo è importante perché è possibile che siano state apportate sessioni in corso l'ultima volta che l'archivio online è stato chiuso e che queste informazioni devono essere visualizzate nuovamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso di Download Manager**](using-the-download-manager.md)
</dt> </dl>

 

 




