---
description: Il servizio componenti in coda COM+ migliora il modello di programmazione COM fornendo un ambiente in cui un componente può essere richiamato in modalità sincrona (in tempo reale) o in modo asincrono (in coda).
ms.assetid: fd455679-b2b3-487f-8494-9ea296ce2c89
title: Architettura dei componenti in coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8a2f6e1012bd3c11a27a44214ee28e84d5bd404
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104551694"
---
# <a name="queued-components-architecture"></a><span data-ttu-id="276c0-103">Architettura dei componenti in coda</span><span class="sxs-lookup"><span data-stu-id="276c0-103">Queued Components Architecture</span></span>

<span data-ttu-id="276c0-104">Il servizio componenti in coda COM+ migliora il modello di programmazione COM fornendo un ambiente in cui un componente può essere richiamato in modalità sincrona (in tempo reale) o in modo asincrono (in coda).</span><span class="sxs-lookup"><span data-stu-id="276c0-104">The COM+ queued components service enhances the COM programming model by providing an environment in which a component can be invoked either synchronously (real-time) or asynchronously (queued).</span></span> <span data-ttu-id="276c0-105">Non è necessario che un componente sia in grado di essere utilizzato in un contesto in tempo reale o in coda.</span><span class="sxs-lookup"><span data-stu-id="276c0-105">A component need not be aware of whether it is employed in a real-time or a queued context.</span></span>

<span data-ttu-id="276c0-106">Le applicazioni di messaggistica sono simili alle transazioni di posta elettronica tra i programmi.</span><span class="sxs-lookup"><span data-stu-id="276c0-106">Messaging applications are like email transactions between programs.</span></span> <span data-ttu-id="276c0-107">Il richiedente invia un messaggio al server. Quando il server riceve il messaggio, il messaggio viene elaborato.</span><span class="sxs-lookup"><span data-stu-id="276c0-107">The requester sends a message to the server; when the server gets to it, the message is processed.</span></span> <span data-ttu-id="276c0-108">Analogamente alla posta elettronica, un sistema di messaggistica deve gestire i dettagli della rete e assicurarsi che il messaggio venga spostato dal client al server.</span><span class="sxs-lookup"><span data-stu-id="276c0-108">Like email, a messaging system must handle the network details and ensure that the message moves from the client to the server.</span></span> <span data-ttu-id="276c0-109">Nel Framework dei componenti in coda, l'accodamento dei messaggi è responsabile di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="276c0-109">In the queued components framework, Message Queuing is responsible for this.</span></span>

<span data-ttu-id="276c0-110">Il servizio componenti in coda COM+ è costituito dalle parti seguenti:</span><span class="sxs-lookup"><span data-stu-id="276c0-110">The COM+ queued components service consists of the following parts:</span></span>

-   <span data-ttu-id="276c0-111">Registratore (per il client o il lato di trasmissione)</span><span class="sxs-lookup"><span data-stu-id="276c0-111">Recorder (for the client or send side)</span></span>
-   <span data-ttu-id="276c0-112">Listener (per il server o il lato ricezione)</span><span class="sxs-lookup"><span data-stu-id="276c0-112">Listener (for the server or receive side)</span></span>
-   <span data-ttu-id="276c0-113">Player (per il server o il lato di ricezione)</span><span class="sxs-lookup"><span data-stu-id="276c0-113">Player (for the server or receive side)</span></span>

![Diagramma che mostra il percorso dal client al server: client, registratore, coda, listener, lettore, server.](images/d732774b-1ca6-45ad-bce0-a95b0bfc3edb.png)

## <a name="the-recorder"></a><span data-ttu-id="276c0-115">Registratore</span><span class="sxs-lookup"><span data-stu-id="276c0-115">The Recorder</span></span>

<span data-ttu-id="276c0-116">In uno scenario tipico di componenti in coda, il client chiama un componente in coda.</span><span class="sxs-lookup"><span data-stu-id="276c0-116">In a typical queued components scenario, the client calls a queued component.</span></span> <span data-ttu-id="276c0-117">La chiamata viene effettuata al registratore dei componenti in coda, che lo inserisce come parte di un messaggio nel server e lo inserisce in una coda.</span><span class="sxs-lookup"><span data-stu-id="276c0-117">The call is made to the queued components recorder, which packages it as part of a message to the server and puts it in a queue.</span></span> <span data-ttu-id="276c0-118">Il registratore esegue il marshalling del contesto di sicurezza del client nel messaggio e registra tutte le chiamate al metodo del client.</span><span class="sxs-lookup"><span data-stu-id="276c0-118">The recorder marshals the client's security context into the message and records all of the client's method calls.</span></span> <span data-ttu-id="276c0-119">Nel ruolo di proxy per il componente server, il registratore seleziona le interfacce dalle interfacce di accodamento nel catalogo COM+.</span><span class="sxs-lookup"><span data-stu-id="276c0-119">In its role as proxy for the server component, the recorder selects interfaces from the queuable interfaces in the COM+ catalog.</span></span>

<span data-ttu-id="276c0-120">Una rappresentazione della registrazione viene inviata a Accodamento messaggi come messaggio da inviare a un server.</span><span class="sxs-lookup"><span data-stu-id="276c0-120">A representation of the recording is sent to Message Queuing as a message to be sent to a server.</span></span> <span data-ttu-id="276c0-121">Quando il componente in coda presenta l'impostazione dell'attributo Transaction richiesta o supportata, Accodamento messaggi accetta il recapito del messaggio solo se il commit della transazione sul lato client e la coda di Accodamento messaggi sono transazionali, ovvero l'impostazione predefinita normalmente stabilita.</span><span class="sxs-lookup"><span data-stu-id="276c0-121">When the queued component has the transaction attribute setting of Required or Supported, Message Queuing accepts delivery of the message only if the client-side transaction commits and the Message Queuing queue is transactional, which is the default normally established.</span></span> <span data-ttu-id="276c0-122">Quando l'impostazione dell'attributo Transaction è richiesta New, Accodamento messaggi può accettare il messaggio anche se la transazione sul lato client viene interrotta.</span><span class="sxs-lookup"><span data-stu-id="276c0-122">When the transaction attribute setting is Requires New, Message Queuing can accept the message even if the client-side transaction aborts.</span></span> <span data-ttu-id="276c0-123">Per ulteriori informazioni sulle transazioni, vedere [Accodamento messaggi transazionale](transactional-message-queuing.md).</span><span class="sxs-lookup"><span data-stu-id="276c0-123">For more information on transactions, see [Transactional Message Queuing](transactional-message-queuing.md).</span></span>

## <a name="the-listener"></a><span data-ttu-id="276c0-124">Il listener</span><span class="sxs-lookup"><span data-stu-id="276c0-124">The Listener</span></span>

<span data-ttu-id="276c0-125">Il listener dei componenti in coda recupera il messaggio dalla coda e lo passa al lettore dei componenti in coda.</span><span class="sxs-lookup"><span data-stu-id="276c0-125">The queued components listener retrieves the message from the queue and passes it to the queued components player.</span></span>

## <a name="the-player"></a><span data-ttu-id="276c0-126">Il lettore</span><span class="sxs-lookup"><span data-stu-id="276c0-126">The Player</span></span>

<span data-ttu-id="276c0-127">Il giocatore esegue l'unmarshalling del contesto di sicurezza del client sul lato server e quindi richiama il componente server e effettua le stesse chiamate al metodo.</span><span class="sxs-lookup"><span data-stu-id="276c0-127">The player unmarshals the client's security context at the server side and then invokes the server component and makes the same method calls.</span></span> <span data-ttu-id="276c0-128">Le chiamate al metodo non vengono riprodotte dal lettore finché il componente client non viene completato e la transazione che ha registrato il metodo chiama commit.</span><span class="sxs-lookup"><span data-stu-id="276c0-128">The method calls are not played back by the player until the client component completes and the transaction that recorded the method calls commits.</span></span>

## <a name="the-message-mover"></a><span data-ttu-id="276c0-129">Mover del messaggio</span><span class="sxs-lookup"><span data-stu-id="276c0-129">The Message Mover</span></span>

<span data-ttu-id="276c0-130">Il motore messaggi in coda è un'utilità che sposta tutti i messaggi di Accodamento messaggi non riusciti da una coda a un'altra, in modo che possano essere ripetuti.</span><span class="sxs-lookup"><span data-stu-id="276c0-130">The queued components message mover is a utility that moves all failed Message Queuing messages from one queue to another so that they can be retried.</span></span> <span data-ttu-id="276c0-131">L'utilità del Mover del messaggio è un oggetto di automazione che può essere richiamato con un VBScript. Per ulteriori informazioni, vedere [gestione degli errori](handling-errors-in-queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="276c0-131">The message mover utility is an Automation object that can be invoked with a VBScript; for more information, see [Handling Errors](handling-errors-in-queued-components.md).</span></span>

 

 



