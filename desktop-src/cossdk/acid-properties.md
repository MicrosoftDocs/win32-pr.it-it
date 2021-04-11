---
description: Coniato dai pionieri dell'elaborazione delle transazioni, l'acronimo ACID si basa su Atomic, coerenti, isolated e Durable.
ms.assetid: 857d145c-710d-4097-8ed6-df11e8d52228
title: Proprietà ACID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2e725cae75b4aa80d25f2959d474e8baa05f70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126600"
---
# <a name="acid-properties"></a><span data-ttu-id="83f04-103">Proprietà ACID</span><span class="sxs-lookup"><span data-stu-id="83f04-103">ACID Properties</span></span>

<span data-ttu-id="83f04-104">Coniato dai pionieri dell'elaborazione delle transazioni, l'acronimo ACID si basa su Atomic, coerenti, isolated e Durable.</span><span class="sxs-lookup"><span data-stu-id="83f04-104">Coined by transaction processing pioneers, the acronym ACID stands for atomic, consistent, isolated, and durable.</span></span> <span data-ttu-id="83f04-105">Per garantire un comportamento prevedibile, tutte le transazioni devono possedere queste proprietà di base, rafforzando il ruolo di transazioni cruciali come proposizioni all-o-None.</span><span class="sxs-lookup"><span data-stu-id="83f04-105">To ensure predictable behavior, all transactions must possess these basic properties, reinforcing the role of mission-critical transactions as all-or-none propositions.</span></span>

<span data-ttu-id="83f04-106">L'elenco seguente contiene una definizione e una descrizione di ogni proprietà ACID:</span><span class="sxs-lookup"><span data-stu-id="83f04-106">The following list contains a definition and a description of each ACID property:</span></span>

<dl> <dt>

<span data-ttu-id="83f04-107"><span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>Atomica</span><span class="sxs-lookup"><span data-stu-id="83f04-107"><span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>Atomic</span></span>
</dt> <dd>

<span data-ttu-id="83f04-108">Una transazione deve essere eseguita una sola volta e deve essere atomica, ovvero tutto il lavoro viene eseguito o nessuno di essi è.</span><span class="sxs-lookup"><span data-stu-id="83f04-108">A transaction must execute exactly once and must be atomic—either all of the work is done or none of it is.</span></span> <span data-ttu-id="83f04-109">Le operazioni all'interno di una transazione condividono in genere una finalità comune e sono interdipendenti.</span><span class="sxs-lookup"><span data-stu-id="83f04-109">Operations within a transaction usually share a common intent and are interdependent.</span></span> <span data-ttu-id="83f04-110">Eseguendo solo un subset di queste operazioni, il sistema potrebbe compromettere la finalità complessiva della transazione.</span><span class="sxs-lookup"><span data-stu-id="83f04-110">By performing only a subset of these operations, the system could compromise the overall intent of the transaction.</span></span> <span data-ttu-id="83f04-111">L'atomicità Elimina la possibilità di elaborare solo un subset di operazioni.</span><span class="sxs-lookup"><span data-stu-id="83f04-111">Atomicity eliminates the chance of processing only a subset of operations.</span></span>

</dd> <dt>

<span data-ttu-id="83f04-112"><span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Coerente</span><span class="sxs-lookup"><span data-stu-id="83f04-112"><span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Consistent</span></span>
</dt> <dd>

<span data-ttu-id="83f04-113">Una transazione deve mantenere la coerenza dei dati, trasformando uno stato coerente dei dati in un altro stato coerente di dati.</span><span class="sxs-lookup"><span data-stu-id="83f04-113">A transaction must preserve the consistency of data, transforming one consistent state of data into another consistent state of data.</span></span> <span data-ttu-id="83f04-114">Gran parte della responsabilità di mantenere la coerenza spetta allo sviluppatore di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="83f04-114">Much of the responsibility for maintaining consistency falls to the application developer.</span></span>

</dd> <dt>

<span data-ttu-id="83f04-115"><span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>Isolato</span><span class="sxs-lookup"><span data-stu-id="83f04-115"><span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>Isolated</span></span>
</dt> <dd>

<span data-ttu-id="83f04-116">Una transazione deve essere un'unità di isolamento, il che significa che le transazioni simultanee devono comportarsi come se fossero l'unica transazione in esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="83f04-116">A transaction must be a unit of isolation, which means that concurrent transactions should behave as if each were the only transaction running in the system.</span></span> <span data-ttu-id="83f04-117">Poiché un livello elevato di isolamento può limitare il numero di transazioni simultanee, alcune applicazioni riducono il livello di isolamento in Exchange per una migliore velocità effettiva.</span><span class="sxs-lookup"><span data-stu-id="83f04-117">Because a high degree of isolation can limit the number of concurrent transactions, some applications reduce the isolation level in exchange for better throughput.</span></span> <span data-ttu-id="83f04-118">Per ulteriori informazioni, vedere [configurazione dei livelli di isolamento delle transazioni](configuring-transaction-isolation-levels.md) .</span><span class="sxs-lookup"><span data-stu-id="83f04-118">See [Configuring Transaction Isolation Levels](configuring-transaction-isolation-levels.md) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="83f04-119"><span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Durevole</span><span class="sxs-lookup"><span data-stu-id="83f04-119"><span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Durable</span></span>
</dt> <dd>

<span data-ttu-id="83f04-120">Una transazione deve essere reversibile e pertanto deve avere durabilità.</span><span class="sxs-lookup"><span data-stu-id="83f04-120">A transaction must be recoverable and therefore must have durability.</span></span> <span data-ttu-id="83f04-121">Se viene eseguito il commit di una transazione, il sistema garantisce che gli aggiornamenti possano essere mantenuti anche se il computer si arresta immediatamente dopo il commit.</span><span class="sxs-lookup"><span data-stu-id="83f04-121">If a transaction commits, the system guarantees that its updates can persist even if the computer crashes immediately after the commit.</span></span> <span data-ttu-id="83f04-122">La registrazione specializzata consente alla procedura di riavvio del sistema di completare le operazioni non completate richieste dalla transazione, rendendo la transazione durevole.</span><span class="sxs-lookup"><span data-stu-id="83f04-122">Specialized logging allows the system's restart procedure to complete unfinished operations required by the transaction, making the transaction durable.</span></span>

</dd> </dl>

 

 



