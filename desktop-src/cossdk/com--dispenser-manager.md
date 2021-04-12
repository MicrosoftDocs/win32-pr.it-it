---
description: Il gestore di dispenser fornisce il pool di risorse per i distributori di risorse e assicura che una risorsa fornita da un dispenser di risorse sia correttamente integrata nella transazione oggetti applicazione.
ms.assetid: c8986943-56a1-4668-9e80-7ab2a42333a8
title: Gestore di distribuzioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2422b7debb8ee12ed97444f3b16f31e663e1e71
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523578"
---
# <a name="com-dispenser-manager"></a><span data-ttu-id="fd6c9-103">Gestore di distribuzioni COM+</span><span class="sxs-lookup"><span data-stu-id="fd6c9-103">COM+ Dispenser Manager</span></span>

<span data-ttu-id="fd6c9-104">Il responsabile del dispenser fornisce il pool di risorse per i distributori di risorse e assicura che una risorsa fornita da un dispenser di risorse sia correttamente integrata nella transazione dell'oggetto applicazione.</span><span class="sxs-lookup"><span data-stu-id="fd6c9-104">The dispenser manager provides resource pooling for the resource dispensers and ensures that a resource supplied by a resource dispenser is correctly enlisted in the application object's transaction.</span></span> <span data-ttu-id="fd6c9-105">Il gestore del dispenser recupera automaticamente le risorse ancora riservate alla fine della durata di un oggetto, eliminando la possibilità di perdita di risorse.</span><span class="sxs-lookup"><span data-stu-id="fd6c9-105">The dispenser manager automatically reclaims resources that are still reserved at the end of an object's lifetime, eliminating the possibility of resource "leaks."</span></span> <span data-ttu-id="fd6c9-106">Il responsabile del dispenser può richiedere a un dispenser di risorse di creare una nuova risorsa o eliminare le risorse inattive quando necessario per modificare i livelli di inventario, anziché usare impostazioni statiche.</span><span class="sxs-lookup"><span data-stu-id="fd6c9-106">The dispenser manager can ask a resource dispenser to create a new resource or to destroy idle resources when necessary to adjust inventory levels, rather than using static settings.</span></span>

> [!Note]  
> <span data-ttu-id="fd6c9-107">Poiché le interfacce del dispenser di risorse esposte all'applicazione non devono essere interfacce COM, il gestore di dispenser può essere usato in un processo senza inizializzare COM, ad esempio per supportare il dispenser di risorse ODBC.</span><span class="sxs-lookup"><span data-stu-id="fd6c9-107">Because resource dispenser interfaces exposed to the application are not required to be COM interfaces, the dispenser manager can be used in a process without initializing COM, for example, to support the ODBC resource dispenser.</span></span>

 

<span data-ttu-id="fd6c9-108">Al momento della creazione delle risorse, il dispenser di risorse può specificare per quanto tempo è consentita la permanenza di una risorsa inattiva nel pool prima che venga distrutta.</span><span class="sxs-lookup"><span data-stu-id="fd6c9-108">Upon resource creation, the resource dispenser may specify how long an idle resource is allowed to remain in the pool before it's destroyed.</span></span> <span data-ttu-id="fd6c9-109">Un thread che viene eseguito in Gestione dispenser cerca sempre queste risorse inattive.</span><span class="sxs-lookup"><span data-stu-id="fd6c9-109">A thread that runs in the dispenser manager is always looking for these idle resources.</span></span>

## <a name="the-inventory-statistics-manager"></a><span data-ttu-id="fd6c9-110">Gestione statistiche inventario</span><span class="sxs-lookup"><span data-stu-id="fd6c9-110">The Inventory Statistics Manager</span></span>

<span data-ttu-id="fd6c9-111">Il gestore di dispenser USA *Inventory Statistics Manager* per gestire i livelli di inventario delle risorse del pool.</span><span class="sxs-lookup"><span data-stu-id="fd6c9-111">The dispenser manager uses the *inventory statistics manager* to manage pool resource inventory levels.</span></span> <span data-ttu-id="fd6c9-112">Inventory Statistics Manager mantiene un record del momento in cui ogni risorsa è stata usata e rimuove le risorse dall'inventario quando non sono state usate per *x* secondi, in cui il valore di *x* viene impostato per ogni risorsa quando viene creata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="fd6c9-112">The inventory statistics manager maintains a record of when each resource was used and removes resources from inventory when they have not been used for *x* seconds, where the value of *x* is set per resource when the resource is created.</span></span>

## <a name="the-holder-component"></a><span data-ttu-id="fd6c9-113">Componente del contenitore</span><span class="sxs-lookup"><span data-stu-id="fd6c9-113">The Holder Component</span></span>

<span data-ttu-id="fd6c9-114">Il responsabile del dispenser esegue il polling di ogni *titolare*, un componente creato dal responsabile del dispenser, che elenca l'inventario delle risorse per ogni dispenser di risorse, ogni 10 secondi per consentire la modifica dell'inventario delle risorse.</span><span class="sxs-lookup"><span data-stu-id="fd6c9-114">The dispenser manager polls each *holder*, a component created by the dispenser manager that lists the resource inventory for each resource dispenser, every 10 seconds to allow it to readjust its resource inventory.</span></span> <span data-ttu-id="fd6c9-115">Ogni titolare chiama Inventory Statistics Manager per suggerire i livelli di inventario per ogni tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="fd6c9-115">Each holder calls the inventory statistics manager to suggest inventory levels for each type of resource.</span></span> <span data-ttu-id="fd6c9-116">Di conseguenza, il titolare può richiedere al dispenser di risorse di creare o distruggere un inventario.</span><span class="sxs-lookup"><span data-stu-id="fd6c9-116">As a result, the holder may ask the resource dispenser to either create or destroy some inventory.</span></span>

<span data-ttu-id="fd6c9-117">Il titolare e il dispenser di risorse comunicano per richiedere risorse di un determinato tipo.</span><span class="sxs-lookup"><span data-stu-id="fd6c9-117">The holder and resource dispenser communicate to request resources of a particular type.</span></span> <span data-ttu-id="fd6c9-118">Tra il titolare e il dispenser di risorse esistono le relazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="fd6c9-118">The following relationships exist between the holder and resource dispenser:</span></span>

-   <span data-ttu-id="fd6c9-119">Il titolare può richiedere una risorsa dal dispenser di risorse.</span><span class="sxs-lookup"><span data-stu-id="fd6c9-119">The holder can request a resource from the resource dispenser.</span></span> <span data-ttu-id="fd6c9-120">Il dispenser di risorse restituisce una risorsa disponibile o ne crea uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="fd6c9-120">The resource dispenser either returns an available resource or creates a new one.</span></span>
-   <span data-ttu-id="fd6c9-121">Il titolare può notificare al dispenser di risorse che un'applicazione non necessita più di una risorsa e quindi restituirla al pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="fd6c9-121">The holder can notify the resource dispenser that an application no longer needs a resource and then return it to the resource pool.</span></span>
-   <span data-ttu-id="fd6c9-122">Il titolare e il dispenser di risorse interagiscono per mantenere le dimensioni del pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="fd6c9-122">The holder and the resource dispenser work together to maintain the size of the resource pool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd6c9-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fd6c9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd6c9-124">Concetti relativi al dispenser di risorse COM+</span><span class="sxs-lookup"><span data-stu-id="fd6c9-124">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



