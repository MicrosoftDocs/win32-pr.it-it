---
title: Recuperare gli attributi dell'oggetto, selezionare nuovi oggetti
description: Un'applicazione può recuperare gli attributi per una penna, un pennello, una tavolozza, un tipo di carattere o una bitmap chiamando le funzioni GetCurrentObject e GetObject.
ms.assetid: 09d8412f-a67d-48d5-9c04-9233dee43cf9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c58d946f61a6a83dcfeb2ddae24d735d3596e5e864cf672bab832d7db3aedf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117886147"
---
# <a name="retrieve-object-attributes-select-new-objects"></a>Recuperare gli attributi dell'oggetto, selezionare nuovi oggetti

Un'applicazione può recuperare gli attributi per una penna, un pennello, una tavolozza, un tipo di carattere o una bitmap chiamando le [**funzioni GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) [**e GetObject.**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) La **funzione GetCurrentObject** restituisce un handle che identifica l'oggetto attualmente selezionato nel controller di dominio. La **funzione GetObject** restituisce una struttura che descrive gli attributi dell'oggetto.

L'esempio seguente illustra come un'applicazione può recuperare gli attributi del pennello corrente e usare i dati recuperati per determinare se è necessario selezionare un nuovo pennello.


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
> L'applicazione ha salvato l'handle del pennello originale quando chiama la [**funzione SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) la prima volta. Questo handle viene salvato in modo che il pennello originale possa essere selezionato nuovamente nel controller di dominio dopo il completamento dell'ultima operazione di disegno con il nuovo pennello. Dopo aver selezionato di nuovo il pennello originale nel controller di dominio, il nuovo pennello viene eliminato, liberando memoria nell'heap GDI.

 

 

 



