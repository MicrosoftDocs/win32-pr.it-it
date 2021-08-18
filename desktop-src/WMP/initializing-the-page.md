---
title: Inizializzazione della pagina
description: Inizializzazione della pagina
ms.assetid: 66bd3810-01a3-4413-9dad-12cf71e72ed1
keywords:
- Windows Media Player online store, Download Manager
- negozi online, Download Manager
- Store online di tipo 2, Download Manager
- Windows Media Player negozi online, inizializzazione di pagine
- negozi online, inizializzazione di pagine
- Tipo 2 di negozi online, inizializzazione di pagine
- Windows Media Player,Download Manager
- Windows Media Player Download Manager
- Download Manager
- inizializzazione di pagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e929038c45e5f85a640b5c4ce5c86be56957fdb9067624feddf381ab5093623
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748166"
---
# <a name="initializing-the-page"></a>Inizializzazione della pagina

Quando la pagina Web viene caricata, viene **eseguita la funzione Init.** Questo codice recupera prima tutti i dati archiviati in una sessione precedente. Per informazioni dettagliate, vedere [Gestione delle informazioni sulla sessione](maintaining-session-information.md). Crea quindi **l'oggetto DownloadManager** e lo archivia nella variabile globale denominata g \_ oManager.


```C++
g_oManager = external.DownloadManager;

```



Successivamente, la funzione connette **l'evento OnColorChange** alla funzione **denominata OnAppColor** e quindi chiama direttamente la funzione per inizializzare il colore di sfondo. Vedere [Corrispondenza dei Windows Media Player colori.](matching-the-windows-media-player-colors.md)

Infine, la funzione avvia un timer con un intervallo di un secondo e inizializza le caselle di riepilogo che visualizzano le raccolte di download in sospeso e gli elementi di download. Questo è importante perché potrebbero essere in corso sessioni l'ultima volta che il negozio online è stato chiuso e queste informazioni devono essere visualizzate di nuovo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso di Download Manager**](using-the-download-manager.md)
</dt> </dl>

 

 




