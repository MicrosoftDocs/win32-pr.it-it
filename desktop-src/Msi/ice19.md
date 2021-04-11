---
description: ICE19 verifica che i componenti annunciati facciano riferimento a un file nella colonna percorso tasto della tabella dei componenti e che un collegamento annunciato faccia riferimento a una directory in questa colonna.
ms.assetid: 438153c1-bc4b-4ecf-ab85-d66ad69c987c
title: ICE19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a53aa3268a1c77f674d4a130c9de02c44b56243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232249"
---
# <a name="ice19"></a><span data-ttu-id="aaa5d-103">ICE19</span><span class="sxs-lookup"><span data-stu-id="aaa5d-103">ICE19</span></span>

<span data-ttu-id="aaa5d-104">ICE19 verifica che i componenti annunciati facciano riferimento a un file nella colonna percorso tasto della [tabella dei componenti](component-table.md) e che un collegamento annunciato faccia riferimento a una directory in questa colonna.</span><span class="sxs-lookup"><span data-stu-id="aaa5d-104">ICE19 validates that advertised components reference a file in the KeyPath column of the [Component table](component-table.md) and that an advertised shortcut references a directory in this column.</span></span>

<span data-ttu-id="aaa5d-105">ICE19 verifica che i collegamenti o i componenti annunciati dispongano di un ComponentId.</span><span class="sxs-lookup"><span data-stu-id="aaa5d-105">ICE19 validates that advertised components or shortcuts have a ComponentId.</span></span> <span data-ttu-id="aaa5d-106">I componenti della [tabella PublishComponent](publishcomponent-table.md), che non vengono annunciati in un'altra tabella, vengono controllati solo per verificare se hanno un ComponentID.</span><span class="sxs-lookup"><span data-stu-id="aaa5d-106">Components in the [PublishComponent table](publishcomponent-table.md), which are not advertised in another table, are only checked to see whether they have a ComponentId.</span></span>

## <a name="result"></a><span data-ttu-id="aaa5d-107">Risultato</span><span class="sxs-lookup"><span data-stu-id="aaa5d-107">Result</span></span>

<span data-ttu-id="aaa5d-108">ICE19 Invia un messaggio di errore se la colonna di percorso della tabella dei componenti non fa riferimento a un file nel caso di un componente annunciato o di una directory nel caso di un collegamento annunciato.</span><span class="sxs-lookup"><span data-stu-id="aaa5d-108">ICE19 posts an error message if the KeyPath column of the Component table does not reference a file in the case of an advertised component or a directory in the case of an advertised shortcut.</span></span> <span data-ttu-id="aaa5d-109">ICE19 Invia un messaggio di errore se i collegamenti o i componenti annunciati non dispongono di un ComponentId.</span><span class="sxs-lookup"><span data-stu-id="aaa5d-109">ICE19 posts an error message if any advertised components or shortcuts do not have a ComponentId.</span></span>

## <a name="example"></a><span data-ttu-id="aaa5d-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="aaa5d-110">Example</span></span>

<span data-ttu-id="aaa5d-111">ICE19 invia i messaggi di errore seguenti per l'esempio illustrato:</span><span class="sxs-lookup"><span data-stu-id="aaa5d-111">ICE19 posts the following error messages for the example shown:</span></span>

-   <span data-ttu-id="aaa5d-112">L'estensione FLP fa riferimento al componente comp1 che non contiene un ComponentId specificato nella [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="aaa5d-112">Extension flp references the component Comp1 which does not have a ComponentId specified in the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="aaa5d-113">Estensione exe fa riferimento al componente Comp4 che fa riferimento a una directory come percorso di proprietà.</span><span class="sxs-lookup"><span data-stu-id="aaa5d-113">Extension exe references the component Comp4 which references a directory as its KeyPath.</span></span> <span data-ttu-id="aaa5d-114">Il percorso della tabella dei componenti è null.</span><span class="sxs-lookup"><span data-stu-id="aaa5d-114">The KeyPath is Null in the Component table.</span></span>
-   <span data-ttu-id="aaa5d-115">Il collegamento Shortcut2 fa riferimento al componente COMP3 che fa riferimento a una voce del registro di sistema come percorso della chiave.</span><span class="sxs-lookup"><span data-stu-id="aaa5d-115">Shortcut Shortcut2 references the component Comp3 which references a Registry entry as the key path.</span></span> <span data-ttu-id="aaa5d-116">Il valore della colonna attributi nella tabella dei componenti è 4.</span><span class="sxs-lookup"><span data-stu-id="aaa5d-116">The value of the Attributes column in the Component table is 4.</span></span>

<span data-ttu-id="aaa5d-117">[Tabella componenti](component-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="aaa5d-117">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="aaa5d-118">Componente</span><span class="sxs-lookup"><span data-stu-id="aaa5d-118">Component</span></span> | <span data-ttu-id="aaa5d-119">ComponentId</span><span class="sxs-lookup"><span data-stu-id="aaa5d-119">ComponentId</span></span>                            | <span data-ttu-id="aaa5d-120">Attributi</span><span class="sxs-lookup"><span data-stu-id="aaa5d-120">Attributes</span></span> | <span data-ttu-id="aaa5d-121">KeyPath</span><span class="sxs-lookup"><span data-stu-id="aaa5d-121">KeyPath</span></span> |
|-----------|----------------------------------------|------------|---------|
| <span data-ttu-id="aaa5d-122">Comp1</span><span class="sxs-lookup"><span data-stu-id="aaa5d-122">Comp1</span></span>     | <span data-ttu-id="aaa5d-123">Null</span><span class="sxs-lookup"><span data-stu-id="aaa5d-123">Null</span></span>                                   | <span data-ttu-id="aaa5d-124">0</span><span class="sxs-lookup"><span data-stu-id="aaa5d-124">0</span></span>          | <span data-ttu-id="aaa5d-125">File1</span><span class="sxs-lookup"><span data-stu-id="aaa5d-125">File1</span></span>   |
| <span data-ttu-id="aaa5d-126">Comp2</span><span class="sxs-lookup"><span data-stu-id="aaa5d-126">Comp2</span></span>     | {00000002-0003-0000-0000-624474736554} | <span data-ttu-id="aaa5d-127">0</span><span class="sxs-lookup"><span data-stu-id="aaa5d-127">0</span></span>          | <span data-ttu-id="aaa5d-128">File2</span><span class="sxs-lookup"><span data-stu-id="aaa5d-128">File2</span></span>   |
| <span data-ttu-id="aaa5d-129">COMP3</span><span class="sxs-lookup"><span data-stu-id="aaa5d-129">Comp3</span></span>     | {00000003-0003-0000-0000-624474736554} | <span data-ttu-id="aaa5d-130">4</span><span class="sxs-lookup"><span data-stu-id="aaa5d-130">4</span></span>          | <span data-ttu-id="aaa5d-131">Reg3</span><span class="sxs-lookup"><span data-stu-id="aaa5d-131">Reg3</span></span>    |
| <span data-ttu-id="aaa5d-132">Comp4</span><span class="sxs-lookup"><span data-stu-id="aaa5d-132">Comp4</span></span>     | {00000004-0003-0000-0000-624474736554} | <span data-ttu-id="aaa5d-133">0</span><span class="sxs-lookup"><span data-stu-id="aaa5d-133">0</span></span>          | <span data-ttu-id="aaa5d-134">Null</span><span class="sxs-lookup"><span data-stu-id="aaa5d-134">Null</span></span>    |



 

<span data-ttu-id="aaa5d-135">[Tabella di estensione](extension-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="aaa5d-135">[Extension Table](extension-table.md) (partial)</span></span>



| <span data-ttu-id="aaa5d-136">Estensione</span><span class="sxs-lookup"><span data-stu-id="aaa5d-136">Extension</span></span> | <span data-ttu-id="aaa5d-137">Componente\_</span><span class="sxs-lookup"><span data-stu-id="aaa5d-137">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="aaa5d-138">FLP</span><span class="sxs-lookup"><span data-stu-id="aaa5d-138">flp</span></span>       | <span data-ttu-id="aaa5d-139">Comp1</span><span class="sxs-lookup"><span data-stu-id="aaa5d-139">Comp1</span></span>       |
| <span data-ttu-id="aaa5d-140">TST</span><span class="sxs-lookup"><span data-stu-id="aaa5d-140">tst</span></span>       | <span data-ttu-id="aaa5d-141">Comp2</span><span class="sxs-lookup"><span data-stu-id="aaa5d-141">Comp2</span></span>       |
| <span data-ttu-id="aaa5d-142">exe</span><span class="sxs-lookup"><span data-stu-id="aaa5d-142">exe</span></span>       | <span data-ttu-id="aaa5d-143">Comp4</span><span class="sxs-lookup"><span data-stu-id="aaa5d-143">Comp4</span></span>       |



 

<span data-ttu-id="aaa5d-144">[Tabella collegamenti](shortcut-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="aaa5d-144">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="aaa5d-145">Tasto di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="aaa5d-145">Shortcut</span></span>  | <span data-ttu-id="aaa5d-146">Componente\_</span><span class="sxs-lookup"><span data-stu-id="aaa5d-146">Component\_</span></span> | <span data-ttu-id="aaa5d-147">Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="aaa5d-147">Feature\_</span></span>      |
|-----------|-------------|----------------|
| <span data-ttu-id="aaa5d-148">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="aaa5d-148">Shortcut1</span></span> | <span data-ttu-id="aaa5d-149">Comp4</span><span class="sxs-lookup"><span data-stu-id="aaa5d-149">Comp4</span></span>       | <span data-ttu-id="aaa5d-150">ProductFeature</span><span class="sxs-lookup"><span data-stu-id="aaa5d-150">ProductFeature</span></span> |
| <span data-ttu-id="aaa5d-151">Shortcut2</span><span class="sxs-lookup"><span data-stu-id="aaa5d-151">Shortcut2</span></span> | <span data-ttu-id="aaa5d-152">COMP3</span><span class="sxs-lookup"><span data-stu-id="aaa5d-152">Comp3</span></span>       | <span data-ttu-id="aaa5d-153">ProductFeature</span><span class="sxs-lookup"><span data-stu-id="aaa5d-153">ProductFeature</span></span> |



 

<span data-ttu-id="aaa5d-154">[Tabella delle funzionalità](feature-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="aaa5d-154">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="aaa5d-155">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="aaa5d-155">Feature</span></span>        |
|----------------|
| <span data-ttu-id="aaa5d-156">ProductFeature</span><span class="sxs-lookup"><span data-stu-id="aaa5d-156">ProductFeature</span></span> |



 

> [!Note]  
> <span data-ttu-id="aaa5d-157">Se l'estensione FLP e exe fanno riferimento allo stesso componente, il file EXE o il server COM che li apre deve essere lo stesso.</span><span class="sxs-lookup"><span data-stu-id="aaa5d-157">If the extension flp and exe both reference the same component, the EXE or COM server that opens them must be the same.</span></span> <span data-ttu-id="aaa5d-158">Questo file EXE corrisponde in genere al percorso di un componente.</span><span class="sxs-lookup"><span data-stu-id="aaa5d-158">This EXE is normally the KeyPath for the Component.</span></span> <span data-ttu-id="aaa5d-159">Per OFFICE, le estensioni doc e xls non possono fare riferimento allo stesso componente perché lo stesso file EXE non apre entrambe le estensioni.</span><span class="sxs-lookup"><span data-stu-id="aaa5d-159">For OFFICE, the extensions doc and xls cannot reference the same component because the same EXE does not open both extensions.</span></span> <span data-ttu-id="aaa5d-160">È necessario winword.exe per aprire le estensioni del documento ed è necessario excel.exe per aprire le estensioni xls.</span><span class="sxs-lookup"><span data-stu-id="aaa5d-160">You need winword.exe to open doc extensions and you need excel.exe to open xls extensions.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="aaa5d-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aaa5d-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aaa5d-162">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="aaa5d-162">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



