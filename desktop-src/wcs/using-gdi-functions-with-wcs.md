---
title: Uso di funzioni GDI con WCS
description: Nell'interfaccia GDI (Graphics Device Interface) sono disponibili varie funzioni che usano o operano sui dati dei colori.
ms.assetid: a19ec8b9-11c9-4fde-a99a-7f4a112b49e7
keywords:
- Windows Color System (WCS), graphics device interface (GDI)
- WCS (Windows Color System),graphics device interface (GDI)
- gestione del colore delle immagini, interfaccia GDI (Graphics Device Interface)
- gestione dei colori, interfaccia GDI (Graphics Device Interface)
- colors,graphics device interface (GDI)
- Graphics Device Interface (GDI)
- GDI (interfaccia del dispositivo grafica)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fad8445623efb8854e81e7e1569beab9ed4169b
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443652"
---
# <a name="using-gdi-functions-with-wcs"></a>Uso di funzioni GDI con WCS

Nell'interfaccia GDI (Graphics Device Interface) sono disponibili varie funzioni che usano o operano sui dati dei colori. Alcuni sono abilitati per l'uso con WCS e altri no. Le funzioni GDI seguenti sono rilevanti per ICM:

-   [Funzioni del contesto di dispositivo con WCS](#device-context-functions-with-wcs)
-   [Funzioni penna e pennello con WCS](#pen-and-brush-functions-with-wcs)
-   [Funzioni di output di testo con WCS](#text-output-functions-with-wcs)
-   [Funzioni bitmap con WCS](#bitmap-functions-with-wcs)

## <a name="device-context-functions-with-wcs"></a>Funzioni del contesto di dispositivo con WCS



|    Funzione                |   Descrizione                                                                                                                                                                                                                              |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CreateCompatibleDC | Se il contesto di dispositivo (DC) passato a questa funzione tramite il relativo parametro hdc è abilitato per ICM, anche il controller di dominio creato dalla funzione è abilitato per ICM. Gli spazi colori di origine e di destinazione vengono specificati nel controller di dominio. |
| CreateDC           | ICM può essere abilitato impostando il membro dmICMMethod della struttura DEVMODE a cui punta il parametro pInitData sul valore appropriato. Per informazioni dettagliate, vedere la documentazione di Platform SDK sulla struttura DEVMODE.  |
| ResetDC            | Il profilo colori del contesto di dispositivo specificato dal parametro hdc verrà reimpostato in base alle informazioni nella struttura DEVMODE specificata dal parametro lpInitData.                                                   |



 

## <a name="pen-and-brush-functions-with-wcs"></a>Funzioni penna e pennello con WCS



|    Funzione                |   Descrizione                                                                                                                                                                                                                              |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Funzioni pennello | Durante la creazione del pennello non viene eseguita alcuna gestione del colore. Tuttavia, la gestione del colore verrà eseguita quando il pennello viene selezionato in un controller di dominio abilitato per ICM. |
| CreatePen       | Durante la creazione della penna non viene eseguita alcuna gestione del colore. Tuttavia, la gestione del colore verrà eseguita quando il pennello viene selezionato in un controller di dominio abilitato per ICM.   |
| ExtCreatePen    | Durante la creazione della penna non viene eseguita alcuna gestione del colore. Tuttavia, la gestione del colore verrà eseguita quando il pennello viene selezionato in un controller di dominio abilitato per ICM.   |
| SelectObject    | Se l'oggetto selezionato è un pennello o una penna, viene eseguita la gestione del colore.                                                              |
| SetDCBrushColor | La gestione del colore viene eseguita se WCS è abilitato.                                                                                              |
| SetDCPenColor   | La gestione del colore viene eseguita se WCS è abilitato.                                                                                              |



 

## <a name="text-output-functions-with-wcs"></a>Funzioni di output di testo con WCS



|    Funzione                |   Descrizione                                                                                                                                                                                                                              |
|--------------|--------------------------------------------------|
| SetBkColor   | La gestione del colore viene eseguita se WCS è abilitato. |
| SetTextColor | La gestione del colore viene eseguita se WCS è abilitato. |



 

## <a name="bitmap-functions-with-wcs"></a>Funzioni bitmap con WCS



|    Funzione                |   Descrizione                                                                                                                                                                                                                              |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bitblt            | Quando si verificano blit, non viene eseguita alcuna gestione del colore.                                                                                                                                                                                                                                                                                                                                                                                             |
| CreateDIBitmap    | Il parametro fuUsage specifica che il membro bmiColors della struttura BITMAPINFO a cui punta il parametro lpbmi non contiene informazioni sul colore. In caso contrario, non viene eseguita alcuna gestione del colore per questa bitmap. La bitmap deve usare la versione 4 o 5 della struttura BITMAPINFO per poter abilitato la gestione dei colori. Il contenuto della bitmap risultante non corrisponde al colore dopo la creazione della bitmap. |
| CreateDIBSection  | Se la struttura BITMAPINFO passata tramite il parametro pbmi non è la versione 4 o 5, non viene eseguita alcuna gestione del colore. Se è la versione 4 o 5, la gestione dei colori è abilitata e lo spazio colore specificato è associato alla bitmap.                                                                                                                                                                                                   |
| MaskBlt           | Quando si verificano blit, non viene eseguita alcuna gestione del colore.                                                                                                                                                                                                                                                                                                                                                                                             |
| SelectObject      | Se l'oggetto è una bitmap creata con CreateDIBSection, viene eseguita la gestione del colore. Lo spazio colori della bitmap viene usato come spazio colore di destinazione.                                                                                                                                                                                                                                                                                       |
| SetDIBits         | Viene eseguita la gestione del colore. Se la struttura BITMAPINFO specificata non è la versione 4 o 5, il profilo colori del controller di dominio corrente viene usato come profilo dello spazio colori di origine. Se non ne ha uno, viene usato lo spazio sRGB. Se la struttura BITMAPINFO specificata è versione 4 o 5, il profilo dello spazio colori specificato nell'intestazione della bitmap viene usato come profilo dello spazio colori di origine.                                         |
| SetDIBitsToDevice | Viene eseguita la gestione del colore. Se la struttura BITMAPINFO specificata non è versione 4 o 5, il profilo colori del contesto di dispositivo corrente viene usato come profilo dello spazio colori di origine. Se non ne ha uno, viene usato lo spazio colori sRGB. Se la struttura BITMAPINFO specificata è versione 4 o 5, come spazio colori di origine viene usato il profilo dello spazio colori associato alla bitmap.                                    |
| SetDIBColorTable  | Non viene eseguita alcuna gestione del colore.                                                                                                                                                                                                                                                                                                                                                                                                              |
| StretchBlt        | Quando si verificano blit, non viene eseguita alcuna gestione del colore.                                                                                                                                                                                                                                                                                                                                                                                             |
| StretchDIBits     | Viene eseguita la gestione del colore. Se la struttura BITMAPINFO specificata non è la versione 4 o 5, il profilo colori del controller di dominio corrente viene usato come profilo dello spazio colori di origine. Se non ne ha uno, viene usato lo spazio sRGB. Se la struttura BITMAPINFO specificata è versione 4 o 5, il profilo dello spazio colori specificato nell'intestazione della bitmap viene usato come profilo dello spazio colori di origine.                                         |



 

 

 




