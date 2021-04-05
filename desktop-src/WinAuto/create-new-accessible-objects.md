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
# <a name="create-new-accessible-objects"></a>Creare nuovi oggetti accessibili

In questo scenario, il server crea un nuovo oggetto accessibile in risposta a ogni richiesta del [**\_ client ObjID**](object-identifiers.md) .

Nell'esempio di codice seguente, un puntatore al controllo viene recuperato dai dati della finestra aggiuntiva. Questo e l'handle di finestra vengono passati al costruttore dell'oggetto AccServer (Custom Accessibility Server). Questo oggetto viene creato ogni volta che viene ricevuto il [**\_ client ObjID**](object-identifiers.md) .

Quando viene creato l'oggetto, il server ottiene un riferimento, che deve essere rilasciato dopo la chiamata a [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), in modo che l'oggetto venga eliminato al termine del client. Si noti che **LresultFromObject** incrementa il conteggio dei riferimenti più volte, ma è responsabilità delle applicazioni client e di Microsoft Active Accessibility Runtime per rilasciare questi riferimenti.


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



 

 




