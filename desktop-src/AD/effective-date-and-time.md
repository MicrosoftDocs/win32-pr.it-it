---
title: Data e ora valide
description: La data e l'ora effettive sono una strategia di prevenzione che impedisce la distorsione della versione e gli aggiornamenti parziali rinviando i dati effettivi di informazioni a un certo punto in futuro quando la modifica ha una probabilità elevata di essere replicata completamente.
ms.assetid: 5e24f90a-dd53-4720-815e-9a1db51847a3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448941b7ab0d85d50123985a120beb04f256d877
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044130"
---
# <a name="effective-date-and-time"></a><span data-ttu-id="46ec3-103">Data e ora valide</span><span class="sxs-lookup"><span data-stu-id="46ec3-103">Effective Date and Time</span></span>

<span data-ttu-id="46ec3-104">La *data e l'ora effettive* sono una strategia di prevenzione che impedisce la distorsione della versione e gli aggiornamenti parziali rinviando i dati effettivi di informazioni a un certo punto in futuro quando la modifica ha una probabilità elevata di essere replicata completamente.</span><span class="sxs-lookup"><span data-stu-id="46ec3-104">*Effective date and time* is an avoidance strategy that prevents version skew and partial updates by deferring the effective data of information to some point in the future when the change has a high probability of being fully replicated.</span></span> <span data-ttu-id="46ec3-105">Per implementare le date effettive, gli oggetti applicazione devono includere un timestamp di data effettivo, che viene compilato quando l'oggetto viene creato o modificato.</span><span class="sxs-lookup"><span data-stu-id="46ec3-105">To implement effective dates, the application objects must include an effective date timestamp, which is filled in when the object is created or changed.</span></span> <span data-ttu-id="46ec3-106">I consumer degli oggetti verificano il timestamp e rinviano l'utilizzo degli oggetti fino a quando non viene raggiunta la data e l'ora.</span><span class="sxs-lookup"><span data-stu-id="46ec3-106">Consumers of the objects verify the timestamp and defer use of the objects until that date and time are reached.</span></span>

<span data-ttu-id="46ec3-107">Alcune considerazioni importanti:</span><span class="sxs-lookup"><span data-stu-id="46ec3-107">Some important considerations:</span></span>

-   <span data-ttu-id="46ec3-108">Le applicazioni che scelgono questo approccio devono assicurarsi che esista un set di dati applicabili da usare finché gli oggetti aggiornati non diventano effettivi.</span><span class="sxs-lookup"><span data-stu-id="46ec3-108">Applications that choose this approach must ensure that there is a set of applicable data to use until the updated objects become effective.</span></span>
-   <span data-ttu-id="46ec3-109">Il servizio tempo distribuito in Windows NT 4,0 mantiene sincronizzati gli orologi di Windows 2000 connessi.</span><span class="sxs-lookup"><span data-stu-id="46ec3-109">Distributed time service in Windows NT 4.0 keeps the clocks of the connected Windows 2000 synchronized.</span></span> <span data-ttu-id="46ec3-110">Tuttavia, il servizio ora non è perfetto, quindi è presente una piccola finestra per la distorsione della versione.</span><span class="sxs-lookup"><span data-stu-id="46ec3-110">No time service is perfect, however, so there is a small window for version skew.</span></span>
-   <span data-ttu-id="46ec3-111">L'impostazione di una data di validità valida presuppone la conoscenza della latenza di replica complessiva per il sistema distribuito in questione.</span><span class="sxs-lookup"><span data-stu-id="46ec3-111">Setting a good effective date presumes knowledge of the overall replication latency for the distributed system in question.</span></span> <span data-ttu-id="46ec3-112">In una rete stabile una regola empirica valida per le date effettive è (tempo dell'aggiornamento) + (2 \* (latenza complessiva media).</span><span class="sxs-lookup"><span data-stu-id="46ec3-112">In a stable network a good rule of thumb for effective dates is the (time of the update) + (2\*(average overall latency)).</span></span> <span data-ttu-id="46ec3-113">Quindi, per un sistema la cui media di latenza complessiva è di 4 ore, un ritardo di 8 ore è ragionevole.</span><span class="sxs-lookup"><span data-stu-id="46ec3-113">So, for a system whose overall latency averages 4 hours, a delay of 8 hours is reasonable.</span></span>
-   <span data-ttu-id="46ec3-114">In una rete instabile, determinare un valore "positivo" per le date effettive è molto più difficile, poiché la latenza può essere estremamente variabile.</span><span class="sxs-lookup"><span data-stu-id="46ec3-114">In an unstable network, determining a "good" value for effective dates is much more difficult, since the latency may be highly variable.</span></span> <span data-ttu-id="46ec3-115">La data effettiva è la più "efficace" in una rete instabile se combinata con altre strategie di prevenzione o rilevamento, ad esempio checksum o GUID di coerenza.</span><span class="sxs-lookup"><span data-stu-id="46ec3-115">Effective date is most "effective" in an unstable network when combined with other avoidance or detection strategies such as checksums or consistency GUIDs.</span></span> <span data-ttu-id="46ec3-116">Per ulteriori informazioni, vedere [checksum e conteggi degli oggetti](checksums-and-object-counts.md).</span><span class="sxs-lookup"><span data-stu-id="46ec3-116">For more information, see [Checksums and Object Counts](checksums-and-object-counts.md).</span></span>

 

 




