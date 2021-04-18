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
# <a name="how-to-raise-events-from-a-ui-automation-provider"></a><span data-ttu-id="d76e2-103">Come generare eventi da un provider di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="d76e2-103">How to Raise Events from a UI Automation Provider</span></span>

<span data-ttu-id="d76e2-104">Questo argomento contiene codice di esempio che illustra come un provider di automazione interfaccia utente Microsoft genera un evento.</span><span class="sxs-lookup"><span data-stu-id="d76e2-104">This topic contains example code that shows how a Microsoft UI Automation provider raises an event.</span></span>

<span data-ttu-id="d76e2-105">Nell'esempio di codice seguente viene illustrato un metodo da un'applicazione che implementa un pulsante personalizzato.</span><span class="sxs-lookup"><span data-stu-id="d76e2-105">The following example code shows a method from an application that implements a custom button.</span></span> <span data-ttu-id="d76e2-106">L'applicazione chiama il metodo ogni volta che viene richiamato il pulsante personalizzato.</span><span class="sxs-lookup"><span data-stu-id="d76e2-106">The application calls the method whenever the custom button is invoked.</span></span> <span data-ttu-id="d76e2-107">Il metodo controlla se tutti i client sono in ascolto di eventi e, in caso affermativo, genera l'evento di [**\_ richiamo \_ InvokedEventId**](uiauto-event-ids.md) per la notifica ai client che il pulsante è stato richiamato.</span><span class="sxs-lookup"><span data-stu-id="d76e2-107">The method checks whether any clients are listening for events and, if so, raises the [**UIA\_Invoke\_InvokedEventId**](uiauto-event-ids.md) event to notify the clients that the button was invoked.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d76e2-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d76e2-108">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d76e2-109">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="d76e2-109">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d76e2-110">Cenni preliminari sugli eventi di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="d76e2-110">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

[<span data-ttu-id="d76e2-111">Procedure per i provider di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="d76e2-111">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




