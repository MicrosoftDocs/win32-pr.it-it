---
title: Creare nuove interfacce per lo stesso oggetto
description: Creare nuove interfacce per lo stesso oggetto
ms.assetid: 127c44b6-51a6-4fd6-9edc-9fbe0d08d458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aae1d6328b6d803e4d20207381fe596c5f584fee8281e1e6651ffc2325fb044
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998711"
---
# <a name="create-new-interfaces-to-the-same-object"></a>Creare nuove interfacce per lo stesso oggetto

In questo scenario, il server risponde a ogni [**richiesta OBJID \_ CLIENT**](object-identifiers.md) ottenendo un nuovo puntatore a interfaccia allo stesso oggetto.

Nel codice di esempio seguente *m \_ pUIObj* è un puntatore a un oggetto che supporta più interfacce Component Object Model (COM). Anche se un oggetto esistente viene riutilizzato, viene creato un nuovo puntatore a interfaccia ogni volta che l'oggetto viene recuperato, quindi il conteggio dei riferimenti deve essere decrementato.


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



 

 




