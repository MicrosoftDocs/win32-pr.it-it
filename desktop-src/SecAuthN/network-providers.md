---
description: Un provider di rete è una DLL che supporta un protocollo di rete specifico.
ms.assetid: ebd47c1b-f427-4fa1-a2ec-1e73be297bef
title: Provider di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30e3cc231f461d48e7ce71d908cb92f6cd06eabd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232822"
---
# <a name="network-providers"></a><span data-ttu-id="cb115-103">Provider di rete</span><span class="sxs-lookup"><span data-stu-id="cb115-103">Network Providers</span></span>

<span data-ttu-id="cb115-104">Un provider di rete è una DLL che supporta un protocollo di rete specifico.</span><span class="sxs-lookup"><span data-stu-id="cb115-104">A network provider is a DLL that supports a specific network protocol.</span></span> <span data-ttu-id="cb115-105">Implementa inoltre l' [API del provider di rete](network-provider-api.md).</span><span class="sxs-lookup"><span data-stu-id="cb115-105">It also implements the [Network Provider API](network-provider-api.md).</span></span> <span data-ttu-id="cb115-106">In questo modo è possibile interagire con il sistema operativo Windows per ricevere richieste di rete standard, ad esempio richieste di connessione o disconnessione.</span><span class="sxs-lookup"><span data-stu-id="cb115-106">This enables it to interact with the Windows operating system to receive standard network requests, such as connection or disconnection requests.</span></span> <span data-ttu-id="cb115-107">Per gestire queste richieste, il provider di rete chiama quindi l'API specifica della rete che è appropriata per il protocollo di rete supportato dal provider di rete.</span><span class="sxs-lookup"><span data-stu-id="cb115-107">To handle these requests, the network provider then calls the network-specific API that is appropriate to the network protocol the network provider supports.</span></span> <span data-ttu-id="cb115-108">In altre parole, il provider di rete esegue il wrapping della funzionalità specifica della rete in una DLL, che espone un'interfaccia standard a Windows.</span><span class="sxs-lookup"><span data-stu-id="cb115-108">In other words, the network provider wraps the network-specific functionality in a DLL, which exposes a standard interface to Windows.</span></span>

<span data-ttu-id="cb115-109">Utilizzando i provider di rete, Windows può supportare molti tipi diversi di protocolli di rete senza dover individuare i dettagli specifici della rete di ogni rete.</span><span class="sxs-lookup"><span data-stu-id="cb115-109">Using network providers, Windows can support many different types of network protocols without having to know the network-specific details of each network.</span></span> <span data-ttu-id="cb115-110">Questa operazione è essenziale perché i nuovi protocolli di rete sono in fase di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="cb115-110">This is essential because new network protocols are being developed all the time.</span></span> <span data-ttu-id="cb115-111">Con i provider di rete, il supporto di un nuovo protocollo richiede semplicemente la creazione e l'installazione di un nuovo provider di rete.</span><span class="sxs-lookup"><span data-stu-id="cb115-111">With network providers, supporting a new protocol simply requires creating and installing a new network provider.</span></span>

<span data-ttu-id="cb115-112">Per informazioni sulle funzioni e sulle strutture del provider di rete, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb115-112">For information about network provider functions and structures, see the following topics:</span></span>

-   [<span data-ttu-id="cb115-113">Funzioni del provider di rete</span><span class="sxs-lookup"><span data-stu-id="cb115-113">Network Provider Functions</span></span>](authentication-functions.md)
-   [<span data-ttu-id="cb115-114">Strutture del provider di rete</span><span class="sxs-lookup"><span data-stu-id="cb115-114">Network Provider Structures</span></span>](authentication-structures.md)

 

 



