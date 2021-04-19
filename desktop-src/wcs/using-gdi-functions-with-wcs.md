---
title: Uso delle funzioni GDI con WCS
description: Sono disponibili varie funzioni nell'interfaccia GDI (Graphics Device Interface) che usano o operano sui dati di colore.
ms.assetid: a19ec8b9-11c9-4fde-a99a-7f4a112b49e7
keywords:
- Windows Color System (WCS), Graphics Device Interface (GDI)
- WCS (sistema di colori Windows), GDI (Graphics Device Interface)
- Gestione colori immagine, GDI (Graphics Device Interface)
- gestione dei colori, GDI (Graphics Device Interface)
- colori, interfaccia GDI (Graphics Device Interface)
- GDI (Graphics Device Interface)
- GDI (Graphics Device Interface)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f411d5d91c36bf5d2f2fa82f332c9b15519d800d
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/26/2021
ms.locfileid: "106320084"
---
# <a name="using-gdi-functions-with-wcs"></a>Uso delle funzioni GDI con WCS

Sono disponibili varie funzioni nell'interfaccia GDI (Graphics Device Interface) che usano o operano sui dati di colore. Alcune sono abilitate per l'uso con WCS e altre no. Le funzioni GDI seguenti sono rilevanti per ICM:

-   [Funzioni di contesto del dispositivo con WCS](#device-context-functions-with-wcs)
-   [Funzioni di penna e pennello con WCS](#pen-and-brush-functions-with-wcs)
-   [Funzioni di output di testo con WCS](#text-output-functions-with-wcs)
-   [Funzioni bitmap con WCS](#bitmap-functions-with-wcs)

## <a name="device-context-functions-with-wcs"></a>Funzioni di contesto del dispositivo con WCS



|                    |                                                                                                                                                                                                                                 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CreateCompatibleDC | Se il contesto di dispositivo (DC) passato a questa funzione tramite il relativo parametro hdc è abilitato per ICM, anche il controller di dominio creato dalla funzione è abilitato per ICM. Gli spazi dei colori di origine e di destinazione sono specificati nel controller di dominio. |
| CreateDC           | È possibile abilitare la funzionalità ICM impostando il membro dmICMMethod della struttura DEVMODE a cui punta il parametro pInitData sul valore appropriato. Per informazioni dettagliate, vedere la documentazione di Platform SDK sulla struttura DEVMODE.  |
| ResetDC            | Il profilo colori del contesto di dispositivo specificato dal parametro hdc verrà reimpostato in base alle informazioni contenute nella struttura DEVMODE specificata dal parametro lpInitData.                                                   |



 

## <a name="pen-and-brush-functions-with-wcs"></a>Funzioni di penna e pennello con WCS



|                 |                                                                                                                                               |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Funzioni pennello | Non viene eseguita alcuna gestione dei colori durante la creazione del pennello. Tuttavia, la gestione dei colori viene eseguita quando il pennello è selezionato in un controller di dominio abilitato per ICM. |
| CreatePen       | Non viene eseguita alcuna gestione dei colori durante la creazione della penna. Tuttavia, la gestione dei colori viene eseguita quando il pennello è selezionato in un controller di dominio abilitato per ICM.   |
| ExtCreatePen    | Non viene eseguita alcuna gestione dei colori durante la creazione della penna. Tuttavia, la gestione dei colori viene eseguita quando il pennello è selezionato in un controller di dominio abilitato per ICM.   |
| SelectObject    | Se l'oggetto selezionato è un pennello o una penna, viene eseguita la gestione dei colori.                                                              |
| SetDCBrushColor | La gestione dei colori viene eseguita se WCS è abilitato.                                                                                              |
| SetDCPenColor   | La gestione dei colori viene eseguita se WCS è abilitato.                                                                                              |



 

## <a name="text-output-functions-with-wcs"></a>Funzioni di output di testo con WCS



|              |                                                  |
|--------------|--------------------------------------------------|
| SetBkColor   | La gestione dei colori viene eseguita se WCS è abilitato. |
| SetTextColor | La gestione dei colori viene eseguita se WCS è abilitato. |



 

## <a name="bitmap-functions-with-wcs"></a>Funzioni bitmap con WCS



|                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BitBlt            | Non viene eseguita alcuna gestione dei colori quando si verifica Blits.                                                                                                                                                                                                                                                                                                                                                                                             |
| CreateDIBitmap    | Il parametro fuUsage specifica che il membro bmiColors della struttura BITMAPINFO a cui punta il parametro lpbmi non contiene informazioni sui colori. In caso contrario, non viene eseguita alcuna gestione dei colori per questa bitmap. Per abilitare la gestione dei colori, la bitmap deve usare la versione 4 o la versione 5 della struttura BITMAPINFO. Il contenuto della bitmap risultante non corrisponde al colore dopo la creazione della bitmap. |
| CreateDIBSection  | Se la struttura BITMAPINFO passata tramite il parametro PBMI non è la versione 4 o la versione 5, non viene eseguita alcuna gestione dei colori. Se è la versione 4 o 5, la gestione dei colori è abilitata e lo spazio colore specificato è associato alla bitmap.                                                                                                                                                                                                   |
| MaskBlt           | Non viene eseguita alcuna gestione dei colori quando si verifica Blits.                                                                                                                                                                                                                                                                                                                                                                                             |
| SelectObject      | Se l'oggetto è una bitmap creata con CreateDIBSection, viene eseguita la gestione dei colori. Lo spazio dei colori della bitmap viene utilizzato come spazio colore di destinazione.                                                                                                                                                                                                                                                                                       |
| SetDIBits         | Viene eseguita la gestione dei colori. Se la struttura BITMAPINFO specificata non è la versione 4 o la versione 5, il profilo colori del controller di dominio corrente viene usato come profilo dello spazio dei colori di origine. Se non ne esiste uno, viene usato lo spazio sRGB. Se la struttura BITMAPINFO specificata è la versione 4 o la versione 5, il profilo dello spazio dei colori specificato nell'intestazione bitmap viene usato come profilo dello spazio dei colori di origine.                                         |
| SetDIBitsToDevice | Viene eseguita la gestione dei colori. Se la struttura BITMAPINFO specificata non è la versione 4 o la versione 5, il profilo colori del contesto di dispositivo corrente viene usato come profilo dello spazio dei colori di origine. Se non è disponibile, viene usato lo spazio dei colori di sRGB. Se la struttura BITMAPINFO specificata è la versione 4 o la versione 5, il profilo dello spazio dei colori associato alla bitmap viene usato come spazio dei colori di origine.                                    |
| SetDIBColorTable  | Non viene eseguita alcuna gestione dei colori.                                                                                                                                                                                                                                                                                                                                                                                                              |
| StretchBlt        | Non viene eseguita alcuna gestione dei colori quando si verifica Blits.                                                                                                                                                                                                                                                                                                                                                                                             |
| StretchDIBits     | Viene eseguita la gestione dei colori. Se la struttura BITMAPINFO specificata non è la versione 4 o la versione 5, il profilo colori del controller di dominio corrente viene usato come profilo dello spazio dei colori di origine. Se non ne esiste uno, viene usato lo spazio sRGB. Se la struttura BITMAPINFO specificata è la versione 4 o la versione 5, il profilo dello spazio dei colori specificato nell'intestazione bitmap viene usato come profilo dello spazio dei colori di origine.                                         |



 

 

 




