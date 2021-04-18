---
description: ICE62 esegue verifiche complete sulla tabella IsolatedComponent per i dati che possono causare un comportamento imprevisto.
ms.assetid: 649d3989-8121-4303-aa3e-63bc6649f445
title: ICE62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245e205b2d004efa99ae1605ff5255ef69834a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314791"
---
# <a name="ice62"></a><span data-ttu-id="83dd3-103">ICE62</span><span class="sxs-lookup"><span data-stu-id="83dd3-103">ICE62</span></span>

<span data-ttu-id="83dd3-104">ICE62 esegue verifiche complete sulla [tabella IsolatedComponent](isolatedcomponent-table.md) per i dati che possono causare un comportamento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="83dd3-104">ICE62 performs extensive checks on the [IsolatedComponent table](isolatedcomponent-table.md) for data that may cause unexpected behavior.</span></span>

<span data-ttu-id="83dd3-105">La mancata correzione di un errore segnalato da ICE62 può comportare un errore del sistema di componenti isolati in un'ampia gamma di modi.</span><span class="sxs-lookup"><span data-stu-id="83dd3-105">Failure to fix an error reported by ICE62 can result in a failure of the isolated component system in a wide variety of ways.</span></span> <span data-ttu-id="83dd3-106">Se, ad esempio, il bit SharedDllRefCount non è impostato per un componente condiviso, la registrazione per il componente potrebbe essere rimossa quando un'altra applicazione usa tale ComponentId e viene disinstallata.</span><span class="sxs-lookup"><span data-stu-id="83dd3-106">For example, if the SharedDllRefCount bit is not set for a shared component, the registration for the component could be removed when another application uses that ComponentId and is uninstalled.</span></span>

## <a name="result"></a><span data-ttu-id="83dd3-107">Risultato</span><span class="sxs-lookup"><span data-stu-id="83dd3-107">Result</span></span>

<span data-ttu-id="83dd3-108">ICE62 Invia un avviso o un errore quando trova i dati nella tabella IsolatedComponent che possono produrre un comportamento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="83dd3-108">ICE62 posts a warning or error when it finds data in the IsolatedComponent table that may produce unexpected behavior.</span></span>

## <a name="example"></a><span data-ttu-id="83dd3-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="83dd3-109">Example</span></span>

<span data-ttu-id="83dd3-110">ICE62 segnala gli errori e gli avvisi seguenti per gli esempi mostrati.</span><span class="sxs-lookup"><span data-stu-id="83dd3-110">ICE62 reports the following errors and warning for the examples shown.</span></span>

``` syntax
The component 'Component2' is listed as an isolated application 
component in the IsolatedComponent table, but the key path is not a file.
```

<span data-ttu-id="83dd3-111">Component2 è elencato come componente dell'applicazione per l'isolamento di Component1.</span><span class="sxs-lookup"><span data-stu-id="83dd3-111">Component2 is listed as the application component for the isolation of component1.</span></span> <span data-ttu-id="83dd3-112">Tuttavia, Component2 dispone di un percorso della chiave del registro di sistema e non fornisce un percorso eseguibile valido da utilizzare per isolare il componente.</span><span class="sxs-lookup"><span data-stu-id="83dd3-112">However, Component2 has a registry key path, and does not provide a valid executable path to use to isolate the component.</span></span>

<span data-ttu-id="83dd3-113">Per correggere l'errore, usare un componente diverso come applicazione per il componente isolato Component1.</span><span class="sxs-lookup"><span data-stu-id="83dd3-113">To fix this error, use a different component as the application for the isolated component Component1.</span></span>

``` syntax
The component 'Component1' is listed as an isolated shared component in the 
IsolatedComponent table, but is not marked with the SharedDllRefCount component attribute.
```

<span data-ttu-id="83dd3-114">Component1 è elencato come componente condiviso isolato, ma non ha il bit SharedDllRefCount impostato.</span><span class="sxs-lookup"><span data-stu-id="83dd3-114">Component1 is listed as an isolated shared component, but does not have the SharedDllRefCount bit set.</span></span> <span data-ttu-id="83dd3-115">Questo potrebbe comportare la durata del componente non corretto.</span><span class="sxs-lookup"><span data-stu-id="83dd3-115">This could result in the lifetime of the component being incorrect.</span></span> <span data-ttu-id="83dd3-116">Se un'altra applicazione utilizza questo componente (isolato o meno) e viene disinstallato, la registrazione per il componente viene rimossa, ma la copia isolata di questa applicazione rimane.</span><span class="sxs-lookup"><span data-stu-id="83dd3-116">If another application uses this component (isolated or not) and is uninstalled, the registration for the component is removed but this application's isolated copy remains.</span></span> <span data-ttu-id="83dd3-117">Ciò causa problemi di ripristino e disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="83dd3-117">This causes repair and uninstall problems.</span></span>

<span data-ttu-id="83dd3-118">Per correggere l'errore, impostare il bit SharedDllRefCount per il componente.</span><span class="sxs-lookup"><span data-stu-id="83dd3-118">To fix this error, set the SharedDllRefCount bit for the component.</span></span>

``` syntax
The isolated shared component 'Component1' is not installed by the same feature as 
(or a parent feature of) its isolated application component 'Component2' (which is installed by feature 'Feature2').
```

<span data-ttu-id="83dd3-119">Component1 e Component2 vengono installati da diverse funzionalità.</span><span class="sxs-lookup"><span data-stu-id="83dd3-119">Component1 and Component2 are installed by different features.</span></span> <span data-ttu-id="83dd3-120">Component1 viene installato da Feature1 e Component2 viene installato da Funzionalità2.</span><span class="sxs-lookup"><span data-stu-id="83dd3-120">Component1 is installed by Feature1, and Component2 is installed by Feature2.</span></span> <span data-ttu-id="83dd3-121">Feature1 non è un elemento padre di funzionalità2, di conseguenza è possibile che l'applicazione sia installata, ma non il componente isolato, per suddividere l'isolamento.</span><span class="sxs-lookup"><span data-stu-id="83dd3-121">Feature1 is not a parent of Feature2, hence it is possible for the application to be installed but not the isolated component, breaking the isolation.</span></span>

<span data-ttu-id="83dd3-122">Per correggere l'errore, aggiungere una voce alla tabella FeatureComponents che collega Component1 alla stessa funzione di (o a una funzionalità padre di) la funzionalità che installa Component2.</span><span class="sxs-lookup"><span data-stu-id="83dd3-122">To fix this error, add an entry to the FeatureComponents table linking Component1 to the same feature as (or a parent feature of) the feature that installs Component2.</span></span>

``` syntax
WARNING: The isolated shared component 'Component1' (referenced in the IsolatedComponent table) 
is conditionalized. Isolated shared component conditions should never change from TRUE to FALSE after the first install of the product.
```

<span data-ttu-id="83dd3-123">Component1 presenta una condizione nella tabella dei componenti.</span><span class="sxs-lookup"><span data-stu-id="83dd3-123">Component1 has a condition in the Component table.</span></span> <span data-ttu-id="83dd3-124">Se questa condizione viene modificata da TRUE a FALSE durante il ciclo di vita di un'installazione di in un computer, il componente isolato potrebbe essere orfano senza informazioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="83dd3-124">If this condition ever changes from TRUE to FALSE during the lifetime of an installation on a computer, the isolated component could be orphaned without registration information.</span></span>

<span data-ttu-id="83dd3-125">Per correggere il problema, rimuovere la condizione oppure creare la condizione in modo che non possa mai passare da TRUE a FALSE.</span><span class="sxs-lookup"><span data-stu-id="83dd3-125">To fix this warning, remove the condition, or author the condition so that it can never change from TRUE to FALSE.</span></span>

``` syntax
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component2') that are installed to the directory 'TARGETDIR'.
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component3') that are installed to the directory 'TARGETDIR'.
```

<span data-ttu-id="83dd3-126">Component1 è isolato sia per Component2 che per Component3 e i due componenti vengono inoltre installati nella stessa directory.</span><span class="sxs-lookup"><span data-stu-id="83dd3-126">Component1 is isolated for both Component2 and Component3, and the two components are also installed to the same directory.</span></span> <span data-ttu-id="83dd3-127">Le applicazioni condividono un componente isolato, ma se un'applicazione viene rimossa, viene rimosso anche il componente condiviso, causando la perdita del componente isolato da parte di altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="83dd3-127">The applications share an isolated component, but if one application is removed the shared component is removed as well causing the other applications to lose the isolated component.</span></span>

<span data-ttu-id="83dd3-128">Per correggere il problema, installare le applicazioni in directory diverse o controllare se alcune applicazioni richiedono effettivamente un componente isolato.</span><span class="sxs-lookup"><span data-stu-id="83dd3-128">To fix this warning, install the applications to different directories or check whether some of the applications truly require an isolated component.</span></span>

[<span data-ttu-id="83dd3-129">Tabella IsolatedComponent</span><span class="sxs-lookup"><span data-stu-id="83dd3-129">IsolatedComponent Table</span></span>](isolatedcomponent-table.md)



| <span data-ttu-id="83dd3-130">Componente \_ condiviso</span><span class="sxs-lookup"><span data-stu-id="83dd3-130">Component\_Shared</span></span> | <span data-ttu-id="83dd3-131">\_Applicazione componente</span><span class="sxs-lookup"><span data-stu-id="83dd3-131">Component\_Application</span></span> |
|-------------------|------------------------|
| <span data-ttu-id="83dd3-132">Component1</span><span class="sxs-lookup"><span data-stu-id="83dd3-132">Component1</span></span>        | <span data-ttu-id="83dd3-133">Component2</span><span class="sxs-lookup"><span data-stu-id="83dd3-133">Component2</span></span>             |
| <span data-ttu-id="83dd3-134">Component1</span><span class="sxs-lookup"><span data-stu-id="83dd3-134">Component1</span></span>        | <span data-ttu-id="83dd3-135">Component3</span><span class="sxs-lookup"><span data-stu-id="83dd3-135">Component3</span></span>             |



 

[<span data-ttu-id="83dd3-136">Tabella componenti</span><span class="sxs-lookup"><span data-stu-id="83dd3-136">Component Table</span></span>](component-table.md)



| <span data-ttu-id="83dd3-137">Componente</span><span class="sxs-lookup"><span data-stu-id="83dd3-137">Component</span></span>  | <span data-ttu-id="83dd3-138">ComponentId</span><span class="sxs-lookup"><span data-stu-id="83dd3-138">ComponentId</span></span> | <span data-ttu-id="83dd3-139">Directory\_</span><span class="sxs-lookup"><span data-stu-id="83dd3-139">Directory\_</span></span> | <span data-ttu-id="83dd3-140">Attributi</span><span class="sxs-lookup"><span data-stu-id="83dd3-140">Attributes</span></span> | <span data-ttu-id="83dd3-141">Condizione</span><span class="sxs-lookup"><span data-stu-id="83dd3-141">Condition</span></span>   | <span data-ttu-id="83dd3-142">KeyPath</span><span class="sxs-lookup"><span data-stu-id="83dd3-142">KeyPath</span></span>   |
|------------|-------------|-------------|------------|-------------|-----------|
| <span data-ttu-id="83dd3-143">Component1</span><span class="sxs-lookup"><span data-stu-id="83dd3-143">Component1</span></span> |             | <span data-ttu-id="83dd3-144">Dir1</span><span class="sxs-lookup"><span data-stu-id="83dd3-144">Dir1</span></span>        | <span data-ttu-id="83dd3-145">0</span><span class="sxs-lookup"><span data-stu-id="83dd3-145">0</span></span>          | <span data-ttu-id="83dd3-146">MYCONDITION</span><span class="sxs-lookup"><span data-stu-id="83dd3-146">MYCONDITION</span></span> | <span data-ttu-id="83dd3-147">File1</span><span class="sxs-lookup"><span data-stu-id="83dd3-147">File1</span></span>     |
| <span data-ttu-id="83dd3-148">Component2</span><span class="sxs-lookup"><span data-stu-id="83dd3-148">Component2</span></span> |             | <span data-ttu-id="83dd3-149">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="83dd3-149">TARGETDIR</span></span>   | <span data-ttu-id="83dd3-150">4</span><span class="sxs-lookup"><span data-stu-id="83dd3-150">4</span></span>          |             | <span data-ttu-id="83dd3-151">Registry2</span><span class="sxs-lookup"><span data-stu-id="83dd3-151">Registry2</span></span> |
| <span data-ttu-id="83dd3-152">Component3</span><span class="sxs-lookup"><span data-stu-id="83dd3-152">Component3</span></span> |             | <span data-ttu-id="83dd3-153">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="83dd3-153">TARGETDIR</span></span>   | <span data-ttu-id="83dd3-154">0</span><span class="sxs-lookup"><span data-stu-id="83dd3-154">0</span></span>          |             | <span data-ttu-id="83dd3-155">File3</span><span class="sxs-lookup"><span data-stu-id="83dd3-155">File3</span></span>     |



 

[<span data-ttu-id="83dd3-156">FeatureComponentsTable</span><span class="sxs-lookup"><span data-stu-id="83dd3-156">FeatureComponentsTable</span></span>](featurecomponents-table.md)



| <span data-ttu-id="83dd3-157">Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="83dd3-157">Feature\_</span></span> | <span data-ttu-id="83dd3-158">Componente\_</span><span class="sxs-lookup"><span data-stu-id="83dd3-158">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="83dd3-159">Feature1</span><span class="sxs-lookup"><span data-stu-id="83dd3-159">Feature1</span></span>  | <span data-ttu-id="83dd3-160">Component1</span><span class="sxs-lookup"><span data-stu-id="83dd3-160">Component1</span></span>  |
| <span data-ttu-id="83dd3-161">Funzionalità2</span><span class="sxs-lookup"><span data-stu-id="83dd3-161">Feature2</span></span>  | <span data-ttu-id="83dd3-162">Component2</span><span class="sxs-lookup"><span data-stu-id="83dd3-162">Component2</span></span>  |
| <span data-ttu-id="83dd3-163">Feature1</span><span class="sxs-lookup"><span data-stu-id="83dd3-163">Feature1</span></span>  | <span data-ttu-id="83dd3-164">Component3</span><span class="sxs-lookup"><span data-stu-id="83dd3-164">Component3</span></span>  |



 

<span data-ttu-id="83dd3-165">[Tabella delle funzionalità](feature-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="83dd3-165">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="83dd3-166">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="83dd3-166">Feature</span></span>  | <span data-ttu-id="83dd3-167">\_Elemento padre della funzionalità</span><span class="sxs-lookup"><span data-stu-id="83dd3-167">Feature\_Parent</span></span> |
|----------|-----------------|
| <span data-ttu-id="83dd3-168">Feature1</span><span class="sxs-lookup"><span data-stu-id="83dd3-168">Feature1</span></span> |                 |
| <span data-ttu-id="83dd3-169">Funzionalità2</span><span class="sxs-lookup"><span data-stu-id="83dd3-169">Feature2</span></span> |                 |



 

## <a name="related-topics"></a><span data-ttu-id="83dd3-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="83dd3-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83dd3-171">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="83dd3-171">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



