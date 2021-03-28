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
# <a name="retrieve-object-attributes-select-new-objects"></a><span data-ttu-id="35c51-103">Recupera attributi oggetto, seleziona nuovi oggetti</span><span class="sxs-lookup"><span data-stu-id="35c51-103">Retrieve object attributes, select new objects</span></span>

<span data-ttu-id="35c51-104">Un'applicazione può recuperare gli attributi per una penna, un pennello, una tavolozza, un tipo di carattere o una bitmap chiamando le funzioni [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) e [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) .</span><span class="sxs-lookup"><span data-stu-id="35c51-104">An application can retrieve the attributes for a pen, brush, palette, font, or bitmap by calling the [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) and [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) functions.</span></span> <span data-ttu-id="35c51-105">La funzione **GetCurrentObject** restituisce un handle che identifica l'oggetto attualmente selezionato nel controller di dominio; la funzione **GetObject** restituisce una struttura che descrive gli attributi dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="35c51-105">The **GetCurrentObject** function returns a handle identifying the object currently selected into the DC; the **GetObject** function returns a structure that describes the attributes of the object.</span></span>

<span data-ttu-id="35c51-106">Nell'esempio seguente viene illustrato come un'applicazione può recuperare gli attributi del pennello correnti e utilizzare i dati recuperati per determinare se è necessario selezionare un nuovo pennello.</span><span class="sxs-lookup"><span data-stu-id="35c51-106">The following example shows how an application can retrieve the current brush attributes and use the retrieved data to determine whether it is necessary to select a new brush.</span></span>


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
> <span data-ttu-id="35c51-107">L'applicazione ha salvato il pennello originale per la prima volta chiamando la funzione [**SelezionaOggetto**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) .</span><span class="sxs-lookup"><span data-stu-id="35c51-107">The application saved the original brush handle when calling the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function the first time.</span></span> <span data-ttu-id="35c51-108">Questo handle viene salvato in modo che il pennello originale possa essere nuovamente selezionato nel controller di dominio dopo che l'ultima operazione di disegno è stata completata con il nuovo pennello.</span><span class="sxs-lookup"><span data-stu-id="35c51-108">This handle is saved so that the original brush can be selected back into the DC after the last painting operation has been completed with the new brush.</span></span> <span data-ttu-id="35c51-109">Dopo aver selezionato di nuovo il pennello originale nel controller di dominio, il nuovo pennello viene eliminato, liberando la memoria nell'heap GDI.</span><span class="sxs-lookup"><span data-stu-id="35c51-109">After the original brush is selected back into the DC, the new brush is deleted, freeing memory in the GDI heap.</span></span>

 

 

 



