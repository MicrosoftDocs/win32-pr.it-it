---
description: Differenze tra l'i/o locale e l'I/O di rete in Windows.
ms.assetid: 8a8f20bd-fa41-4f1a-b9bf-5f09683cd46c
title: Differenze nell'I/O locale e di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30c4faf6b7358a1c7c134dccdeb12298309c654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313892"
---
# <a name="differences-in-local-and-network-io"></a><span data-ttu-id="d8d4a-103">Differenze nell'I/O locale e di rete</span><span class="sxs-lookup"><span data-stu-id="d8d4a-103">Differences in Local and Network I/O</span></span>

<span data-ttu-id="d8d4a-104">Esistono alcune differenze rilevanti tra I/o locale e I/O di rete in Windows:</span><span class="sxs-lookup"><span data-stu-id="d8d4a-104">There are some notable differences between local I/O and network I/O on Windows:</span></span>

-   <span data-ttu-id="d8d4a-105">Il supporto di I/O di rete dipende dal redirector e dal protocollo di rete.</span><span class="sxs-lookup"><span data-stu-id="d8d4a-105">Network I/O support depends on the redirector and the network protocol.</span></span>
-   <span data-ttu-id="d8d4a-106">Le prestazioni di I/O di rete variano a seconda del numero di operazioni di I/O di rete eseguite e della velocità della connessione di rete.</span><span class="sxs-lookup"><span data-stu-id="d8d4a-106">Network I/O performance depends on how many network I/O operations are taking place and the speed of the network connection.</span></span> <span data-ttu-id="d8d4a-107">L'applicazione deve essere in grado di gestire le operazioni di I/O di rete con i server che potrebbero essere molto più veloci o più lenti del computer locale, oltre a modifiche temporanee nella capacità di rete.</span><span class="sxs-lookup"><span data-stu-id="d8d4a-107">Your application must be able to handle network I/O operations with servers that may be much faster or slower than your local machine, as well as transient changes in network capacity.</span></span> <span data-ttu-id="d8d4a-108">In questi casi, l'applicazione potrebbe dover attendere più tempo per il completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d8d4a-108">In these cases, your application may need to allow more time for the operation to complete.</span></span>
-   <span data-ttu-id="d8d4a-109">Le funzioni utilizzate per eseguire operazioni di I/O su file locali possono comportarsi in modo diverso in rete.</span><span class="sxs-lookup"><span data-stu-id="d8d4a-109">The functions you use to perform local file I/O may behave differently over the network.</span></span> <span data-ttu-id="d8d4a-110">È ad esempio possibile che si verifichi il timeout di un'operazione di I/O di rete che richiede molto tempo per il completamento. In alcune situazioni, gli handle di file possono essere lasciati aperti a tempo indefinito a causa di questo.</span><span class="sxs-lookup"><span data-stu-id="d8d4a-110">For example, a network I/O operation that takes a long time to complete may time out. In some situations, file handles may be left open indefinitely because of this.</span></span> <span data-ttu-id="d8d4a-111">Un altro esempio è che le funzioni possono restituire codici di errore per l'applicazione per l'elaborazione specifiche per l'I/O di rete.</span><span class="sxs-lookup"><span data-stu-id="d8d4a-111">Another example is that functions may return error codes for your application to process that are specific to network I/O.</span></span>

 

 



