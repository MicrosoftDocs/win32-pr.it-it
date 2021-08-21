---
title: Creare nuovi oggetti accessibili
description: Creare nuovi oggetti accessibili
ms.assetid: d34a52d1-1eb2-4bb4-989c-a1ca4b5d815f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaaa9ee8669199a9f4de938b4e1cb9e6dd24336bd86527a2cc528709e303543e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052819"
---
# <a name="create-new-accessible-objects"></a>Creare nuovi oggetti accessibili

In questo scenario, il server crea un nuovo oggetto accessibile in risposta a ogni [**richiesta OBJID \_ CLIENT.**](object-identifiers.md)

Nel codice di esempio seguente un puntatore al controllo viene recuperato dai dati aggiuntivi della finestra. Questo e l'handle di finestra vengono passati al costruttore dell'oggetto del server di accessibilità personalizzato (AccServer). Questo oggetto viene creato ogni volta [**che viene ricevuto OBJID \_ CLIENT.**](object-identifiers.md)

Quando l'oggetto viene creato, il server ottiene un riferimento, che deve essere rilasciato dopo la chiamata di [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), in modo che l'oggetto viene eliminato non appena il client lo completa. Si noti che **LresultFromObject** incrementa il conteggio dei riferimenti più volte, ma è responsabilità delle applicazioni client e del runtime Microsoft Active Accessibility rilasciare questi riferimenti.


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



 

 




