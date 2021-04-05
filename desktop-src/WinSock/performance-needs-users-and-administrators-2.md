---
description: Esigenze di prestazioni degli utenti e degli amministratori con le applicazioni Windows Sockets (Winsock).
ms.assetid: 6c4365c6-a406-497b-a313-1faeb3e3b7f5
title: 'Esigenze di prestazioni: utenti e amministratori'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009a8178cf1d7516e9c16493916f8cf911752b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049478"
---
# <a name="performance-needs-users-and-administrators"></a><span data-ttu-id="e5e39-103">Esigenze di prestazioni: utenti e amministratori</span><span class="sxs-lookup"><span data-stu-id="e5e39-103">Performance Needs: Users and Administrators</span></span>

<span data-ttu-id="e5e39-104">Gli utenti possono valutare le prestazioni delle applicazioni in base alla loro esperienza:</span><span class="sxs-lookup"><span data-stu-id="e5e39-104">Users judge application performance by their experience:</span></span>

-   <span data-ttu-id="e5e39-105">L'applicazione è pronta per rispondere?</span><span class="sxs-lookup"><span data-stu-id="e5e39-105">Is the application quick to respond?</span></span>
-   <span data-ttu-id="e5e39-106">Icona a forma di clessidra visualizzata durante l'esecuzione delle operazioni in background.</span><span class="sxs-lookup"><span data-stu-id="e5e39-106">Is an hourglass icon displayed while background operations are carried out?</span></span>
-   <span data-ttu-id="e5e39-107">L'applicazione viene avviata e chiusa rapidamente?</span><span class="sxs-lookup"><span data-stu-id="e5e39-107">Does the application launch and close quickly?</span></span>
-   <span data-ttu-id="e5e39-108">Gli errori vengono gestiti in modo comprensibile?</span><span class="sxs-lookup"><span data-stu-id="e5e39-108">Are errors handled in an understandable way?</span></span>

<span data-ttu-id="e5e39-109">Per riepilogare, gli utenti desiderano che le applicazioni siano veloci e prevedibili.</span><span class="sxs-lookup"><span data-stu-id="e5e39-109">To summarize, users want applications to be fast and predictable.</span></span>

<span data-ttu-id="e5e39-110">Al contrario, gli amministratori spesso giudicano le prestazioni di un'applicazione sull'efficienza dell'utilizzo delle risorse di rete.</span><span class="sxs-lookup"><span data-stu-id="e5e39-110">In contrast, administrators often judge an application's performance on how efficiently it uses network resources.</span></span> <span data-ttu-id="e5e39-111">Gli amministratori possono richiedere:</span><span class="sxs-lookup"><span data-stu-id="e5e39-111">Administrators may ask:</span></span>

-   <span data-ttu-id="e5e39-112">L'applicazione ha un sovraccarico ridotto e un utilizzo efficiente della rete?</span><span class="sxs-lookup"><span data-stu-id="e5e39-112">Does the application have low overhead and efficient network usage?</span></span>
-   <span data-ttu-id="e5e39-113">Il numero minimo di connessioni viene utilizzato, quindi il server può servire il maggior numero possibile di utenti in una sola volta?</span><span class="sxs-lookup"><span data-stu-id="e5e39-113">Are the minimum number of connections used, so my server can service as many users at once as possible?</span></span>
-   <span data-ttu-id="e5e39-114">Sto chiamando sempre helpdesk?</span><span class="sxs-lookup"><span data-stu-id="e5e39-114">Am I constantly calling helpdesk?</span></span>

<span data-ttu-id="e5e39-115">In breve, gli amministratori desiderano la scalabilità delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e5e39-115">In short, administrators want applications to scale.</span></span>

## <a name="best-practices-for-performance-needs"></a><span data-ttu-id="e5e39-116">Procedure consigliate per le esigenze di prestazioni</span><span class="sxs-lookup"><span data-stu-id="e5e39-116">Best Practices for Performance Needs</span></span>

<span data-ttu-id="e5e39-117">Quando si sviluppa un'applicazione Windows Sockets, questi requisiti di prestazioni vengono convertiti in regole utili.</span><span class="sxs-lookup"><span data-stu-id="e5e39-117">When developing a Windows Sockets application, these performance requirements translate into useful rules.</span></span>

-   <span data-ttu-id="e5e39-118">L'inizializzazione delle applicazioni di rete è rapida.</span><span class="sxs-lookup"><span data-stu-id="e5e39-118">Have network applications initialize quickly.</span></span>

    <span data-ttu-id="e5e39-119">L'interfaccia utente non deve attendere la risposta alla rete.</span><span class="sxs-lookup"><span data-stu-id="e5e39-119">The user interface should not have to wait for network responses.</span></span> <span data-ttu-id="e5e39-120">Alcune attività possono essere eseguite prima che la rete sia disponibile o senza la rete.</span><span class="sxs-lookup"><span data-stu-id="e5e39-120">Some tasks can be performed before the network is available, or without the network.</span></span> <span data-ttu-id="e5e39-121">Se la rete non risponde, l'utente potrebbe avere bisogno dell'interfaccia utente per operazioni semplici, ad esempio la chiusura dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e5e39-121">If the network is not responding, the user may need the user interface for simple operations, such as closing the application.</span></span>

-   <span data-ttu-id="e5e39-122">Non attendere che la rete venga arrestata.</span><span class="sxs-lookup"><span data-stu-id="e5e39-122">Do not wait for the network for shutdown.</span></span>

    <span data-ttu-id="e5e39-123">Le applicazioni client-server scritte correttamente gestiscono le disconnessioni interrotte normalmente.</span><span class="sxs-lookup"><span data-stu-id="e5e39-123">Properly written client-server applications handle abortive disconnects gracefully.</span></span> <span data-ttu-id="e5e39-124">Non avviare un'operazione potenzialmente lunga, ad esempio la sincronizzazione di file o cartelle con un server, che non può essere interrotta al momento dell'arresto.</span><span class="sxs-lookup"><span data-stu-id="e5e39-124">Do not initiate a potentially lengthy operation, such as synchronizing files or folders with a server, that cannot be interrupted on shutdown.</span></span> <span data-ttu-id="e5e39-125">Le reti non rispondono in modo coerente, quindi anche le piccole operazioni possono rivelarsi molto tempo.</span><span class="sxs-lookup"><span data-stu-id="e5e39-125">Networks are not consistently responsive, so even small operations could prove time consuming.</span></span> <span data-ttu-id="e5e39-126">Fornire un feedback positivo per gli utenti, incluse le indicazioni sullo stato di avanzamento e i tempi di completamento stimati.</span><span class="sxs-lookup"><span data-stu-id="e5e39-126">Provide positive feedback for users, including indications of progress and estimated completion times.</span></span>

-   <span data-ttu-id="e5e39-127">Assicurarsi di disporre di un'interfaccia utente reattiva.</span><span class="sxs-lookup"><span data-stu-id="e5e39-127">Ensure a responsive user interface.</span></span>

    <span data-ttu-id="e5e39-128">La velocità di risposta dell'applicazione consente di eliminare chiamate al supporto tecnico non necessarie.</span><span class="sxs-lookup"><span data-stu-id="e5e39-128">Application responsiveness helps eliminate unnecessary helpdesk calls.</span></span> <span data-ttu-id="e5e39-129">Una guida efficace per la risposta interattiva è 500 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="e5e39-129">A good guideline for interactive response is 500 milliseconds.</span></span> <span data-ttu-id="e5e39-130">Gli utenti percepiscono pause più lunghe di 500 millisecondi come un ritardo nelle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="e5e39-130">Users perceive pauses longer than 500 milliseconds as a lag in performance.</span></span> <span data-ttu-id="e5e39-131">Le applicazioni devono essere sufficientemente reattive per fornire all'utente l'attendibilità dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e5e39-131">Applications should be responsive enough to provide the user with confidence about the application.</span></span>

-   <span data-ttu-id="e5e39-132">Esaminare gli errori di rete.</span><span class="sxs-lookup"><span data-stu-id="e5e39-132">Scrutinize network errors.</span></span>

    <span data-ttu-id="e5e39-133">Non tutti gli errori di rete sono di importanza critica.</span><span class="sxs-lookup"><span data-stu-id="e5e39-133">Not all network errors are critical.</span></span> <span data-ttu-id="e5e39-134">Ad esempio, un'applicazione che ha ricevuto o inviato tutti i relativi dati può probabilmente ignorare gli errori quando si chiude la connessione.</span><span class="sxs-lookup"><span data-stu-id="e5e39-134">For example, an application that has received or posted all of its data can likely ignore errors when closing the connection.</span></span> <span data-ttu-id="e5e39-135">Non presupporre che la rete o l'utente sia disponibile; è possibile gestire gli errori senza l'intervento dell'utente o ignorarli se gli errori sono non critici.</span><span class="sxs-lookup"><span data-stu-id="e5e39-135">Do not assume the network or the user is available; either handle errors without user intervention, or ignore them if errors are noncritical.</span></span>

-   <span data-ttu-id="e5e39-136">Un'applicazione deve definire il proprio timeout ragionevole.</span><span class="sxs-lookup"><span data-stu-id="e5e39-136">An application should define its own reasonable time outs.</span></span>

    <span data-ttu-id="e5e39-137">Una richiesta Windows Sockets Connect (), ad esempio, può bloccarsi in alcune condizioni per un tempo di 21 secondi.</span><span class="sxs-lookup"><span data-stu-id="e5e39-137">For example, a Windows Sockets connect() request may block under some conditions for as much as 21 seconds.</span></span> <span data-ttu-id="e5e39-138">È possibile che le applicazioni debbano introdurre i propri timeout nel modo appropriato per gli utenti.</span><span class="sxs-lookup"><span data-stu-id="e5e39-138">Applications may need to introduce their own time outs as appropriate for their users.</span></span>

-   <span data-ttu-id="e5e39-139">Ridurre al minimo il sovraccarico del protocollo.</span><span class="sxs-lookup"><span data-stu-id="e5e39-139">Minimize protocol overhead.</span></span>

    <span data-ttu-id="e5e39-140">La conservazione della larghezza di banda della rete riguarda parzialmente la riduzione del sovraccarico del protocollo sostenuto dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e5e39-140">Conserving network bandwidth is partially about minimizing the protocol overhead incurred by your application.</span></span> <span data-ttu-id="e5e39-141">Si tratta anche di eliminare il traffico di rete superfluo.</span><span class="sxs-lookup"><span data-stu-id="e5e39-141">It is also about eliminating unnecessary network traffic.</span></span> <span data-ttu-id="e5e39-142">Per il trasferimento dei dati dell'applicazione è possibile usare protocolli con sovraccarico di intestazione inferiore.</span><span class="sxs-lookup"><span data-stu-id="e5e39-142">Protocols with a lower header overhead can be used to transfer application data.</span></span> <span data-ttu-id="e5e39-143">Ad esempio, quando si inviano quantità minori di dati non critici o ripetibili, utilizzare UDP anziché TCP per ridurre l'overhead associato alla creazione e manutenzione della connessione.</span><span class="sxs-lookup"><span data-stu-id="e5e39-143">For example, when sending smaller amounts of noncritical or repeatable data, use UDP as opposed to TCP to reduce the overhead associated with connection establishment and maintenance.</span></span> <span data-ttu-id="e5e39-144">Se gli stessi dati devono essere inviati a più destinatari, prendere in considerazione il multicast.</span><span class="sxs-lookup"><span data-stu-id="e5e39-144">If the same data must be sent to multiple recipients, consider multicast.</span></span> <span data-ttu-id="e5e39-145">Tenere presente che le applicazioni UDP non sono controllate dal flusso. Se si supera la larghezza di banda disponibile, è possibile che si verifichi un errore irreversibile della rete.</span><span class="sxs-lookup"><span data-stu-id="e5e39-145">Be aware that UDP applications are not flow-controlled—pushing beyond the available bandwidth can cause catastrophic network failure.</span></span> <span data-ttu-id="e5e39-146">L'utilità netstat può essere usata con le opzioni **-e** e **-s** per visualizzare le statistiche per diversi protocolli.</span><span class="sxs-lookup"><span data-stu-id="e5e39-146">The Netstat utility can be used with its **-e** and **-s** options to display statistics for various protocols.</span></span>

-   <span data-ttu-id="e5e39-147">Conservare le risorse di sistema.</span><span class="sxs-lookup"><span data-stu-id="e5e39-147">Conserve system resources.</span></span>

    <span data-ttu-id="e5e39-148">Le risorse di sistema possono essere utilizzate rapidamente se non viene utilizzato il vincolo appropriato.</span><span class="sxs-lookup"><span data-stu-id="e5e39-148">System resources can be consumed quickly if proper restraint is not used.</span></span> <span data-ttu-id="e5e39-149">Ad esempio, le connessioni Sockets e TCP utilizzano risorse.</span><span class="sxs-lookup"><span data-stu-id="e5e39-149">For example, sockets and TCP connections consume resources.</span></span> <span data-ttu-id="e5e39-150">Non usare più connessioni TCP per ogni client, dove ne sarà disponibile uno per lo scopo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e5e39-150">Do not use several TCP connections per client where one will serve the application's purpose.</span></span>

<span data-ttu-id="e5e39-151">Per le applicazioni transazionali, un'esperienza utente ottimale e un basso utilizzo della rete non rappresentano obiettivi in conflitto.</span><span class="sxs-lookup"><span data-stu-id="e5e39-151">For transactional applications, good user experience and low network utilization are not conflicting goals.</span></span> <span data-ttu-id="e5e39-152">La rete è un collo di bottiglia.</span><span class="sxs-lookup"><span data-stu-id="e5e39-152">The network is a bottleneck.</span></span> <span data-ttu-id="e5e39-153">Le applicazioni con utilizzo intensivo di rete dedicano più tempo all'attesa e le applicazioni di rete ben scritte sono progettate per ridurre al minimo il tempo di attesa superfluo, sia per l'interfaccia utente che per trasmissioni di rete.</span><span class="sxs-lookup"><span data-stu-id="e5e39-153">Network-intensive applications spend more time waiting, and well written network applications are designed to minimize unnecessary wait time, both for the user interface and for network transmissions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5e39-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e5e39-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5e39-155">Applicazioni Windows Sockets a prestazioni elevate</span><span class="sxs-lookup"><span data-stu-id="e5e39-155">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="e5e39-156">Dimensioni prestazioni</span><span class="sxs-lookup"><span data-stu-id="e5e39-156">Performance Dimensions</span></span>](performance-dimensions-2.md)
</dt> </dl>

 

 



