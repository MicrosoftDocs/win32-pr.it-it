---
description: COM+ gestisce automaticamente i thread. Ogni componente COM dispone di una proprietà ThreadingModel che è possibile specificare quando si sviluppa il componente. Questa proprietà determina il modo in cui gli oggetti Components vengono assegnati ai thread per l'esecuzione del metodo.
ms.assetid: 5fae8475-3d2e-4939-80a7-bc9a677a50b3
title: Attributo del modello di threading
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91960a753b29ac5f5209a5bafa31c362f3dfe08d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401398"
---
# <a name="threading-model-attribute"></a><span data-ttu-id="459c0-105">Attributo del modello di threading</span><span class="sxs-lookup"><span data-stu-id="459c0-105">Threading Model Attribute</span></span>

<span data-ttu-id="459c0-106">COM+ gestisce automaticamente i thread.</span><span class="sxs-lookup"><span data-stu-id="459c0-106">COM+ manages threads for you.</span></span> <span data-ttu-id="459c0-107">Ogni componente COM dispone di una proprietà **ThreadingModel** che è possibile specificare quando si sviluppa il componente.</span><span class="sxs-lookup"><span data-stu-id="459c0-107">Every COM component has a **ThreadingModel** property that you can specify when you develop the component.</span></span> <span data-ttu-id="459c0-108">Questa proprietà determina il modo in cui gli oggetti del componente vengono assegnati ai thread per l'esecuzione del metodo.</span><span class="sxs-lookup"><span data-stu-id="459c0-108">This property determines how the component's objects are assigned to threads for method execution.</span></span>

<span data-ttu-id="459c0-109">È possibile utilizzare lo strumento di amministrazione Servizi componenti per visualizzare la proprietà del modello di threading facendo clic con il pulsante destro del mouse su un componente nella cartella **componenti** , scegliendo **Proprietà**, quindi facendo clic sulla scheda **concorrenza** . In **modello di threading** i valori possibili sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="459c0-109">You can use the Component Services administrative tool to view the threading-model property by right-clicking a component in the **Components** folder, clicking **Properties**, and then clicking the **Concurrency** tab. Under **Threading Model**, the possible values are as follows:</span></span>

-   <span data-ttu-id="459c0-110">**Apartment thread principale**</span><span class="sxs-lookup"><span data-stu-id="459c0-110">**Main Thread Apartment**</span></span>
-   <span data-ttu-id="459c0-111">**Apartment a thread singolo**</span><span class="sxs-lookup"><span data-stu-id="459c0-111">**Single Thread Apartment**</span></span>
-   <span data-ttu-id="459c0-112">**Apartment thread libero**</span><span class="sxs-lookup"><span data-stu-id="459c0-112">**Free Thread Apartment**</span></span>
-   <span data-ttu-id="459c0-113">**Apartment neutro**</span><span class="sxs-lookup"><span data-stu-id="459c0-113">**Neutral Apartment**</span></span>
-   <span data-ttu-id="459c0-114">**Qualsiasi Apartment**</span><span class="sxs-lookup"><span data-stu-id="459c0-114">**Any Apartment**</span></span>

<span data-ttu-id="459c0-115">Il modello di threading preferito per COM+ è l' [Apartment neutro](neutral-apartments.md).</span><span class="sxs-lookup"><span data-stu-id="459c0-115">The preferred threading model for COM+ is the [neutral apartment](neutral-apartments.md).</span></span> <span data-ttu-id="459c0-116">Tuttavia, se non si specifica un modello di threading per il componente, COM+ utilizza l'Apartment thread principale, che è l'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="459c0-116">However, if you do not specify a threading model for your component, COM+ uses the main thread apartment, which is the default.</span></span>

> [!Note]  
> <span data-ttu-id="459c0-117">Per informazioni più dettagliate, vedere [scelta del modello di threading](/windows/desktop/com/choosing-the-threading-model).</span><span class="sxs-lookup"><span data-stu-id="459c0-117">For more detailed information, see [Choosing the Threading Model](/windows/desktop/com/choosing-the-threading-model).</span></span>

 

<span data-ttu-id="459c0-118">La tabella seguente illustra il modello di programmazione per gli appartamenti in COM+.</span><span class="sxs-lookup"><span data-stu-id="459c0-118">The following table shows the programming model for apartments in COM+.</span></span>



| <span data-ttu-id="459c0-119">Modello</span><span class="sxs-lookup"><span data-stu-id="459c0-119">Model</span></span>                     | <span data-ttu-id="459c0-120">Apartment</span><span class="sxs-lookup"><span data-stu-id="459c0-120">Apartment</span></span>                                                 | <span data-ttu-id="459c0-121">Gratuito</span><span class="sxs-lookup"><span data-stu-id="459c0-121">Free</span></span>                               | <span data-ttu-id="459c0-122">Entrambi</span><span class="sxs-lookup"><span data-stu-id="459c0-122">Both</span></span>                               | <span data-ttu-id="459c0-123">Neutralità</span><span class="sxs-lookup"><span data-stu-id="459c0-123">Neutral</span></span>                      | <span data-ttu-id="459c0-124">Non specificato</span><span class="sxs-lookup"><span data-stu-id="459c0-124">Not Specified</span></span>                      |
|---------------------------|-----------------------------------------------------------|------------------------------------|------------------------------------|------------------------------|------------------------------------|
| <span data-ttu-id="459c0-125">A thread singolo, non principale</span><span class="sxs-lookup"><span data-stu-id="459c0-125">Single-threaded, not main</span></span> | <span data-ttu-id="459c0-126">Creato nell'Apartment corrente</span><span class="sxs-lookup"><span data-stu-id="459c0-126">Created in current apartment</span></span>                              | <span data-ttu-id="459c0-127">Creato in un Apartment a thread multipli</span><span class="sxs-lookup"><span data-stu-id="459c0-127">Created in multithreaded apartment</span></span> | <span data-ttu-id="459c0-128">Creato nell'Apartment corrente</span><span class="sxs-lookup"><span data-stu-id="459c0-128">Created in current apartment</span></span>       | <span data-ttu-id="459c0-129">Creato in un Apartment neutro</span><span class="sxs-lookup"><span data-stu-id="459c0-129">Created in neutral apartment</span></span> | <span data-ttu-id="459c0-130">Creato nell'Apartment a thread principale</span><span class="sxs-lookup"><span data-stu-id="459c0-130">Created in main threaded apartment</span></span> |
| <span data-ttu-id="459c0-131">A thread singolo, principale</span><span class="sxs-lookup"><span data-stu-id="459c0-131">Single-threaded, main</span></span>     | <span data-ttu-id="459c0-132">Creato nell'Apartment corrente</span><span class="sxs-lookup"><span data-stu-id="459c0-132">Created in current apartment</span></span>                              | <span data-ttu-id="459c0-133">Creato in un Apartment a thread multipli</span><span class="sxs-lookup"><span data-stu-id="459c0-133">Created in multithreaded apartment</span></span> | <span data-ttu-id="459c0-134">Creato nell'Apartment corrente</span><span class="sxs-lookup"><span data-stu-id="459c0-134">Created in current apartment</span></span>       | <span data-ttu-id="459c0-135">Creato in un Apartment neutro</span><span class="sxs-lookup"><span data-stu-id="459c0-135">Created in neutral apartment</span></span> | <span data-ttu-id="459c0-136">Creato nell'Apartment corrente</span><span class="sxs-lookup"><span data-stu-id="459c0-136">Created in current apartment</span></span>       |
| <span data-ttu-id="459c0-137">Multithreading</span><span class="sxs-lookup"><span data-stu-id="459c0-137">Multithreaded</span></span>             | <span data-ttu-id="459c0-138">Creato nell'Apartment a thread singolo host</span><span class="sxs-lookup"><span data-stu-id="459c0-138">Created in host single-threaded apartment</span></span>                 | <span data-ttu-id="459c0-139">Creato in un Apartment a thread multipli</span><span class="sxs-lookup"><span data-stu-id="459c0-139">Created in multithreaded apartment</span></span> | <span data-ttu-id="459c0-140">Creato in un Apartment a thread multipli</span><span class="sxs-lookup"><span data-stu-id="459c0-140">Created in multithreaded apartment</span></span> | <span data-ttu-id="459c0-141">Creato in un Apartment neutro</span><span class="sxs-lookup"><span data-stu-id="459c0-141">Created in neutral apartment</span></span> | <span data-ttu-id="459c0-142">Creato nell'Apartment a thread principale</span><span class="sxs-lookup"><span data-stu-id="459c0-142">Created in main threaded apartment</span></span> |
| <span data-ttu-id="459c0-143">Neutro (sul thread STA)</span><span class="sxs-lookup"><span data-stu-id="459c0-143">Neutral (on STA thread)</span></span>   | <span data-ttu-id="459c0-144">Creato nell'Apartment a thread singolo host per questo thread</span><span class="sxs-lookup"><span data-stu-id="459c0-144">Created in host single-threaded apartment for this thread</span></span> | <span data-ttu-id="459c0-145">Creato in un Apartment a thread multipli</span><span class="sxs-lookup"><span data-stu-id="459c0-145">Created in multithreaded apartment</span></span> | <span data-ttu-id="459c0-146">Creato in un Apartment neutro</span><span class="sxs-lookup"><span data-stu-id="459c0-146">Created in neutral apartment</span></span>       | <span data-ttu-id="459c0-147">Creato in un Apartment neutro</span><span class="sxs-lookup"><span data-stu-id="459c0-147">Created in neutral apartment</span></span> | <span data-ttu-id="459c0-148">Creato nell'Apartment a thread principale</span><span class="sxs-lookup"><span data-stu-id="459c0-148">Created in main threaded apartment</span></span> |
| <span data-ttu-id="459c0-149">Neutro (su thread MTA)</span><span class="sxs-lookup"><span data-stu-id="459c0-149">Neutral (on MTA thread)</span></span>   | <span data-ttu-id="459c0-150">Creato nell'Apartment a thread singolo host</span><span class="sxs-lookup"><span data-stu-id="459c0-150">Created in host single-threaded apartment</span></span>                 | <span data-ttu-id="459c0-151">Creato in un Apartment a thread multipli</span><span class="sxs-lookup"><span data-stu-id="459c0-151">Created in multithreaded apartment</span></span> | <span data-ttu-id="459c0-152">Creato in un Apartment neutro</span><span class="sxs-lookup"><span data-stu-id="459c0-152">Created in neutral apartment</span></span>       | <span data-ttu-id="459c0-153">Creato in un Apartment neutro</span><span class="sxs-lookup"><span data-stu-id="459c0-153">Created in neutral apartment</span></span> | <span data-ttu-id="459c0-154">Creato nell'Apartment a thread principale</span><span class="sxs-lookup"><span data-stu-id="459c0-154">Created in main threaded apartment</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="459c0-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="459c0-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="459c0-156">**ThreadingModel**</span><span class="sxs-lookup"><span data-stu-id="459c0-156">**ThreadingModel**</span></span>](components.md)
</dt> </dl>

 

 
