---
title: Recupera attributi oggetto, seleziona nuovi oggetti
description: Un'applicazione può recuperare gli attributi per una penna, un pennello, una tavolozza, un tipo di carattere o una bitmap chiamando le funzioni GetCurrentObject e GetObject.
ms.assetid: 09d8412f-a67d-48d5-9c04-9233dee43cf9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b18dcef03bf769e8b2d11574429b64f481b1a79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978303"
---
# <a name="retrieve-object-attributes-select-new-objects"></a>Recupera attributi oggetto, seleziona nuovi oggetti

Un'applicazione può recuperare gli attributi per una penna, un pennello, una tavolozza, un tipo di carattere o una bitmap chiamando le funzioni [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) e [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) . La funzione **GetCurrentObject** restituisce un handle che identifica l'oggetto attualmente selezionato nel controller di dominio; la funzione **GetObject** restituisce una struttura che descrive gli attributi dell'oggetto.

Nell'esempio seguente viene illustrato come un'applicazione può recuperare gli attributi del pennello correnti e utilizzare i dati recuperati per determinare se è necessario selezionare un nuovo pennello.


```C++
    HDC hdc;                     // display DC handle  
    HBRUSH hbrushNew, hbrushOld; // brush handles  
    HBRUSH hbrush;               // brush handle  
    LOGBRUSH lb;                 // logical-brush structure  
 
    // Retrieve a handle identifying the current brush.  
 
    hbrush = GetCurrentObject(hdc, OBJ_BRUSH); 
 
    // Retrieve a LOGBRUSH structure that contains the  
    // current brush attributes.  
 
    GetObject(hbrush, sizeof(LOGBRUSH), &lb); 
 
    // If the current brush is not a solid-black brush,  
    // replace it with the solid-black stock brush.  
 
    if ((lb.lbStyle != BS_SOLID) 
           || (lb.lbColor != 0x000000)) 
    { 
        hbrushNew = GetStockObject(BLACK_BRUSH); 
        hbrushOld = SelectObject(hdc, hbrushNew); 
    } 
 
    // Perform painting operations with the white brush.  
 
 
    // After completing the last painting operation with the new  
    // brush, the application should select the original brush back  
    // into the device context and delete the new brush.  
    // In this example, hbrushNew contains a handle to a stock object.  
    // It is not necessary (but it is not harmful) to call  
    // DeleteObject on a stock object. If hbrushNew contained a handle  
    // to a brush created by a function such as CreateBrushIndirect,  
    // it would be necessary to call DeleteObject.  
 
    SelectObject(hdc, hbrushOld); 
    DeleteObject(hbrushNew); 
```



> [!Note]
>
> L'applicazione ha salvato il pennello originale per la prima volta chiamando la funzione [**SelezionaOggetto**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) . Questo handle viene salvato in modo che il pennello originale possa essere nuovamente selezionato nel controller di dominio dopo che l'ultima operazione di disegno è stata completata con il nuovo pennello. Dopo aver selezionato di nuovo il pennello originale nel controller di dominio, il nuovo pennello viene eliminato, liberando la memoria nell'heap GDI.

 

 

 



