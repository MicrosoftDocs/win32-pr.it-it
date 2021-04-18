---
title: Come generare eventi da un provider di automazione interfaccia utente
description: Questo argomento contiene codice di esempio che illustra come un provider di automazione interfaccia utente Microsoft genera un evento.
ms.assetid: 43826258-9321-4d44-bd31-6a3b42f00d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417c86771c24cc1a67fd907aaf0628037edce44d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298757"
---
# <a name="how-to-raise-events-from-a-ui-automation-provider"></a>Come generare eventi da un provider di automazione interfaccia utente

Questo argomento contiene codice di esempio che illustra come un provider di automazione interfaccia utente Microsoft genera un evento.

Nell'esempio di codice seguente viene illustrato un metodo da un'applicazione che implementa un pulsante personalizzato. L'applicazione chiama il metodo ogni volta che viene richiamato il pulsante personalizzato. Il metodo controlla se tutti i client sono in ascolto di eventi e, in caso affermativo, genera l'evento di [**\_ richiamo \_ InvokedEventId**](uiauto-event-ids.md) per la notifica ai client che il pulsante è stato richiamato.


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

[Procedure per i provider di automazione interfaccia utente](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




