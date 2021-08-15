---
title: Riutilizzare i puntatori esistenti agli oggetti
description: Riutilizzare i puntatori esistenti agli oggetti
ms.assetid: 7e1610c6-89b2-4e7e-aee5-94a6cab87a22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14571234ee937d2237d3102316665f15a9ab55415042ddaeda749bfaa21e4807
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998121"
---
# <a name="reuse-existing-pointers-to-objects"></a>Riutilizzare i puntatori esistenti agli oggetti

In questo scenario, il server risponde a una richiesta [**CLIENT OBJID \_**](object-identifiers.md) usando ogni volta lo stesso puntatore di interfaccia [**IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

Nel codice di esempio seguente l'oggetto controllo viene recuperato dai dati aggiuntivi della finestra e viene chiamato un metodo del controllo per recuperare l'oggetto server di accessibilità (la classe AccServer definita dall'applicazione), se presente. Se il server di accessibilità non esiste ancora, viene creato.

Quando viene creato, l'oggetto server di accessibilità ha un conteggio dei riferimenti di 1. [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) incrementa il conteggio dei riferimenti più volte, ma questi riferimenti verranno rilasciati al termine dell'esecuzione dell'oggetto da parte del client. Il server rilascia il relativo riferimento quando la finestra di controllo viene distrutta.


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



 

 




