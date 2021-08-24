---
title: Come generare eventi da un provider Automazione interfaccia utente
description: Questo argomento contiene codice di esempio che illustra come un provider microsoft Automazione interfaccia utente genera un evento .
ms.assetid: 43826258-9321-4d44-bd31-6a3b42f00d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75717dfcccaca5f62ac3431f9b3decb01842ce9bc696d07bfff54f35ffc13640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133294"
---
# <a name="how-to-raise-events-from-a-ui-automation-provider"></a>Come generare eventi da un provider Automazione interfaccia utente

Questo argomento contiene codice di esempio che illustra come un provider microsoft Automazione interfaccia utente genera un evento .

Nell'esempio di codice seguente viene illustrato un metodo da un'applicazione che implementa un pulsante personalizzato. L'applicazione chiama il metodo ogni volta che viene richiamato il pulsante personalizzato. Il metodo controlla se alcuni client sono in ascolto di eventi e, in tal caso, genera l'evento [**\_ \_ InvokedEventId**](uiauto-event-ids.md) di UIA per notificare ai client che il pulsante è stato richiamato.


```C++
// Responds to a button click. The source of the click could 
// be the mouse, the keyboard, or a client's call to 
// IUIAutomationInvokePattern::Invoke.
void CustomButton::InvokeButton(HWND hwnd)
{
    // TODO: Perform program actions invoked by the control.

    // Check whether any clients are listening for UI Automation 
    // events.
    if (UiaClientsAreListening())
    {
        // Raise an Invoked event. GetUIAutomationProvider is an
        // application-defined method that returns a pointer to
        // the application's IRawElementProviderSimple interface.
        UiaRaiseAutomationEvent(
            GetUIAutomationProvider(hwnd), UIA_Invoke_InvokedEventId); 
    }
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sugli eventi di automazione interfaccia utente](uiauto-eventsoverview.md)
</dt> <dt>

[Procedure per i provider di Automazione interfaccia utente](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




