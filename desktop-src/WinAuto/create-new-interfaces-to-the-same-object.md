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
# <a name="create-new-interfaces-to-the-same-object"></a>Crea nuove interfacce per lo stesso oggetto

In questo scenario, il server risponde a ogni richiesta [**del \_ client ObjID**](object-identifiers.md) ottenendo un nuovo puntatore di interfaccia allo stesso oggetto.

Nell'esempio di codice seguente, *m \_ pUIObj* è un puntatore a un oggetto che supporta più di un'interfaccia Component Object Model (com). Anche se viene riutilizzato un oggetto esistente, viene creato un nuovo puntatore di interfaccia ogni volta che viene recuperato l'oggetto, pertanto è necessario decrementare il conteggio dei riferimenti.


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



 

 




