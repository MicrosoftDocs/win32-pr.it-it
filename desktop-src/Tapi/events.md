---
description: Gli eventi sono una parte essenziale della gestione delle chiamate in TAPI 3. La gestione degli eventi include quattro fasi.
ms.assetid: db43f4e0-f2f5-49b1-a03d-3df3de0e5611
title: Eventi (API di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a9a7d994c7bc9f8019224d826d586d698bc605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529071"
---
# <a name="events-telephony-api"></a><span data-ttu-id="c31c1-104">Eventi (API di telefonia)</span><span class="sxs-lookup"><span data-stu-id="c31c1-104">Events (Telephony API)</span></span>

<span data-ttu-id="c31c1-105">Gli eventi sono una parte essenziale della gestione delle chiamate in TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="c31c1-105">Events are a crucial part of call handling under TAPI 3.</span></span> <span data-ttu-id="c31c1-106">La gestione degli eventi include quattro fasi.</span><span class="sxs-lookup"><span data-stu-id="c31c1-106">Event handling includes four stages.</span></span>

<span data-ttu-id="c31c1-107">**Per eseguire la registrazione e abilitare la ricezione di eventi**</span><span class="sxs-lookup"><span data-stu-id="c31c1-107">**To register for and enable the reception of events**</span></span>

1.  <span data-ttu-id="c31c1-108">Implementare il metodo [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) .</span><span class="sxs-lookup"><span data-stu-id="c31c1-108">Implement the [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) method.</span></span> <span data-ttu-id="c31c1-109">Questo metodo viene chiamato da TAPI quando si verifica un evento. In genere, questa implementazione non supera **AddRef** il puntatore all'interfaccia **IDispatch** , quindi Invia un post al message pump dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c31c1-109">(TAPI calls this method when an event occurs.) Typically, this implementation does no more than **AddRef** the **IDispatch** interface pointer, then post to the application's message pump.</span></span>
2.  <span data-ttu-id="c31c1-110">Registrare l'interfaccia in uscita [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) usando le interfacce [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) e [**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint) standard com e passare il metodo [**IConnectionPoint:: Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) un puntatore a [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event).</span><span class="sxs-lookup"><span data-stu-id="c31c1-110">Register the [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) outgoing interface using the COM standard [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) and [**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint) interfaces, and pass the [**IConnectionPoint::Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) method a pointer to [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event).</span></span>
3.  <span data-ttu-id="c31c1-111">Chiamare il metodo [**ITTAPI::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) per indicare a TAPI gli eventi che l'applicazione gestirà.</span><span class="sxs-lookup"><span data-stu-id="c31c1-111">Call the [**ITTAPI::put\_EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) method to tell TAPI which events the application will handle.</span></span> <span data-ttu-id="c31c1-112">Il filtro eventi è costituito dai membri **o** dell'enumerazione di [**\_ eventi TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) .</span><span class="sxs-lookup"><span data-stu-id="c31c1-112">The event filter consists of **OR** ed members of the [**TAPI\_EVENT**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) enumeration.</span></span>
    > [!Note]  
    > <span data-ttu-id="c31c1-113">È necessario chiamare il metodo **ITTAPI::p UT \_ EventFilter** per impostare la maschera di filtro eventi e abilitare la ricezione di eventi.</span><span class="sxs-lookup"><span data-stu-id="c31c1-113">You must call the **ITTAPI::put\_EventFilter** method to set the event filter mask and enable reception of events.</span></span> <span data-ttu-id="c31c1-114">Se non si chiama **ITTAPI::p UT \_ EventFilter**, l'applicazione non riceverà alcun evento.</span><span class="sxs-lookup"><span data-stu-id="c31c1-114">If you do not call **ITTAPI::put\_EventFilter**, your application will not receive any events.</span></span>

     

<span data-ttu-id="c31c1-115">È anche necessario chiamare il metodo [**ITTAPI:: RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) per ogni oggetto Address su cui l'applicazione gestirà le chiamate.</span><span class="sxs-lookup"><span data-stu-id="c31c1-115">You must also call the [**ITTAPI::RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) method for each address object on which the application will handle calls.</span></span>

<span data-ttu-id="c31c1-116">Per un elenco di tutte le interfacce eventi, vedere [interfacce eventi](./event-interfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="c31c1-116">See [Event Interfaces](./event-interfaces.md) for a list of all event interfaces.</span></span> <span data-ttu-id="c31c1-117">Vedere [registrare gli eventi](register-events.md) per esempi di codice che illustrano il processo di registrazione e [ricevono una chiamata](receive-a-call.md) per un esempio di codice che mostra un uso di eventi.</span><span class="sxs-lookup"><span data-stu-id="c31c1-117">See [Register Events](register-events.md) for code examples that illustrate the registration process and [Receive a Call](receive-a-call.md) for a code example that shows one use of events.</span></span>

 

 
