---
title: Annullamento di chiamate al metodo
description: Con l'introduzione di applicazioni distribuite e basate sul Web, alcune chiamate al metodo possono richiedere un tempo inaccettabile per la restituzione.
ms.assetid: 18228ff1-8c1c-430a-ae5f-0e9a56b0fe3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e2a78f042e528036135df4865e8a454cd687da
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300520"
---
# <a name="canceling-method-calls"></a><span data-ttu-id="508b0-103">Annullamento di chiamate al metodo</span><span class="sxs-lookup"><span data-stu-id="508b0-103">Canceling Method Calls</span></span>

<span data-ttu-id="508b0-104">Con l'introduzione di applicazioni distribuite e basate sul Web, alcune chiamate al metodo possono richiedere un tempo inaccettabile per la restituzione.</span><span class="sxs-lookup"><span data-stu-id="508b0-104">With the introduction of distributed and Web-based applications, some method calls can take an unacceptably long time to return.</span></span> <span data-ttu-id="508b0-105">La latenza della connessione di rete potrebbe essere elevata, il computer server potrebbe servire molti client o il componente server può passare una grande quantità di dati, ad esempio un file multimediale.</span><span class="sxs-lookup"><span data-stu-id="508b0-105">The latency of the network connection may be high, the server machine may be serving many clients, or the server component may be passing a large amount of data, such as a multimedia file.</span></span> <span data-ttu-id="508b0-106">Gli utenti devono essere in grado di annullare una richiesta che sta richiedendo troppo tempo e l'applicazione deve essere in grado di gestire le richieste di annullamento e continuare con le altre attività.</span><span class="sxs-lookup"><span data-stu-id="508b0-106">Users should be able to cancel a request that is taking too long, and the application should be able to handle cancellation requests and continue with its other work.</span></span> <span data-ttu-id="508b0-107">In COM, è possibile usare l'interfaccia [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) per annullare una chiamata in sospeso originata da un Apartment a thread singolo.</span><span class="sxs-lookup"><span data-stu-id="508b0-107">In COM, you can use the [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) interface to cancel a pending call that originates from a single-threaded apartment.</span></span>

<span data-ttu-id="508b0-108">Quando viene effettuato il marshalling di una chiamata, il proxy crea un oggetto Cancel, che implementa l'interfaccia [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) .</span><span class="sxs-lookup"><span data-stu-id="508b0-108">When a call is marshaled, the proxy creates a cancel object, which implements the [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) interface.</span></span> <span data-ttu-id="508b0-109">L'oggetto Cancel è associato sia alla chiamata che al thread in cui la chiamata è in sospeso.</span><span class="sxs-lookup"><span data-stu-id="508b0-109">The cancel object is associated with both the call and the thread on which the call is pending.</span></span>

<span data-ttu-id="508b0-110">Per annullare la chiamata in sospeso, il client passa una richiesta di annullamento tramite l'oggetto Cancel, che gestisce i dettagli della notifica all'oggetto server che la chiamata è stata annullata.</span><span class="sxs-lookup"><span data-stu-id="508b0-110">To cancel the pending call, the client passes a cancellation request through the cancel object, which handles the details of notifying the server object that the call has been canceled.</span></span> <span data-ttu-id="508b0-111">Se il metodo chiamato non ha restituito, l'oggetto server, durante il rilevamento della richiesta di annullamento, pulisce tutte le risorse del programma che ha allocato e invia una notifica al client, restituendo un valore **HRESULT** appropriato, che ha annullato l'esecuzione della chiamata.</span><span class="sxs-lookup"><span data-stu-id="508b0-111">If the called method has not returned, the server object, on detecting the cancellation request, cleans up any program resources it has allocated and notifies its client, by returning an appropriate **HRESULT** value, that it canceled execution of the call.</span></span> <span data-ttu-id="508b0-112">Se il metodo chiamato è già stato restituito, l'oggetto Cancel invia una notifica al client.</span><span class="sxs-lookup"><span data-stu-id="508b0-112">If the called method has already returned, the cancel object notifies the client.</span></span> <span data-ttu-id="508b0-113">In entrambi i casi, il thread client viene sbloccato e può continuare l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="508b0-113">In either case, the client thread is unblocked and can continue processing.</span></span>

<span data-ttu-id="508b0-114">Il modo in cui l'oggetto server risponde a una richiesta di annullamento è a discrezione dell'implementatore del server, ma il thread chiamante sul client sarà sempre sbloccato e ignorerà i risultati che il server tenterà di passare.</span><span class="sxs-lookup"><span data-stu-id="508b0-114">How the server object responds to a cancellation request is at the discretion of the server implementer, but the calling thread on the client will always be unblocked and will ignore whatever results the server tries to pass to it.</span></span> <span data-ttu-id="508b0-115">Gli oggetti Cancel forniscono un mezzo per richiedere che un metodo attualmente in esecuzione venga annullato, ma non vi è alcuna garanzia che l'oggetto server arresterà l'elaborazione della chiamata.</span><span class="sxs-lookup"><span data-stu-id="508b0-115">Cancel objects provide a means to request that a currently running method be canceled, but there is no guarantee that the server object will stop processing the call.</span></span> <span data-ttu-id="508b0-116">Ad esempio, è possibile che la chiamata sia già stata restituita oppure che l'oggetto server non supporti l'annullamento degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="508b0-116">For example, the call may have already returned, or the server object may not support cancel objects.</span></span>

<span data-ttu-id="508b0-117">COM fornisce automaticamente un'implementazione standard degli oggetti Cancel per gli oggetti e le interfacce client che utilizzano il marshalling standard.</span><span class="sxs-lookup"><span data-stu-id="508b0-117">COM automatically provides a standard implementation of cancel objects for client objects and interfaces that use standard marshaling.</span></span> <span data-ttu-id="508b0-118">Per gli oggetti e le interfacce che usano il marshalling personalizzato, sarà necessario implementare un oggetto Cancel personalizzato.</span><span class="sxs-lookup"><span data-stu-id="508b0-118">For objects and interfaces that use custom marshaling, you will need to implement your own cancel object.</span></span>

<span data-ttu-id="508b0-119">Al momento, gli oggetti Cancel gestiscono solo le chiamate sincrone.</span><span class="sxs-lookup"><span data-stu-id="508b0-119">At this time, cancel objects handle only synchronous calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="508b0-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="508b0-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="508b0-121">Annullamento di una chiamata asincrona</span><span class="sxs-lookup"><span data-stu-id="508b0-121">Canceling an Asynchronous Call</span></span>](canceling-an-asynchronous-call.md)
</dt> <dt>

[<span data-ttu-id="508b0-122">**CoGetCancelObject**</span><span class="sxs-lookup"><span data-stu-id="508b0-122">**CoGetCancelObject**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcancelobject)
</dt> <dt>

[<span data-ttu-id="508b0-123">**CoSetCancelObject**</span><span class="sxs-lookup"><span data-stu-id="508b0-123">**CoSetCancelObject**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cosetcancelobject)
</dt> <dt>

[<span data-ttu-id="508b0-124">**CoTestCancel**</span><span class="sxs-lookup"><span data-stu-id="508b0-124">**CoTestCancel**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotestcancel)
</dt> </dl>

 

 