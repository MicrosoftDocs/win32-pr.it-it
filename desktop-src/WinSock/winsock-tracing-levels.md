---
description: 'Altre informazioni su: livelli di traccia Winsock'
ms.assetid: a92bc4d2-257a-478a-b10d-4fada4323c9b
title: Livelli di traccia Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b225558015fb823cd02028a1ae1433d3d0549896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315753"
---
# <a name="winsock-tracing-levels"></a><span data-ttu-id="13c8c-103">Livelli di traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="13c8c-103">Winsock Tracing Levels</span></span>

## <a name="levels-of-winsock-tracing"></a><span data-ttu-id="13c8c-104">Livelli di traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="13c8c-104">Levels of Winsock Tracing</span></span>

<span data-ttu-id="13c8c-105">Nella traccia Winsock sono possibili due livelli di registrazione:</span><span class="sxs-lookup"><span data-stu-id="13c8c-105">There are two levels of logging possible in Winsock tracing:</span></span>

-   <span data-ttu-id="13c8c-106">Informazioni</span><span class="sxs-lookup"><span data-stu-id="13c8c-106">Information</span></span>
-   <span data-ttu-id="13c8c-107">Dettagliato</span><span class="sxs-lookup"><span data-stu-id="13c8c-107">Verbose</span></span>

<span data-ttu-id="13c8c-108">Il livello informazioni analizza il socket creare e chiudere gli eventi, nonché gli eventuali errori che si verificano nel socket.</span><span class="sxs-lookup"><span data-stu-id="13c8c-108">The information level traces socket create and close events, as well as any errors that occur on the socket.</span></span>

<span data-ttu-id="13c8c-109">Il livello dettagliato include gli eventi a livello di informazioni e aggiunge ulteriori tracce per gli eventi di trasmissione e ricezione.</span><span class="sxs-lookup"><span data-stu-id="13c8c-109">The verbose level includes the information level events, and adds additional tracing for send and receive events.</span></span> <span data-ttu-id="13c8c-110">La registrazione dettagliata verrebbe utilizzata per rilevare i problemi di danneggiamento del buffer e le applicazioni scritte in modo non corretto.</span><span class="sxs-lookup"><span data-stu-id="13c8c-110">The verbose logging would be used to catch buffer corruption issues as well as poorly written applications.</span></span>

<span data-ttu-id="13c8c-111">Con la traccia eventi di rete Winsock è possibile utilizzare il livello di informazioni o dettagliato.</span><span class="sxs-lookup"><span data-stu-id="13c8c-111">Either the information or verbose level can be used with the Winsock Network Event tracing.</span></span> <span data-ttu-id="13c8c-112">La traccia delle modifiche del catalogo Winsock supporta solo il livello di informazioni.</span><span class="sxs-lookup"><span data-stu-id="13c8c-112">The Winsock Catalog Change tracing supports only information level.</span></span>

## <a name="information-event-tracing"></a><span data-ttu-id="13c8c-113">Traccia eventi informativi</span><span class="sxs-lookup"><span data-stu-id="13c8c-113">Information Event Tracing</span></span>

<span data-ttu-id="13c8c-114">Nell'elenco seguente vengono illustrate le operazioni di socket di eventi di rete Winsock tracciate a livello di informazioni:</span><span class="sxs-lookup"><span data-stu-id="13c8c-114">The following list details those Winsock network event socket operations that are traced at the information level:</span></span>

-   <span data-ttu-id="13c8c-115">Creazione socket</span><span class="sxs-lookup"><span data-stu-id="13c8c-115">Socket creation</span></span>

    <span data-ttu-id="13c8c-116">Un evento viene registrato nella creazione del socket che può essere usato per tracciare la durata di un socket.</span><span class="sxs-lookup"><span data-stu-id="13c8c-116">An event is logged on socket creation which can be used to trace the lifetime of a socket.</span></span> <span data-ttu-id="13c8c-117">Questi eventi includono anche socket creati accettando connessioni su un socket di ascolto.</span><span class="sxs-lookup"><span data-stu-id="13c8c-117">These events also includes sockets created by accepting connections on a listening socket.</span></span>

-   <span data-ttu-id="13c8c-118">Associazione</span><span class="sxs-lookup"><span data-stu-id="13c8c-118">Bind</span></span>

    <span data-ttu-id="13c8c-119">L'indirizzo IP locale viene registrato per consentire la correlazione tra le informazioni di traccia di Winsock e le chiamate al socket di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="13c8c-119">The local IP address is logged to help correlate the Winsock tracing information to an application's socket calls.</span></span>

-   <span data-ttu-id="13c8c-120">Connessione</span><span class="sxs-lookup"><span data-stu-id="13c8c-120">Connect</span></span>

    <span data-ttu-id="13c8c-121">L'indirizzo IP remoto del socket connesso viene registrato per consentire la correlazione delle informazioni di traccia di Winsock alle chiamate socket di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="13c8c-121">The remote IP address of the connected socket is logged to help correlate the Winsock tracing information to an application's socket calls.</span></span>

-   <span data-ttu-id="13c8c-122">Interruzioni e annullamenti avviati da Winsock</span><span class="sxs-lookup"><span data-stu-id="13c8c-122">Winsock-initiated aborts and cancels</span></span>

    <span data-ttu-id="13c8c-123">Quando Winsock interrompe attivamente o Annulla una richiesta, l'evento viene registrato.</span><span class="sxs-lookup"><span data-stu-id="13c8c-123">Anytime Winsock actively aborts or cancels a request, the event is logged.</span></span>

-   <span data-ttu-id="13c8c-124">Reimpostazioni avviate dal trasporto</span><span class="sxs-lookup"><span data-stu-id="13c8c-124">Transport initiated resets</span></span>

    <span data-ttu-id="13c8c-125">Ogni volta che il trasporto sottostante indica che la connessione è stata reimpostata, l'evento viene registrato.</span><span class="sxs-lookup"><span data-stu-id="13c8c-125">Anytime the underlying transport indicates a connection has been reset, the event is logged.</span></span>

-   <span data-ttu-id="13c8c-126">Inviare e ricevere errori</span><span class="sxs-lookup"><span data-stu-id="13c8c-126">Send and receive errors</span></span>

    <span data-ttu-id="13c8c-127">Ogni volta che una chiamata di trasmissione o ricezione al trasporto sottostante ha esito negativo, viene registrato l'evento.</span><span class="sxs-lookup"><span data-stu-id="13c8c-127">Whenever a send or receive call to the underlying transport fails, the event is logged.</span></span>

-   <span data-ttu-id="13c8c-128">Disconnetti e Chiudi socket</span><span class="sxs-lookup"><span data-stu-id="13c8c-128">Socket disconnect and close</span></span>

    <span data-ttu-id="13c8c-129">Un evento viene registrato quando un handle di socket viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="13c8c-129">An event is logged when a socket handle is closed.</span></span>

## <a name="verbose-event-tracing"></a><span data-ttu-id="13c8c-130">Traccia eventi dettagliati</span><span class="sxs-lookup"><span data-stu-id="13c8c-130">Verbose Event Tracing</span></span>

<span data-ttu-id="13c8c-131">Tutti gli eventi informativi vengono tracciati a livello dettagliato.</span><span class="sxs-lookup"><span data-stu-id="13c8c-131">All of the information events are traced at the verbose level.</span></span> <span data-ttu-id="13c8c-132">Nell'elenco seguente vengono illustrate le operazioni aggiuntive del socket di eventi di rete Winsock tracciate a livello dettagliato:</span><span class="sxs-lookup"><span data-stu-id="13c8c-132">The following list details those additional Winsock network event socket operations that are traced at the verbose level:</span></span>

-   <span data-ttu-id="13c8c-133">Buffer di invio e ricezione</span><span class="sxs-lookup"><span data-stu-id="13c8c-133">Send and receive buffers</span></span>

    <span data-ttu-id="13c8c-134">Gli eventi vengono registrati negli indirizzi del buffer utente e le lunghezze quando le chiamate di invio e ricezione vengono inviate a Winsock, oltre al completamento di queste chiamate.</span><span class="sxs-lookup"><span data-stu-id="13c8c-134">Events are logged of user buffer addresses and lengths when send and receive calls are posted to Winsock, as well as upon completion of these calls.</span></span> <span data-ttu-id="13c8c-135">Questa operazione è utile per la diagnosi dei problemi di riutilizzo del buffer, nonché per l'utilizzo inefficiente dei buffer.</span><span class="sxs-lookup"><span data-stu-id="13c8c-135">This is useful for diagnosing buffer re-use issues as well as inefficient use of buffers.</span></span>

-   <span data-ttu-id="13c8c-136">Opzioni socket</span><span class="sxs-lookup"><span data-stu-id="13c8c-136">Socket options</span></span>

    <span data-ttu-id="13c8c-137">Un evento viene registrato quando un'applicazione modifica determinati valori di opzioni del socket.</span><span class="sxs-lookup"><span data-stu-id="13c8c-137">An event is logged when an application changes certain socket option values.</span></span> <span data-ttu-id="13c8c-138">Alcune delle opzioni registrate includono \_ sndbuf, pertanto \_ RCVBUF, SIO Abilita l' \_ \_ \_ Accodamento circolare e FIONBIO.</span><span class="sxs-lookup"><span data-stu-id="13c8c-138">Some of the options logged include SO\_SNDBUF, SO\_RCVBUF, SIO\_ENABLE\_CIRCULAR\_QUEUEING, and FIONBIO.</span></span>

-   <span data-ttu-id="13c8c-139">WSAPoll e Select</span><span class="sxs-lookup"><span data-stu-id="13c8c-139">WSAPoll and select</span></span>

    <span data-ttu-id="13c8c-140">Un evento viene registrato nell'utilizzo di un'applicazione di [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) e nelle chiamate [**SELECT**](/windows/desktop/api/Winsock2/nf-winsock2-select) che possono essere usate per individuare i colli di bottiglia delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="13c8c-140">An event is logged of an application's usage of [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) and [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) calls which can be used to find performance bottlenecks.</span></span>

-   <span data-ttu-id="13c8c-141">Interruzioni e annullamenti avviati da Winsock</span><span class="sxs-lookup"><span data-stu-id="13c8c-141">Winsock-initiated aborts and cancels</span></span>

    <span data-ttu-id="13c8c-142">Quando Winsock interrompe attivamente o Annulla una richiesta, l'evento viene registrato.</span><span class="sxs-lookup"><span data-stu-id="13c8c-142">Anytime Winsock actively aborts or cancels a request, the event is logged.</span></span>

-   <span data-ttu-id="13c8c-143">Maschera eventi</span><span class="sxs-lookup"><span data-stu-id="13c8c-143">Event mask</span></span>

    <span data-ttu-id="13c8c-144">Viene registrato un evento della maschera di eventi registrata da un'applicazione per l'utilizzo della funzione [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) .</span><span class="sxs-lookup"><span data-stu-id="13c8c-144">An event is logged of the event mask an application registers for using the [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function.</span></span>

-   <span data-ttu-id="13c8c-145">Datagram</span><span class="sxs-lookup"><span data-stu-id="13c8c-145">Datagram</span></span>

    <span data-ttu-id="13c8c-146">Un evento viene registrato ogni volta che viene ricevuto un datagramma e non è disponibile spazio nel buffer in cui copiarlo.</span><span class="sxs-lookup"><span data-stu-id="13c8c-146">An event is logged whenever a datagram arrives and there is no buffer space in which to copy it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13c8c-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="13c8c-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13c8c-148">Controllo della traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="13c8c-148">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="13c8c-149">Traccia Winsock</span><span class="sxs-lookup"><span data-stu-id="13c8c-149">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="13c8c-150">Dettagli della traccia delle modifiche del catalogo Winsock</span><span class="sxs-lookup"><span data-stu-id="13c8c-150">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="13c8c-151">Dettagli traccia eventi di rete Winsock</span><span class="sxs-lookup"><span data-stu-id="13c8c-151">Winsock Network Event Tracing Details</span></span>](winsock-tracing-event-details.md)
</dt> </dl>

 

 
