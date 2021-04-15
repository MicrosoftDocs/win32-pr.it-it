---
description: Stati risorse in pool disponibili per il dispenser di risorse COM+
ms.assetid: 5037f11c-d113-49b0-b26f-0e3bc59ae8b3
title: Stati risorse in pool disponibili per il dispenser di risorse COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff0bc59dcc2b7e95e060c0d6e96a5880d09d26e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483429"
---
# <a name="pooled-resource-states-available-to-com-resource-dispenser"></a><span data-ttu-id="05873-103">Stati risorse in pool disponibili per il dispenser di risorse COM+</span><span class="sxs-lookup"><span data-stu-id="05873-103">Pooled Resource States Available to COM+ Resource Dispenser</span></span>

<span data-ttu-id="05873-104">In qualsiasi momento, una risorsa è in uso o non è in uso e può essere integrata o non integrata in una transazione.</span><span class="sxs-lookup"><span data-stu-id="05873-104">At any one time, a resource is either in use or not in use and is either enlisted or not enlisted in a transaction.</span></span> <span data-ttu-id="05873-105">In questo modo si producono quattro stati possibili per le risorse, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="05873-105">This yields four possible resource states, as follows:</span></span>

-   <span data-ttu-id="05873-106">**Risorse nell'inventario rimosso.**</span><span class="sxs-lookup"><span data-stu-id="05873-106">**Resources in unenlisted inventory.**</span></span> <span data-ttu-id="05873-107">Una risorsa che non è utilizzata da un oggetto e non è integrata in una transazione si trova nell'inventario rimosso.</span><span class="sxs-lookup"><span data-stu-id="05873-107">A resource that is not in use by an object and not enlisted in a transaction is in unenlisted inventory.</span></span> <span data-ttu-id="05873-108">Una risorsa nell'inventario generale è disponibile per l'assegnazione.</span><span class="sxs-lookup"><span data-stu-id="05873-108">A resource in general inventory is available for assignment.</span></span>

-   <span data-ttu-id="05873-109">**Risorse nell'inventario integrato.**</span><span class="sxs-lookup"><span data-stu-id="05873-109">**Resources in enlisted inventory.**</span></span> <span data-ttu-id="05873-110">Una risorsa che non è utilizzata da un oggetto ma è integrata in una transazione è nell'inventario integrato.</span><span class="sxs-lookup"><span data-stu-id="05873-110">A resource that is not in use by an object but is enlisted in a transaction is in enlisted inventory.</span></span> <span data-ttu-id="05873-111">Tale risorsa è disponibile per l'assegnazione solo a oggetti in esecuzione nella stessa transazione.</span><span class="sxs-lookup"><span data-stu-id="05873-111">Such a resource is available for assignment only to objects running in the same transaction.</span></span> <span data-ttu-id="05873-112">Una risorsa passa dall'inventario integrato all'inventario rimosso quando COM+ notifica al gestore del dispenser che la transazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="05873-112">A resource moves from enlisted inventory to unenlisted inventory when COM+ notifies the dispenser manager that the transaction is complete.</span></span>

-   <span data-ttu-id="05873-113">**Risorse in uso rimosso.**</span><span class="sxs-lookup"><span data-stu-id="05873-113">**Resources in unenlisted use.**</span></span> <span data-ttu-id="05873-114">Se una risorsa viene assegnata a un oggetto e l'istanza non è in esecuzione in una transazione o il dispenser di risorse ha identificato la risorsa come non transazionale, questa risorsa è in uso non integrato.</span><span class="sxs-lookup"><span data-stu-id="05873-114">If a resource is assigned to an object and the instance is not running in a transaction or the resource dispenser has identified the resource as non-transactional, this resource is in unenlisted use.</span></span>

-   <span data-ttu-id="05873-115">**Risorse in uso integrata.**</span><span class="sxs-lookup"><span data-stu-id="05873-115">**Resources in enlisted use.**</span></span> <span data-ttu-id="05873-116">Se una risorsa viene assegnata a un oggetto, l'istanza è in esecuzione in una transazione e il dispenser di risorse ha integrato correttamente la risorsa nella transazione, questa risorsa viene utilizzata nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="05873-116">If a resource is assigned to an object, the instance is running in a transaction, and the resource dispenser has successfully enlisted the resource in the transaction, this resource is in enlisted use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05873-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="05873-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05873-118">Concetti relativi al dispenser di risorse COM+</span><span class="sxs-lookup"><span data-stu-id="05873-118">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="05873-119">Integrazione di una risorsa in una transazione</span><span class="sxs-lookup"><span data-stu-id="05873-119">Enlisting a Resource in a Transaction</span></span>](enlisting-a-resource-in-a-transaction.md)
</dt> </dl>

 

 



