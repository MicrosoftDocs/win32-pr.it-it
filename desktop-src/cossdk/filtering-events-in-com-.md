---
description: 'Gli eventi COM+ forniscono due modi per controllare gli eventi che raggiungono i sottoscrittori: filtro del server di pubblicazione e filtro dei parametri.'
ms.assetid: dfc82a57-5587-462d-a43d-516b7d70e25e
title: Filtro di eventi in COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d3a7d152813e4806a9cfb6a342255e0981ecf37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748863"
---
# <a name="filtering-events-in-com"></a><span data-ttu-id="e9807-103">Filtro di eventi in COM+</span><span class="sxs-lookup"><span data-stu-id="e9807-103">Filtering Events in COM+</span></span>

<span data-ttu-id="e9807-104">Gli eventi COM+ forniscono due modi per controllare gli eventi che raggiungono i sottoscrittori: *filtro del server di pubblicazione* e filtro dei *parametri*.</span><span class="sxs-lookup"><span data-stu-id="e9807-104">COM+ Events provides two ways to control which events reach which subscribers: *publisher filtering* and *parameter filtering*.</span></span>

## <a name="publisher-filtering"></a><span data-ttu-id="e9807-105">Filtro editore</span><span class="sxs-lookup"><span data-stu-id="e9807-105">Publisher Filtering</span></span>

<span data-ttu-id="e9807-106">Il filtro dell'editore controlla l'ordine e l'attivazione di un metodo di evento da parte di un oggetto della [classe di evento](the-com--event-class-object.md) .</span><span class="sxs-lookup"><span data-stu-id="e9807-106">Publisher filtering controls the order and firing of an event method by an [event class](the-com--event-class-object.md) object.</span></span> <span data-ttu-id="e9807-107">Il filtro dell'editore consente al server di pubblicazione di determinare i Sottoscrittori che ricevono un determinato evento.</span><span class="sxs-lookup"><span data-stu-id="e9807-107">Publisher filtering allows the publisher to determine which subscribers receive a particular event.</span></span>

<span data-ttu-id="e9807-108">Un esempio di utilizzo efficace del filtraggio del server di pubblicazione è quello di uno scambio azionario.</span><span class="sxs-lookup"><span data-stu-id="e9807-108">An example of effective use of publisher filtering is that of a stock exchange.</span></span> <span data-ttu-id="e9807-109">La maggior parte dei sottoscrittori vuole scoprire quando viene aggiunta una nuova azione.</span><span class="sxs-lookup"><span data-stu-id="e9807-109">Most subscribers want to know when a new stock is added.</span></span> <span data-ttu-id="e9807-110">Tuttavia, molti di questi stessi Sottoscrittori potrebbero non essere in grado di rilevare ogni volta che viene modificato il prezzo azionario.</span><span class="sxs-lookup"><span data-stu-id="e9807-110">However, many of these same subscribers may not want to know whenever each stock price changes.</span></span> <span data-ttu-id="e9807-111">Il filtro dell'editore fornisce la granularità necessaria per recapitare in modo efficace gli eventi ai soli Sottoscrittori che desiderano queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="e9807-111">Publisher filtering provides the granularity required to effectively deliver events to only the subscribers who want this information.</span></span>

<span data-ttu-id="e9807-112">Quando un metodo viene richiamato sull'oggetto della classe di evento di cui è stata creata un'istanza, raccoglie tutti i filtri del server di pubblicazione su tale metodo.</span><span class="sxs-lookup"><span data-stu-id="e9807-112">When a method is invoked on the instantiated event class object, it collects any publisher filters on that method.</span></span> <span data-ttu-id="e9807-113">Il filtro impone all'oggetto evento di attivare il metodo dell'evento in un Sottoscrittore specifico.</span><span class="sxs-lookup"><span data-stu-id="e9807-113">The filter forces the event object to fire the event method to a specific subscriber.</span></span> <span data-ttu-id="e9807-114">Il filtro determina le sottoscrizioni da attivare e l'ordine in cui eseguirle.</span><span class="sxs-lookup"><span data-stu-id="e9807-114">The filter determines which subscriptions to fire and in which order to fire them.</span></span> <span data-ttu-id="e9807-115">Ad esempio, il filtro può leggere l'elenco di sottoscrizioni e creare l'ordine in base ad alcuni criteri dell'applicazione e quindi chiamare i sottoscrittori in tale ordine.</span><span class="sxs-lookup"><span data-stu-id="e9807-115">For example, the filter could read the subscription list and create the order based on some application criteria and then call the subscribers in that order.</span></span>

<span data-ttu-id="e9807-116">Per istruzioni dettagliate sulla creazione di un filtro dell'editore, vedere [creazione di un filtro di pubblicazione](creating-a-publisher-filter.md).</span><span class="sxs-lookup"><span data-stu-id="e9807-116">For detailed instructions on creating a publisher filter, see [Creating a Publisher Filter](creating-a-publisher-filter.md).</span></span>

## <a name="parameter-filtering"></a><span data-ttu-id="e9807-117">Filtro parametri</span><span class="sxs-lookup"><span data-stu-id="e9807-117">Parameter Filtering</span></span>

<span data-ttu-id="e9807-118">Contrariamente al filtraggio del server di pubblicazione, il servizio eventi COM+ fornisce un filtro facoltativo per i parametri del Sottoscrittore per ogni sottoscrizione e ogni chiamata al metodo di evento.</span><span class="sxs-lookup"><span data-stu-id="e9807-118">In contrast to publisher filtering, the COM+ Events service provides an optional subscriber parameter filtering for each subscription and each event method invocation.</span></span> <span data-ttu-id="e9807-119">Il filtro dei parametri valuta la proprietà FilterCriteria della sottoscrizione rispetto ai parametri del metodo dell'evento.</span><span class="sxs-lookup"><span data-stu-id="e9807-119">Parameter filtering evaluates the subscription FilterCriteria property against the parameters of the event method.</span></span> <span data-ttu-id="e9807-120">Questo tipo di filtro viene usato per ogni singolo metodo e per ogni sottoscrizione e fornisce un livello di filtro dei sottoscrittori nell'origine evento.</span><span class="sxs-lookup"><span data-stu-id="e9807-120">This type of filtering is used on a per-method, per-subscription basis and provides a level of subscriber filtering at the event source.</span></span> <span data-ttu-id="e9807-121">La stringa dei criteri di filtro riconosce gli operatori relazionali per verificare l'uguaglianza (=, = =,!,! =, ~, ~ =,  <>), le parentesi annidate e le parole chiave logiche **and**, **or** o **not**.</span><span class="sxs-lookup"><span data-stu-id="e9807-121">The filter criteria string recognizes relational operators for checking equality (=, ==, !, !=, ~, ~=, <>), nested parentheses, and logical keywords **AND**, **OR**, or **NOT**.</span></span>

<span data-ttu-id="e9807-122">Il filtro dei parametri si verifica dopo il filtro del server di pubblicazione e quando viene attivato l'oggetto evento standard per una determinata sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="e9807-122">Parameter filtering occurs after any publisher filtering and when the standard event object is fired for a given subscription.</span></span> <span data-ttu-id="e9807-123">Se viene utilizzato il filtro del server di pubblicazione, il filtro dei parametri si verifica solo quando il filtro del server di pubblicazione richiama [**IFiringControl:: FireSubscription**](/windows/desktop/api/EventSys/nf-eventsys-ifiringcontrol-firesubscription).</span><span class="sxs-lookup"><span data-stu-id="e9807-123">If publisher filtering is used, parameter filtering occurs only when the publisher filter invokes [**IFiringControl::FireSubscription**](/windows/desktop/api/EventSys/nf-eventsys-ifiringcontrol-firesubscription).</span></span> <span data-ttu-id="e9807-124">Per questo motivo, il filtraggio del server di pubblicazione e il filtro dei parametri possono comporre insieme, ma il filtro del server di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="e9807-124">Because of this, publisher filtering and parameter filtering can compose together but publisher filtering takes precedence.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9807-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e9807-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9807-126">Pubblicazione e distribuzione di eventi in COM+</span><span class="sxs-lookup"><span data-stu-id="e9807-126">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="e9807-127">Sottoscrizioni</span><span class="sxs-lookup"><span data-stu-id="e9807-127">Subscriptions</span></span>](subscriptions.md)
</dt> <dt>

[<span data-ttu-id="e9807-128">Oggetto della classe di evento COM+</span><span class="sxs-lookup"><span data-stu-id="e9807-128">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> <dt>

[<span data-ttu-id="e9807-129">Uso di eventi COM+ con componenti in coda COM+</span><span class="sxs-lookup"><span data-stu-id="e9807-129">Using COM+ Events with COM+ Queued Components</span></span>](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



