---
description: Integrazione di una risorsa in una transazione
ms.assetid: b41fe0aa-a4cf-4d4a-9543-8eb0b38f07a2
title: Integrazione di una risorsa in una transazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db0a0bf93f373872c8be79054899dea4199dda7e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401513"
---
# <a name="enlisting-a-resource-in-a-transaction"></a><span data-ttu-id="b0705-103">Integrazione di una risorsa in una transazione</span><span class="sxs-lookup"><span data-stu-id="b0705-103">Enlisting a Resource in a Transaction</span></span>

<span data-ttu-id="b0705-104">Dopo che una risorsa è stata allocata, ma appena prima di restituire la risorsa al dispenser di risorse, il gestore del dispenser verifica con COM+ se l'oggetto chiamante è in esecuzione all'interno di una transazione.</span><span class="sxs-lookup"><span data-stu-id="b0705-104">After a resource is allocated, but just before returning the resource to the resource dispenser, the dispenser manager checks with COM+ to see whether the calling object is running within a transaction.</span></span> <span data-ttu-id="b0705-105">Se l'oggetto chiamante è in esecuzione all'interno di una transazione, il gestore del dispenser chiama di nuovo il dispenser di risorse e chiede di integrare la risorsa nella transazione.</span><span class="sxs-lookup"><span data-stu-id="b0705-105">If the calling object is running within a transaction, the dispenser manager calls back to the resource dispenser and asks it to enlist the resource in the transaction.</span></span> <span data-ttu-id="b0705-106">La risorsa viene quindi restituita al dispenser di risorse, che quindi la restituisce all'istanza chiamante.</span><span class="sxs-lookup"><span data-stu-id="b0705-106">Then the resource is returned to the resource dispenser, which then returns it to the calling instance.</span></span>

<span data-ttu-id="b0705-107">Il dispenser di risorse deve essere in grado di integrarsi in una transazione OLE con il Distributed Transaction Coordinator (DTC).</span><span class="sxs-lookup"><span data-stu-id="b0705-107">The resource dispenser must be able to enlist in an OLE transaction with the Distributed Transaction Coordinator (DTC).</span></span>

> [!Note]  
> <span data-ttu-id="b0705-108">L'integrazione delle transazioni è facoltativa quando un dispenser di risorse distribuisce risorse non transazionali, ad esempio memoria o thread.</span><span class="sxs-lookup"><span data-stu-id="b0705-108">Transaction enlistment is optional when a resource dispenser dispenses non-transactional resources, such as memory or threads.</span></span>

 

<span data-ttu-id="b0705-109">Quando una transazione viene completata, COM+ notifica al gestore del dispenser se è stato eseguito il commit o l'interruzione.</span><span class="sxs-lookup"><span data-stu-id="b0705-109">When a transaction is complete, COM+ notifies the dispenser manager about whether it committed or aborted.</span></span> <span data-ttu-id="b0705-110">Quindi, il responsabile del dispenser informa il titolare di ogni distributore che le risorse integrate in questa transazione possono ora essere spostate nell'inventario generale.</span><span class="sxs-lookup"><span data-stu-id="b0705-110">Then the dispenser manager notifies each resource dispenser's holder that any resources enlisted in this transaction can now be moved to general inventory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0705-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b0705-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0705-112">Concetti relativi al dispenser di risorse COM+</span><span class="sxs-lookup"><span data-stu-id="b0705-112">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="b0705-113">Stati risorse in pool disponibili per il dispenser di risorse COM+</span><span class="sxs-lookup"><span data-stu-id="b0705-113">Pooled Resource States Available to COM+ Resource Dispenser</span></span>](pooled-resource-states-available-to-com--resource-dispenser.md)
</dt> <dt>

[<span data-ttu-id="b0705-114">Processo di allocazione delle risorse del dispenser di risorse</span><span class="sxs-lookup"><span data-stu-id="b0705-114">Resource Dispenser Resource Allocation Process</span></span>](resource-dispenser-resource-allocation-process.md)
</dt> </dl>

 

 



