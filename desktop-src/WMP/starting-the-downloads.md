---
title: Avvio dei download
description: Avvio dei download
ms.assetid: 0a830b11-f7e1-41da-a867-86f9ac361c0b
keywords:
- Windows Media Player online, Download Manager
- online store, Download Manager
- store online di tipo 2, Download Manager
- Windows Media Player store online, avvio dei download
- store online, avvio di download
- store online di tipo 2, avvio dei download
- Windows Media Player,Download Manager
- Windows Media Player Download Manager
- Download Manager
- avvio di download
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d600bb037204b4dae1c07d8938e92eae2862460b94ef285567a8ca14144e72c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995071"
---
# <a name="starting-the-downloads"></a>Avvio dei download

Il download viene avviato quando l'utente fa clic su **Scarica**. Questo pulsante è denominato btnDownload nel codice e la funzione del gestore eventi per l'evento **onClick** è denominata "OnDownload".

"OnDownload" crea innanzitutto un nuovo oggetto **DownloadCollection** vuoto e lo assegna a una variabile locale.


```C++
oDLC = g_oManager.createDownloadCollection();

```



Successivamente, la funzione avvia ognuno dei cinque elementi scaricando e archivia l'oggetto **DownloadItem** restituito in una matrice.


```C++
g_DLI[0] = oDLC.startDownload(g_sFiles[0], g_sDLType);
g_DLI[1] = oDLC.startDownload(g_sFiles[1], g_sDLType);
g_DLI[2] = oDLC.startDownload(g_sFiles[2], g_sDLType);
g_DLI[3] = oDLC.startDownload(g_sFiles[3], g_sDLType);
g_DLI[4] = oDLC.startDownload(g_sFiles[4], g_sDLType);

```



Il codice aggiorna quindi gli elementi dell'interfaccia utente con le informazioni sulla raccolta di download e i relativi elementi di download.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso di Download Manager**](using-the-download-manager.md)
</dt> </dl>

 

 




