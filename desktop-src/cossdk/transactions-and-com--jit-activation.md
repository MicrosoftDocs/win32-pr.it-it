---
description: Transazioni e attivazione JIT COM+
ms.assetid: f7fad383-4081-4a49-aa03-59861fcefc97
title: Transazioni e attivazione JIT COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281691ebc9c8d5c654ea6ff0c3035d7e285f62c5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878194"
---
# <a name="transactions-and-com-jit-activation"></a><span data-ttu-id="92344-103">Transazioni e attivazione JIT COM+</span><span class="sxs-lookup"><span data-stu-id="92344-103">Transactions and COM+ JIT Activation</span></span>

<span data-ttu-id="92344-104">L'attivazione JIT COM+ è strettamente associata a transazioni automatiche.</span><span class="sxs-lookup"><span data-stu-id="92344-104">COM+ JIT Activation is closely bound to automatic transactions.</span></span> <span data-ttu-id="92344-105">Quando si configura un componente in modo da richiedere una transazione o richiede una nuova transazione, viene abilitata automaticamente anche l'attivazione JIT.</span><span class="sxs-lookup"><span data-stu-id="92344-105">When you configure a component so that it requires a transaction or requires a new transaction, JIT Activation is automatically enabled as well.</span></span> <span data-ttu-id="92344-106">Le due funzionalità funzionano naturalmente insieme.</span><span class="sxs-lookup"><span data-stu-id="92344-106">The two features naturally work in conjunction.</span></span> <span data-ttu-id="92344-107">I componenti con attivazione JIT transazionale condividono le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="92344-107">Transactional, JIT-activated components share the following characteristics:</span></span>

-   <span data-ttu-id="92344-108">Apolidia.</span><span class="sxs-lookup"><span data-stu-id="92344-108">Statelessness.</span></span> <span data-ttu-id="92344-109">Non si terrebbe lo stato che violerebbe l'isolamento delle transazioni, né lo stato che andrebbe perso per la disattivazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="92344-109">You would not hold state that would violate transaction isolation nor would you hold state that would be lost on object deactivation.</span></span>

-   <span data-ttu-id="92344-110">Utilizzo rapido.</span><span class="sxs-lookup"><span data-stu-id="92344-110">Rapid use.</span></span> <span data-ttu-id="92344-111">Il modello di utilizzo canonico per un oggetto che esegue il lavoro in una transazione automatica consiste nell'eseguire alcune piccole unità di lavoro, voto ed uscita.</span><span class="sxs-lookup"><span data-stu-id="92344-111">The canonical use pattern for an object performing work in an automatic transaction is to do some small unit of work, vote, and exit.</span></span>

    > [!Note]  
    > <span data-ttu-id="92344-112">Anche i modi in cui si votano le transazioni COM+ e l'operazione di segnalazione per l'attivazione JIT sono strettamente associati.</span><span class="sxs-lookup"><span data-stu-id="92344-112">The ways that you vote in COM+ transactions and signal doneness for JIT Activation are also closely bound together.</span></span> <span data-ttu-id="92344-113">Per ulteriori informazioni, vedere [impostazione del bit fatto](setting-the-done-bit.md).</span><span class="sxs-lookup"><span data-stu-id="92344-113">For more information, see [Setting the Done Bit](setting-the-done-bit.md).</span></span>

     

-   <span data-ttu-id="92344-114">Uso ripetuto.</span><span class="sxs-lookup"><span data-stu-id="92344-114">Repeated use.</span></span> <span data-ttu-id="92344-115">Quando il lavoro transazionale viene suddiviso correttamente, i client utilizzano gli stessi oggetti più volte per eseguire piccoli pacchi di lavoro atomico.</span><span class="sxs-lookup"><span data-stu-id="92344-115">When transactional work is properly broken up, clients use the same objects over and over to perform little parcels of atomic work.</span></span>

-   <span data-ttu-id="92344-116">Disattivato in commit o Abort.</span><span class="sxs-lookup"><span data-stu-id="92344-116">Deactivated on commit or abort.</span></span> <span data-ttu-id="92344-117">In COM+ tutti gli oggetti all'interno del limite della transazione vengono disattivati quando viene eseguito il commit o l'interruzione della transazione.</span><span class="sxs-lookup"><span data-stu-id="92344-117">In COM+, all objects within the transaction boundary are deactivated when the transaction commits or aborts.</span></span>

<span data-ttu-id="92344-118">Insieme ai componenti transazionali COM+, l'attivazione JIT funge da notevole miglioramento delle prestazioni mantenendo il canale aperto perché i client contengono riferimenti di lunga durata a oggetti transazionali.</span><span class="sxs-lookup"><span data-stu-id="92344-118">In conjunction with COM+ transactional components, JIT activation serves as a big performance enhancement by keeping the channel open as clients hold long-lived references to transactional objects.</span></span> <span data-ttu-id="92344-119">Per ulteriori miglioramenti, è possibile scegliere di raggruppare gli oggetti transazionali per riutilizzare le risorse in essi contenute, velocizzare il tempo di riattivazione degli oggetti e gestire in modo accurato la modalità di utilizzo delle risorse di memoria per gli oggetti specificati.</span><span class="sxs-lookup"><span data-stu-id="92344-119">As further enhancements, you can elect to pool the transactional objects to reuse the resources they hold, speed object reactivation time, and closely manage how you use memory resources for given objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92344-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="92344-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92344-121">Concetti relativi all'attivazione JIT di COM+</span><span class="sxs-lookup"><span data-stu-id="92344-121">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="92344-122">Abilitazione dell'attivazione JIT per un componente</span><span class="sxs-lookup"><span data-stu-id="92344-122">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="92344-123">Pool di oggetti e attivazione JIT COM+</span><span class="sxs-lookup"><span data-stu-id="92344-123">Object Pooling and COM+ JIT Activation</span></span>](object-pooling-and-com--jit-activation.md)
</dt> </dl>

 

 



