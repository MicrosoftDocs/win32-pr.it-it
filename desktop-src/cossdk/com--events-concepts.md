---
description: Concetti relativi agli eventi COM+
ms.assetid: 6bfe4852-4029-4dd4-92ad-3061618b1b23
title: Concetti relativi agli eventi COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811dbca17c4e90ba5e8c2bcb8c918ce6634487e5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749087"
---
# <a name="com-events-concepts"></a><span data-ttu-id="a7696-103">Concetti relativi agli eventi COM+</span><span class="sxs-lookup"><span data-stu-id="a7696-103">COM+ Events Concepts</span></span>

<span data-ttu-id="a7696-104">Il servizio eventi COM+ è un sistema di *eventi* automatizzato a regime di controllo libero che archivia le informazioni sugli eventi da autori diversi nel catalogo com+.</span><span class="sxs-lookup"><span data-stu-id="a7696-104">The COM+ events service is an automated, *loosely coupled event* system that stores event information from different publishers in the COM+ catalog.</span></span> <span data-ttu-id="a7696-105">I sottoscrittori possono eseguire una query su questo archivio eventi e selezionare gli eventi per i quali si desiderano sapere.</span><span class="sxs-lookup"><span data-stu-id="a7696-105">Subscribers can query this event store and select the events that they want to hear about.</span></span>

> [!Note]  
> <span data-ttu-id="a7696-106">Un *evento* viene identificato da un metodo in un'interfaccia com+, noto come *metodo di evento*, e viene originato da un server di pubblicazione e inviato al Sottoscrittore o ai sottoscrittori corretti tramite il servizio eventi com+.</span><span class="sxs-lookup"><span data-stu-id="a7696-106">An *event* is identified by a method in a COM+ interface, known as an *event method*, and is originated by a publisher and dispatched to the correct subscriber or subscribers through the COM+ events service.</span></span> <span data-ttu-id="a7696-107">I metodi di evento devono essere denominati in modo univoco e possono contenere solo parametri di input (nessun output o parametri di input/output).</span><span class="sxs-lookup"><span data-stu-id="a7696-107">Event methods must be uniquely named and can contain only input parameters (no output or input/output parameters).</span></span> <span data-ttu-id="a7696-108">Il valore restituito deve essere un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a7696-108">The return value must be an **HRESULT**.</span></span>

 

<span data-ttu-id="a7696-109">Il servizio eventi COM+ gestisce la maggior parte della semantica degli eventi per il server di pubblicazione e il Sottoscrittore.</span><span class="sxs-lookup"><span data-stu-id="a7696-109">The COM+ events service handles most of the event semantics for the publisher and subscriber.</span></span> <span data-ttu-id="a7696-110">Gli editori offrono la pubblicazione di tipi di evento e Sottoscrittori che richiedono tipi di evento dai Publisher.</span><span class="sxs-lookup"><span data-stu-id="a7696-110">Publishers offer to publish event types, and subscribers request event types from publishers.</span></span> <span data-ttu-id="a7696-111">A differenza di un sistema di *eventi strettamente accoppiato* , in cui gli editori devono gestire il sovraccarico della chiamata diretta dei sottoscrittori, il servizio eventi com+ gestisce i dati di sottoscrizione nel catalogo com+, indipendentemente dal server di pubblicazione e dal Sottoscrittore.</span><span class="sxs-lookup"><span data-stu-id="a7696-111">Unlike a *tightly coupled event* system, where publishers must handle the overhead of calling subscribers directly, the COM+ events service maintains subscription data in the COM+ catalog, independent of the publisher and subscriber.</span></span> <span data-ttu-id="a7696-112">Questo semplifica il modello di programmazione per il server di pubblicazione e il Sottoscrittore perché il componente del Sottoscrittore COM+ non deve contenere la logica per la compilazione delle sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="a7696-112">This simplifies the programming model for the publisher and subscriber because the COM+ subscriber component does not need to contain the logic for building subscriptions.</span></span>

<span data-ttu-id="a7696-113">Poiché il ciclo di vita dei dati di sottoscrizione degli eventi COM+ è separato da quello del server di pubblicazione o del Sottoscrittore, le sottoscrizioni possono essere compilate prima che il Sottoscrittore o le applicazioni di pubblicazione siano attive.</span><span class="sxs-lookup"><span data-stu-id="a7696-113">Because the life cycle of the COM+ events subscription data is separate from that of either the publisher or the subscriber, subscriptions can be built prior to either the subscriber or the publisher applications being active.</span></span> <span data-ttu-id="a7696-114">Ciò significa anche che i Publisher e i sottoscrittori possono essere sviluppati e distribuiti separatamente.</span><span class="sxs-lookup"><span data-stu-id="a7696-114">This also means that publishers and subscribers can be developed and deployed separately.</span></span> <span data-ttu-id="a7696-115">Il server di pubblicazione può essere scritto senza conoscere il numero e la posizione dei sottoscrittori.</span><span class="sxs-lookup"><span data-stu-id="a7696-115">The publisher can be written without knowledge of the number and location of the subscribers.</span></span> <span data-ttu-id="a7696-116">I Sottoscrittori utilizzano il servizio eventi COM+ per trovare il server di pubblicazione e gestirne le sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="a7696-116">The subscribers use the COM+ Events service to find the publisher and manage their subscriptions.</span></span>

<span data-ttu-id="a7696-117">Negli argomenti seguenti di questa sezione vengono fornite informazioni dettagliate sugli elementi principali del servizio eventi COM+ e su come utilizzarli.</span><span class="sxs-lookup"><span data-stu-id="a7696-117">The following topics in this section provide detailed information about the core elements of the COM+ events service and how to use them.</span></span>

-   [<span data-ttu-id="a7696-118">Oggetto della classe di evento COM+</span><span class="sxs-lookup"><span data-stu-id="a7696-118">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
-   [<span data-ttu-id="a7696-119">Sottoscrizioni</span><span class="sxs-lookup"><span data-stu-id="a7696-119">Subscriptions</span></span>](subscriptions.md)
-   [<span data-ttu-id="a7696-120">Pubblicazione e distribuzione di eventi in COM+</span><span class="sxs-lookup"><span data-stu-id="a7696-120">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
-   [<span data-ttu-id="a7696-121">Filtro di eventi in COM+</span><span class="sxs-lookup"><span data-stu-id="a7696-121">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
-   [<span data-ttu-id="a7696-122">Uso di eventi COM+ con componenti in coda COM+</span><span class="sxs-lookup"><span data-stu-id="a7696-122">Using COM+ Events with COM+ Queued Components</span></span>](using-com--events-with-com--queued-components.md)

## <a name="related-topics"></a><span data-ttu-id="a7696-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a7696-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7696-124">Considerazioni sulla sicurezza degli eventi COM+</span><span class="sxs-lookup"><span data-stu-id="a7696-124">COM+ Events Security Considerations</span></span>](com--events-security-considerations.md)
</dt> <dt>

[<span data-ttu-id="a7696-125">Attività degli eventi COM+</span><span class="sxs-lookup"><span data-stu-id="a7696-125">COM+ Events Tasks</span></span>](com--events-tasks.md)
</dt> </dl>

 

 



