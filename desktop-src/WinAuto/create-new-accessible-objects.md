---
title: Creare nuovi oggetti accessibili
description: Creare nuovi oggetti accessibili
ms.assetid: d34a52d1-1eb2-4bb4-989c-a1ca4b5d815f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efa85e44d6d51105e6363d276ecb7e5f33d8378
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711092"
---
# <a name="create-new-accessible-objects"></a><span data-ttu-id="eb007-103">Creare nuovi oggetti accessibili</span><span class="sxs-lookup"><span data-stu-id="eb007-103">Create New Accessible Objects</span></span>

<span data-ttu-id="eb007-104">In questo scenario, il server crea un nuovo oggetto accessibile in risposta a ogni richiesta del [**\_ client ObjID**](object-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="eb007-104">In this scenario, the server creates a new accessible object in response to each [**OBJID\_CLIENT**](object-identifiers.md) request.</span></span>

<span data-ttu-id="eb007-105">Nell'esempio di codice seguente, un puntatore al controllo viene recuperato dai dati della finestra aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="eb007-105">In the following example code, a pointer to the control is retrieved from the extra window data.</span></span> <span data-ttu-id="eb007-106">Questo e l'handle di finestra vengono passati al costruttore dell'oggetto AccServer (Custom Accessibility Server).</span><span class="sxs-lookup"><span data-stu-id="eb007-106">This and the window handle are passed to the constructor of the custom accessibility server (AccServer) object.</span></span> <span data-ttu-id="eb007-107">Questo oggetto viene creato ogni volta che viene ricevuto il [**\_ client ObjID**](object-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="eb007-107">This object is created whenever [**OBJID\_CLIENT**](object-identifiers.md) is received.</span></span>

<span data-ttu-id="eb007-108">Quando viene creato l'oggetto, il server ottiene un riferimento, che deve essere rilasciato dopo la chiamata a [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), in modo che l'oggetto venga eliminato al termine del client.</span><span class="sxs-lookup"><span data-stu-id="eb007-108">When the object is created, the server obtains a reference, which must be released after calling [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), so that the object is destroyed as soon as the client is finished with it.</span></span> <span data-ttu-id="eb007-109">Si noti che **LresultFromObject** incrementa il conteggio dei riferimenti più volte, ma è responsabilità delle applicazioni client e di Microsoft Active Accessibility Runtime per rilasciare questi riferimenti.</span><span class="sxs-lookup"><span data-stu-id="eb007-109">Note that **LresultFromObject** increments the reference count several times, but it is the responsibility of client applications, and the Microsoft Active Accessibility runtime, to release these references.</span></span>


```C++
case WM_GETOBJECT:
{
    // Return the IAccessible object. 
    if ((DWORD)lParam == OBJID_CLIENT)
    {
        // Get the control.  
        CustomListControl* pCustomList = (CustomListControl*)(LONG_PTR)GetWindowLongPtr(hwnd, 0);
        AccServer* pAccServer = new AccServer(hwnd, pCustomList);
        if (pAccServer != NULL)  // NULL if out of memory. 
        {
            LRESULT Lresult = LresultFromObject(IID_IAccessible, wParam, pAccServer);
            pAccServer->Release();
            return Lresult;
        }
        else return 0;
    }
    break;
}
```



 

 




