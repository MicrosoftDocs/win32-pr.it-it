---
title: Avvio dei download
description: Avvio dei download
ms.assetid: 0a830b11-f7e1-41da-a867-86f9ac361c0b
keywords:
- Windows Media Player Online Stores, Download Manager
- archivi online, gestione download
- digitare 2 archivi online, Download Manager
- Windows Media Player Online Stores, avvio di download
- negozi online, avvio di download
- digitare 2 archivi online, avvio di download
- Windows Media Player, Download Manager
- Gestione download di Windows Media Player
- Gestione download
- avvio del download
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec723bd504cc511c3ca43db90f3c613a8acefd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396750"
---
# <a name="starting-the-downloads"></a>Avvio dei download

Il download viene avviato quando l'utente fa clic su **download**. Questo pulsante è denominato btnDownload nel codice e la funzione del gestore eventi per l'evento **OnClick** è denominata "ondownload".

Con "ondownload" viene innanzitutto creato un nuovo oggetto **scaricabile** vuoto che viene assegnato a una variabile locale.


```C++
oDLC = g_oManager.createDownloadCollection();

```



Successivamente, la funzione avvia ognuno dei cinque elementi scaricati e archivia l'oggetto **DownloadItem** restituito in una matrice.


```C++
g_DLI[0] = oDLC.startDownload(g_sFiles[0], g_sDLType);
g_DLI[1] = oDLC.startDownload(g_sFiles[1], g_sDLType);
g_DLI[2] = oDLC.startDownload(g_sFiles[2], g_sDLType);
g_DLI[3] = oDLC.startDownload(g_sFiles[3], g_sDLType);
g_DLI[4] = oDLC.startDownload(g_sFiles[4], g_sDLType);

```



Il codice aggiorna quindi gli elementi dell'interfaccia utente con le informazioni sulla raccolta di download e sui relativi elementi di download.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso di Download Manager**](using-the-download-manager.md)
</dt> </dl>

 

 




