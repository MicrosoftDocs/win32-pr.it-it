---
title: Utilizzo di thread
description: È consigliabile ottimizzare e bilanciare l'utilizzo dei thread dell'applicazione per un ambiente multiutente Servizi Desktop remoto multiprocessore.
ms.assetid: 88f4e61f-4a59-4a84-8dca-fdb661835b51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a3b432cf4960c6ec7a8e51b458b9f574663ffe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297881"
---
# <a name="thread-usage"></a><span data-ttu-id="e1927-103">Utilizzo di thread</span><span class="sxs-lookup"><span data-stu-id="e1927-103">Thread usage</span></span>

<span data-ttu-id="e1927-104">I thread rappresentano un modo pratico per consentire a un'applicazione di massimizzare l'utilizzo delle risorse della CPU in un sistema, soprattutto in una configurazione a più processori.</span><span class="sxs-lookup"><span data-stu-id="e1927-104">Threads provide a convenient way of allowing an application to maximize its usage of CPU resources in a system, especially in a multiple processor configuration.</span></span> <span data-ttu-id="e1927-105">In un ambiente di Servizi Desktop remoto, tuttavia, più utenti possono eseguire applicazioni multithread e tutti i thread per tutti gli utenti competono per le risorse della CPU centrale del sistema.</span><span class="sxs-lookup"><span data-stu-id="e1927-105">In a Remote Desktop Services environment, however, multiple users can be running multithreaded applications, and all of the threads for all of the users compete for the central CPU resources of that system.</span></span> <span data-ttu-id="e1927-106">Tenendo presente questo aspetto, è consigliabile ottimizzare e bilanciare l'utilizzo del thread dell'applicazione per un ambiente multiutente Servizi Desktop remoto multiprocessore.</span><span class="sxs-lookup"><span data-stu-id="e1927-106">With this in mind, you should tune and balance application thread usage for a multiuser, multiprocessor Remote Desktop Services environment.</span></span> <span data-ttu-id="e1927-107">Anche se un'applicazione multithreading progettata in modo non corretto con thread inattivi o sprecati potrebbe funzionare adeguatamente in un computer client, è possibile che la stessa applicazione non venga eseguita correttamente in un server Servizi Desktop remoto multiutente.</span><span class="sxs-lookup"><span data-stu-id="e1927-107">While a poorly designed multithreaded application with idle or wasted threads might perform adequately on a client computer, the same application might not perform well on a multiuser Remote Desktop Services server.</span></span>

 

 




