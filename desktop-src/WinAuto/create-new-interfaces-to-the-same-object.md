---
title: Crea nuove interfacce per lo stesso oggetto
description: Crea nuove interfacce per lo stesso oggetto
ms.assetid: 127c44b6-51a6-4fd6-9edc-9fbe0d08d458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b641eed3918af3acbf399427ad5f7427112f399
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298267"
---
# <a name="create-new-interfaces-to-the-same-object"></a><span data-ttu-id="c17bc-103">Crea nuove interfacce per lo stesso oggetto</span><span class="sxs-lookup"><span data-stu-id="c17bc-103">Create New Interfaces to the Same Object</span></span>

<span data-ttu-id="c17bc-104">In questo scenario, il server risponde a ogni richiesta [**del \_ client ObjID**](object-identifiers.md) ottenendo un nuovo puntatore di interfaccia allo stesso oggetto.</span><span class="sxs-lookup"><span data-stu-id="c17bc-104">In this scenario, the server responds to each [**OBJID\_CLIENT**](object-identifiers.md) request by obtaining a new interface pointer to the same object.</span></span>

<span data-ttu-id="c17bc-105">Nell'esempio di codice seguente, *m \_ pUIObj* è un puntatore a un oggetto che supporta più di un'interfaccia Component Object Model (com).</span><span class="sxs-lookup"><span data-stu-id="c17bc-105">In the following example code, *m\_pUIObj* is a pointer to an object that supports more than one Component Object Model (COM) interface.</span></span> <span data-ttu-id="c17bc-106">Anche se viene riutilizzato un oggetto esistente, viene creato un nuovo puntatore di interfaccia ogni volta che viene recuperato l'oggetto, pertanto è necessario decrementare il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="c17bc-106">Even though an existing object is reused, a new interface pointer is created each time the object is retrieved, so the reference count must be decremented.</span></span>


```C++
case WM_GETOBJECT:
   if ((DWORD)lParam == OBJID_CLIENT)
   {
      // Get a new interface to the same object. 
      IAccessible *pAcc = NULL;
      // The following increments the reference count. 
      m_pUIObj->QueryInterface(IID_IAccessible, (LPVOID*)&pAcc); 
      LRESULT lAcc = LresultFromObject(IID_IAccessible, wParam, 
            (LPUNKNOWN) &pAcc); 
      // Release our reference to the object.             
      pAcc->Release();               
      return lAcc;
   }
   break;  // Fall through to DefWindowProc. 
   
```



 

 




