---
title: Riutilizza puntatori esistenti a oggetti
description: Riutilizza puntatori esistenti a oggetti
ms.assetid: 7e1610c6-89b2-4e7e-aee5-94a6cab87a22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c151b8d957fb82718721ad81b452a81a2c71ec84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297904"
---
# <a name="reuse-existing-pointers-to-objects"></a><span data-ttu-id="ab55d-103">Riutilizza puntatori esistenti a oggetti</span><span class="sxs-lookup"><span data-stu-id="ab55d-103">Reuse Existing Pointers to Objects</span></span>

<span data-ttu-id="ab55d-104">In questo scenario, il server risponde a una richiesta [**del \_ client ObjID**](object-identifiers.md) utilizzando ogni volta lo stesso puntatore di interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="ab55d-104">In this scenario, the server responds to an [**OBJID\_CLIENT**](object-identifiers.md) request using the same [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer each time.</span></span>

<span data-ttu-id="ab55d-105">Nell'esempio di codice seguente, l'oggetto controllo viene recuperato dai dati della finestra aggiuntiva e viene chiamato un metodo del controllo per recuperare l'oggetto server di accessibilità (la classe AccServer definita dall'applicazione), se disponibile.</span><span class="sxs-lookup"><span data-stu-id="ab55d-105">In the following example code, the control object is retrieved from the extra window data, and a method of the control is called to retrieve the accessibility server object (the application-defined AccServer class), if any.</span></span> <span data-ttu-id="ab55d-106">Se il server di accessibilità non esiste ancora, viene creato.</span><span class="sxs-lookup"><span data-stu-id="ab55d-106">If the accessibility server does not yet exist, it is created.</span></span>

<span data-ttu-id="ab55d-107">Quando viene creato l'oggetto server di accessibilità, il conteggio dei riferimenti è 1.</span><span class="sxs-lookup"><span data-stu-id="ab55d-107">When the accessibility server object is created, it has a reference count of 1.</span></span> <span data-ttu-id="ab55d-108">[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) incrementa il conteggio dei riferimenti più volte, ma questi riferimenti verranno rilasciati al termine dell'oggetto del client.</span><span class="sxs-lookup"><span data-stu-id="ab55d-108">[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) increments the reference count several times, but these references will be released when the client is finished with the object.</span></span> <span data-ttu-id="ab55d-109">Il server rilascia il riferimento quando la finestra del controllo viene distrutta.</span><span class="sxs-lookup"><span data-stu-id="ab55d-109">The server releases its reference when the control window is destroyed.</span></span>


```C++
case WM_GETOBJECT:
    {
        // Return the IAccessible object. 
        if ((DWORD)lParam == (DWORD)OBJID_CLIENT)
        {
            // Get the control.  
            CustomListControl* pCustomList = (CustomListControl*)(LONG_PTR)GetWindowLongPtr(hwnd, 0);
            // Create the accessible object. 
            AccServer* pAccServer = pCustomList->GetAccServer();
            if (pAccServer == NULL)
            {
                pAccServer = new AccServer(hwnd, pCustomList);
                pCustomList->SetAccServer(pAccServer);
            }
            if (pAccServer != NULL)  // NULL if out of memory. 
            {
                LRESULT Lresult = LresultFromObject(IID_IAccessible, wParam, pAccServer);
                return Lresult;
            }
            else return 0;
        }
        break;
    }

    
case WM_DESTROY:
    {
    CustomListControl* pCustomList = (CustomListControl*)(LONG_PTR)GetWindowLongPtr(hwnd, 0);
    AccServer* pAccServer = pCustomList->GetAccServer();
    if (pAccServer!= NULL)
    {
        // Notify the accessibility object that the control no longer exists. 
        pAccServer->SetControlIsAlive(false);
        // Release the reference created in WM_GETOBJECT. 
        pAccServer->Release(); 
    }   
    // Destroy the control. 
    delete pCustomList;
     break;
    }
```



 

 




