---
description: Processo di allocazione delle risorse del dispenser di risorse
ms.assetid: 695d08f4-ba5c-4a5f-a2ad-481a8ede49ab
title: Processo di allocazione delle risorse del dispenser di risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a12cb22abd6d4d825f1ca048495b032a77fe216
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225634"
---
# <a name="resource-dispenser-resource-allocation-process"></a><span data-ttu-id="b97b1-103">Processo di allocazione delle risorse del dispenser di risorse</span><span class="sxs-lookup"><span data-stu-id="b97b1-103">Resource Dispenser Resource Allocation Process</span></span>

<span data-ttu-id="b97b1-104">Ogni volta che un dispenser di risorse alloca una risorsa dal relativo titolare, si verifica quanto segue:</span><span class="sxs-lookup"><span data-stu-id="b97b1-104">Each time a resource dispenser allocates a resource from its holder, the following occurs:</span></span>

1.  <span data-ttu-id="b97b1-105">Il dispenser di risorse dichiara un identificatore del tipo di risorsa (**RESTYPID**), che descrive il tipo di risorsa necessaria.</span><span class="sxs-lookup"><span data-stu-id="b97b1-105">The resource dispenser declares a resource type identifier (**RESTYPID**), which describes the type of resource required.</span></span>

2.  <span data-ttu-id="b97b1-106">Il dispenser di risorse chiama il metodo [**IHolder:: AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) del contenitore, passando questo **RESTYPID**.</span><span class="sxs-lookup"><span data-stu-id="b97b1-106">The resource dispenser calls the holder's [**IHolder::AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) method, passing this **RESTYPID**.</span></span>

3.  <span data-ttu-id="b97b1-107">Il titolare genera un elenco di candidati dalle risorse disponibili.</span><span class="sxs-lookup"><span data-stu-id="b97b1-107">The holder generates a candidate list from the available resources.</span></span> <span data-ttu-id="b97b1-108">I candidati sono risorse non integrate in una transazione o già integrate nella transazione dell'oggetto chiamante.</span><span class="sxs-lookup"><span data-stu-id="b97b1-108">Candidates are resources that are either not enlisted in a transaction or already enlisted in the calling object's transaction.</span></span>

4.  <span data-ttu-id="b97b1-109">Questi candidati vengono passati singolarmente al metodo [**IDispenserDriver:: RateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-rateresource) , in cui vengono classificati (su una scala da 0 a 100) in base alla corrispondenza tra la risorsa candidata e la **RESTYPID** desiderata.</span><span class="sxs-lookup"><span data-stu-id="b97b1-109">These candidates are individually passed to the [**IDispenserDriver::RateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-rateresource) method where they are rated (on a scale of 0 to 100) by how well the candidate resource matches the desired **RESTYPID**.</span></span>

5.  <span data-ttu-id="b97b1-110">Il titolare sceglie la risorsa che il dispenser di risorse è più alto.</span><span class="sxs-lookup"><span data-stu-id="b97b1-110">The holder chooses the resource that the resource dispenser rates as highest.</span></span>

6.  <span data-ttu-id="b97b1-111">Il dispenser di risorse può terminare il ciclo di classificazione in anticipo assegnando al candidato una valutazione delle risorse 100 (adattamento ottimale).</span><span class="sxs-lookup"><span data-stu-id="b97b1-111">The resource dispenser can terminate the rating loop early by assigning the candidate a resource rating of 100 (a perfect fit).</span></span> <span data-ttu-id="b97b1-112">Una classificazione di 100 verrebbe normalmente riservata per le risorse candidate che sono già state integrate correttamente, a meno che il dispenser di risorse non concluda che l'integrazione è un'operazione economica.</span><span class="sxs-lookup"><span data-stu-id="b97b1-112">A rating of 100 would normally be reserved for candidate resources that are already properly enlisted, unless the resource dispenser concludes that enlistment is an inexpensive operation.</span></span> <span data-ttu-id="b97b1-113">Se tutte le risorse candidate (se presenti) sono classificate come 0 (inutilizzabile), viene creata una nuova risorsa chiamando [**IDispenserDriver:: CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource).</span><span class="sxs-lookup"><span data-stu-id="b97b1-113">If all candidate resources (if any) are rated 0 (unusable), a new resource is created by calling [**IDispenserDriver::CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource).</span></span>

7.  <span data-ttu-id="b97b1-114">Se la risorsa scelta in precedenza non è già integrata nella transazione dell'oggetto chiamante, viene chiamato il metodo [**IDispenserDriver:: EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) del dispenser di risorse.</span><span class="sxs-lookup"><span data-stu-id="b97b1-114">If the resource chosen previously is not already enlisted in the calling object's transaction, the resource dispenser's [**IDispenserDriver::EnlistResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) method is called.</span></span>

8.  <span data-ttu-id="b97b1-115">La chiamata al metodo [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) restituisce il dispenser di risorse con la risorsa integrata.</span><span class="sxs-lookup"><span data-stu-id="b97b1-115">The [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) method call returns to the resource dispenser with the enlisted resource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b97b1-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b97b1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b97b1-117">Concetti relativi al dispenser di risorse COM+</span><span class="sxs-lookup"><span data-stu-id="b97b1-117">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="b97b1-118">Integrazione di una risorsa in una transazione</span><span class="sxs-lookup"><span data-stu-id="b97b1-118">Enlisting a Resource in a Transaction</span></span>](enlisting-a-resource-in-a-transaction.md)
</dt> <dt>

[<span data-ttu-id="b97b1-119">Rilevamento di risorse non allocate</span><span class="sxs-lookup"><span data-stu-id="b97b1-119">Tracking Non-Allocated Resources</span></span>](tracking-non-allocated-resources.md)
</dt> </dl>

 

 



