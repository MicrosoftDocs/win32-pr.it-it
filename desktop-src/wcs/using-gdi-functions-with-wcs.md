---
title: Uso delle funzioni GDI con WCS
description: Nell'interfaccia GDI (Graphics Device Interface) sono disponibili varie funzioni che usano o operano sui dati di colore.
ms.assetid: a19ec8b9-11c9-4fde-a99a-7f4a112b49e7
keywords:
- Windows Sistema di colori (WCS), interfaccia GDI (Graphics Device Interface)
- WCS (Windows Color System),graphics device interface (GDI)
- gestione dei colori delle immagini, interfaccia GDI (Graphics Device Interface)
- gestione dei colori, interfaccia GDI (Graphics Device Interface)
- colori, interfaccia GDI (Graphics Device Interface)
- interfaccia GDI (Graphics Device Interface)
- GDI (interfaccia grafica del dispositivo)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a104378ae46e6b9519d6f795d280d45c28c8fa3fdc7d1e34aae609bcdbd195d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118444678"
---
# <a name="using-gdi-functions-with-wcs"></a>Uso delle funzioni GDI con WCS

Nell'interfaccia GDI (Graphics Device Interface) sono disponibili varie funzioni che usano o operano sui dati di colore. Alcune sono abilitate per l'uso con WCS e altre no. Le funzioni GDI seguenti sono rilevanti per ICM:

-   [Funzioni del contesto di dispositivo con WCS](#device-context-functions-with-wcs)
-   [Funzioni penna e pennello con WCS](#pen-and-brush-functions-with-wcs)
-   [Funzioni di output di testo con WCS](#text-output-functions-with-wcs)
-   [Funzioni bitmap con WCS](#bitmap-functions-with-wcs)

## <a name="device-context-functions-with-wcs"></a>Funzioni del contesto di dispositivo con WCS



|    Funzione                |   Descrizione                                                                                                                                                                                                                              |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CreateCompatibleDC | Se il contesto di dispositivo (DC) passato a questa funzione tramite il relativo parametro hdc è abilitato per ICM, anche il controller di dominio creato dalla funzione ICM abilitato. Gli spazi colori di origine e di destinazione sono specificati nel controller di dominio. |
| CreateDC           | ICM può essere abilitato impostando il membro dmICMMethod della struttura DEVMODE a cui punta il parametro pInitData sul valore appropriato. Per informazioni dettagliate, vedere la documentazione in Platform SDK sulla struttura DEVMODE.  |
| ResetDC            | Il profilo colori del contesto di dispositivo specificato dal parametro hdc verrà reimpostato in base alle informazioni nella struttura DEVMODE specificata dal parametro lpInitData.                                                   |



 

## <a name="pen-and-brush-functions-with-wcs"></a>Funzioni penna e pennello con WCS



|    Funzione                |   Descrizione                                                                                                                                                                                                                              |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Funzioni brush | Non viene eseguita alcuna gestione del colore durante la creazione del pennello. Tuttavia, la gestione dei colori verrà eseguita quando il pennello viene selezionato in un controller ICM abilitato. |
| CreatePen       | Non viene eseguita alcuna gestione del colore durante la creazione della penna. Tuttavia, la gestione dei colori verrà eseguita quando il pennello viene selezionato in un controller ICM abilitato.   |
| ExtCreatePen    | Non viene eseguita alcuna gestione del colore durante la creazione della penna. Tuttavia, la gestione dei colori verrà eseguita quando il pennello viene selezionato in un controller ICM abilitato.   |
| SelectObject    | Se l'oggetto selezionato è un pennello o una penna, viene eseguita la gestione dei colori.                                                              |
| SetDCBrushColor | La gestione dei colori viene eseguita se WCS è abilitato.                                                                                              |
| SetDCPenColor   | La gestione dei colori viene eseguita se WCS è abilitato.                                                                                              |



 

## <a name="text-output-functions-with-wcs"></a>Funzioni di output di testo con WCS



|    Funzione                |   Descrizione                                                                                                                                                                                                                              |
|--------------|--------------------------------------------------|
| SetBkColor   | La gestione dei colori viene eseguita se WCS è abilitato. |
| SetTextColor | La gestione dei colori viene eseguita se WCS è abilitato. |



 

## <a name="bitmap-functions-with-wcs"></a>Funzioni bitmap con WCS



|    Funzione                |   Descrizione                                                                                                                                                                                                                              |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bitblt            | Non viene eseguita alcuna gestione del colore quando si verificano blie.                                                                                                                                                                                                                                                                                                                                                                                             |
| CreateDIBitmap    | Il fuUsage parametro specifica che il bmiColors membro della struttura BITMAPINFO a cui punta il lpbmi parametro non contiene o non contiene informazioni sul colore. In caso contrario, per questa bitmap non viene eseguita alcuna gestione del colore. La bitmap deve usare la versione 4 o la versione 5 della struttura BITMAPINFO per poter essere abilitata la gestione dei colori. Il contenuto della bitmap risultante non corrisponde al colore dopo la creazione della bitmap. |
| CreateDIBSection  | Se la struttura BITMAPINFO passata tramite il parametro pbmi non è la versione 4 o 5, non viene eseguita alcuna gestione dei colori. Se è la versione 4 o 5, la gestione dei colori è abilitata e lo spazio colore specificato è associato alla bitmap.                                                                                                                                                                                                   |
| Oggetto MaskBlt           | Non viene eseguita alcuna gestione del colore quando si verificano blie.                                                                                                                                                                                                                                                                                                                                                                                             |
| SelectObject      | Se l'oggetto è una bitmap creata con CreateDIBSection, viene eseguita la gestione dei colori. Lo spazio colore della bitmap viene usato come spazio colore di destinazione.                                                                                                                                                                                                                                                                                       |
| SetDIBits         | Viene eseguita la gestione dei colori. Se la struttura BITMAPINFO specificata non è la versione 4 o 5, il profilo colori del controller di dominio corrente viene utilizzato come profilo dello spazio colori di origine. Se non ne ha uno, viene usato lo spazio sRGB. Se la struttura BITMAPINFO specificata è la versione 4 o 5, il profilo dello spazio colore specificato nell'intestazione bitmap viene utilizzato come profilo dello spazio colore di origine.                                         |
| SetDIBitsToDevice | Viene eseguita la gestione dei colori. Se la struttura BITMAPINFO specificata non è la versione 4 o 5, il profilo colori del contesto di dispositivo corrente viene usato come profilo dello spazio colore di origine. Se non ne ha uno, viene usato lo spazio colore sRGB. Se la struttura BITMAPINFO specificata è la versione 4 o 5, il profilo dello spazio colore associato alla bitmap viene utilizzato come spazio colore di origine.                                    |
| SetDIBColorTable  | Non viene eseguita alcuna gestione del colore.                                                                                                                                                                                                                                                                                                                                                                                                              |
| StretchBlt        | Non viene eseguita alcuna gestione del colore quando si verificano blie.                                                                                                                                                                                                                                                                                                                                                                                             |
| StretchDIBits     | Viene eseguita la gestione dei colori. Se la struttura BITMAPINFO specificata non è la versione 4 o 5, il profilo colori del controller di dominio corrente viene utilizzato come profilo dello spazio colori di origine. Se non ne ha uno, viene usato lo spazio sRGB. Se la struttura BITMAPINFO specificata è la versione 4 o 5, il profilo dello spazio colore specificato nell'intestazione bitmap viene utilizzato come profilo dello spazio colore di origine.                                         |



 

 

 




