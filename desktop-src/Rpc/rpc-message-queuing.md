---
title: Accodamento messaggi RPC
description: Accodamento messaggi (MSMQ) consente agli utenti di comunicare tra reti e sistemi indipendentemente dallo stato corrente delle applicazioni e dei sistemi che comunicano.
ms.assetid: f1c8665b-3754-4c2e-b3ac-bba1f4b329e1
keywords:
- RPC (Remote Procedure Call), descritto, Accodamento messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b72e9e35ec2aa1cc440c0d0356c681c4fe8548c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045128"
---
# <a name="rpc-message-queuing"></a><span data-ttu-id="bf6d2-104">Accodamento messaggi RPC</span><span class="sxs-lookup"><span data-stu-id="bf6d2-104">RPC Message Queuing</span></span>

<span data-ttu-id="bf6d2-105">Accodamento messaggi (MSMQ) consente agli utenti di comunicare tra reti e sistemi indipendentemente dallo stato corrente delle applicazioni e dei sistemi che comunicano.</span><span class="sxs-lookup"><span data-stu-id="bf6d2-105">Message Queuing (MSMQ) lets users communicate across networks and systems regardless of the current state of the communicating applications and systems.</span></span> <span data-ttu-id="bf6d2-106">Le applicazioni inviano e ricevono messaggi tramite le code di messaggi gestite da MSMQ.</span><span class="sxs-lookup"><span data-stu-id="bf6d2-106">Applications send and receive messages through message queues that MSMQ maintains.</span></span> <span data-ttu-id="bf6d2-107">Le code di messaggi continuano a funzionare anche quando l'applicazione client o server non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="bf6d2-107">The message queues continue to function even when the client or server application is not running.</span></span> <span data-ttu-id="bf6d2-108">Accodamento messaggi fornisce:</span><span class="sxs-lookup"><span data-stu-id="bf6d2-108">Message queuing provides:</span></span>

-   <span data-ttu-id="bf6d2-109">**Messaggistica asincrona.**</span><span class="sxs-lookup"><span data-stu-id="bf6d2-109">**Asynchronous messaging.**</span></span> <span data-ttu-id="bf6d2-110">Con la messaggistica asincrona MSMQ, un'applicazione client può inviare un messaggio a un server e restituire immediatamente un messaggio, anche se il computer di destinazione o il programma server non risponde.</span><span class="sxs-lookup"><span data-stu-id="bf6d2-110">With MSMQ asynchronous messaging, a client application can send a message to a server and return immediately, even if the target computer or server program is not responding.</span></span>
-   <span data-ttu-id="bf6d2-111">**Recapito di messaggi garantito.**</span><span class="sxs-lookup"><span data-stu-id="bf6d2-111">**Guaranteed message delivery.**</span></span> <span data-ttu-id="bf6d2-112">Quando un'applicazione invia un messaggio tramite MSMQ, il messaggio raggiungerà la destinazione anche se l'applicazione di destinazione non è in esecuzione nello stesso momento o se le reti e i sistemi sono offline.</span><span class="sxs-lookup"><span data-stu-id="bf6d2-112">When an application sends a message through MSMQ, the message will reach its destination even if the destination application is not running at the same time or the networks and systems are offline.</span></span>
-   <span data-ttu-id="bf6d2-113">**Routing e configurazione dinamica.**</span><span class="sxs-lookup"><span data-stu-id="bf6d2-113">**Routing and dynamic configuration.**</span></span> <span data-ttu-id="bf6d2-114">MSMQ fornisce un routing flessibile su reti eterogenee.</span><span class="sxs-lookup"><span data-stu-id="bf6d2-114">MSMQ provides flexible routing over heterogeneous networks.</span></span> <span data-ttu-id="bf6d2-115">La configurazione di tali reti può essere modificata dinamicamente senza modifiche sostanziali a sistemi e reti.</span><span class="sxs-lookup"><span data-stu-id="bf6d2-115">The configuration of such networks can be changed dynamically without any major changes to systems and networks themselves.</span></span>
-   <span data-ttu-id="bf6d2-116">**Messaggistica senza connessione.**</span><span class="sxs-lookup"><span data-stu-id="bf6d2-116">**Connectionless messaging.**</span></span> <span data-ttu-id="bf6d2-117">Le applicazioni che usano MSMQ non devono configurare sessioni dirette con le applicazioni di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bf6d2-117">Applications using MSMQ do not need to set up direct sessions with target applications.</span></span>
-   <span data-ttu-id="bf6d2-118">[Sicurezza](security.md).</span><span class="sxs-lookup"><span data-stu-id="bf6d2-118">[Security](security.md).</span></span> <span data-ttu-id="bf6d2-119">MSMQ fornisce comunicazioni sicure basate sulla sicurezza di Windows e sull'API di crittografia (CryptoAPI) per la crittografia e le firme digitali.</span><span class="sxs-lookup"><span data-stu-id="bf6d2-119">MSMQ provides secure communication based on Windows security and the Cryptographic API (CryptoAPI) for encryption and digital signatures.</span></span>
-   <span data-ttu-id="bf6d2-120">**Messaggistica con priorità.**</span><span class="sxs-lookup"><span data-stu-id="bf6d2-120">**Prioritized Messaging.**</span></span> <span data-ttu-id="bf6d2-121">MSMQ trasferisce i messaggi tra le reti in base alla priorità, consentendo una comunicazione più rapida per le applicazioni critiche.</span><span class="sxs-lookup"><span data-stu-id="bf6d2-121">MSMQ transfers messages across networks based on priority, allowing faster communication for critical applications.</span></span>

<span data-ttu-id="bf6d2-122">Microsoft RPC estende il modello Open Software Foundation-Data Communications Equipment (OSF-DCE) per le chiamate di procedura remota consentendo alle applicazioni distribuite di usare MSMQ come trasporto e di controllare molte delle relative funzionalità.</span><span class="sxs-lookup"><span data-stu-id="bf6d2-122">Microsoft RPC extends the Open Software Foundation–Data Communications Equipment (OSF-DCE) model for remote procedure calls by allowing distributed applications to use MSMQ as a transport and to control many of its features.</span></span> <span data-ttu-id="bf6d2-123">Questa funzionalità è disponibile sia per le applicazioni RPC convenzionali sia per le applicazioni COM tramite l'interfaccia **IRPCOptions** .</span><span class="sxs-lookup"><span data-stu-id="bf6d2-123">This functionality is available both to conventional RPC applications and, through the **IRPCOptions** interface, to COM applications.</span></span>

> [!Note]  
> <span data-ttu-id="bf6d2-124">Accodamento messaggi RPC è disponibile solo in Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="bf6d2-124">RPC message queuing is available only on Windows 2000.</span></span> <span data-ttu-id="bf6d2-125">Le versioni successive di Windows non supportano l'accodamento dei messaggi RPC.</span><span class="sxs-lookup"><span data-stu-id="bf6d2-125">Later versions of Windows do not support RPC message queuing.</span></span>

 

<span data-ttu-id="bf6d2-126">Negli argomenti seguenti viene fornita una panoramica di Accodamento messaggi:</span><span class="sxs-lookup"><span data-stu-id="bf6d2-126">The following topics provide an overview of message queuing:</span></span>

-   [<span data-ttu-id="bf6d2-127">Panoramica dell'architettura dei servizi di Accodamento messaggi</span><span class="sxs-lookup"><span data-stu-id="bf6d2-127">Overview of Message Queuing Services Architecture</span></span>](overview-of-message-queuing-services-architecture.md)
-   [<span data-ttu-id="bf6d2-128">Proprietà Message e Message Queue</span><span class="sxs-lookup"><span data-stu-id="bf6d2-128">Message and Message Queue Properties</span></span>](message-and-message-queue-properties.md)
-   [<span data-ttu-id="bf6d2-129">Utilizzo di MSMQ come trasporto RPC</span><span class="sxs-lookup"><span data-stu-id="bf6d2-129">Using MSMQ as an RPC Transport</span></span>](using-msmq-as-an-rpc-transport.md)
-   [<span data-ttu-id="bf6d2-130">Requisiti di sistema per \_ le applicazioni di Accodamento messaggi RPC</span><span class="sxs-lookup"><span data-stu-id="bf6d2-130">System Requirements for RPC-Message\_Queuing Applications</span></span>](system-requirements-for-rpc-message-queuing-applications.md)
-   [<span data-ttu-id="bf6d2-131">Sviluppo di applicazioni di Accodamento RPC-Message</span><span class="sxs-lookup"><span data-stu-id="bf6d2-131">Developing RPC-Message Queuing Applications</span></span>](developing-rpc-message-queuing-applications.md)
-   [<span data-ttu-id="bf6d2-132">Servizi di sicurezza MSMQ</span><span class="sxs-lookup"><span data-stu-id="bf6d2-132">MSMQ Security Services</span></span>](msmq-security-services.md)

 

 




