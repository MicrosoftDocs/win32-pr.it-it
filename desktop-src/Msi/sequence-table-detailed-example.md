---
description: Di seguito è riportato un esempio di una tabella di sequenza.
ms.assetid: 25b3667a-1478-48c4-9c41-4defd25a0103
title: Esempio dettagliato della tabella Sequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4698d5270f2f246fe6e676799ea239e47a950c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318984"
---
# <a name="sequence-table-detailed-example"></a><span data-ttu-id="dc00a-103">Esempio dettagliato della tabella Sequence</span><span class="sxs-lookup"><span data-stu-id="dc00a-103">Sequence Table Detailed Example</span></span>

<span data-ttu-id="dc00a-104">Di seguito è riportato un esempio di una tabella di sequenza.</span><span class="sxs-lookup"><span data-stu-id="dc00a-104">Here is an example of a sequence table.</span></span>



| <span data-ttu-id="dc00a-105">Azione</span><span class="sxs-lookup"><span data-stu-id="dc00a-105">Action</span></span>                                          | <span data-ttu-id="dc00a-106">Condizione</span><span class="sxs-lookup"><span data-stu-id="dc00a-106">Condition</span></span>                                                       | <span data-ttu-id="dc00a-107">Sequenza</span><span class="sxs-lookup"><span data-stu-id="dc00a-107">Sequence</span></span> |
|-------------------------------------------------|-----------------------------------------------------------------|----------|
| [<span data-ttu-id="dc00a-108">LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="dc00a-108">LaunchConditions</span></span>](launchconditions-action.md) |                                                                 |          |
| [<span data-ttu-id="dc00a-109">AppSearch</span><span class="sxs-lookup"><span data-stu-id="dc00a-109">AppSearch</span></span>](appsearch-action.md)               |                                                                 | <span data-ttu-id="dc00a-110">200</span><span class="sxs-lookup"><span data-stu-id="dc00a-110">200</span></span>      |
| [<span data-ttu-id="dc00a-111">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="dc00a-111">CCPSearch</span></span>](ccpsearch-action.md)               | <span data-ttu-id="dc00a-112">\_test CCP</span><span class="sxs-lookup"><span data-stu-id="dc00a-112">CCP\_TEST</span></span>                                                       | <span data-ttu-id="dc00a-113">300</span><span class="sxs-lookup"><span data-stu-id="dc00a-113">300</span></span>      |
| <span data-ttu-id="dc00a-114">CCPDialog</span><span class="sxs-lookup"><span data-stu-id="dc00a-114">CCPDialog</span></span>                                       | <span data-ttu-id="dc00a-115">\_ \_ esito negativo del CCP</span><span class="sxs-lookup"><span data-stu-id="dc00a-115">NOT\_CCP\_SUCCESS</span></span>                                               | <span data-ttu-id="dc00a-116">400</span><span class="sxs-lookup"><span data-stu-id="dc00a-116">400</span></span>      |
| <span data-ttu-id="dc00a-117">MyCustomConfig</span><span class="sxs-lookup"><span data-stu-id="dc00a-117">MyCustomConfig</span></span>                                  | <span data-ttu-id="dc00a-118">NON [ **installato**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="dc00a-118">NOT [**Installed**](installed.md)</span></span>                              | <span data-ttu-id="dc00a-119">500</span><span class="sxs-lookup"><span data-stu-id="dc00a-119">500</span></span>      |
| [<span data-ttu-id="dc00a-120">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="dc00a-120">CostInitialize</span></span>](costinitialize-action.md)     |                                                                 | <span data-ttu-id="dc00a-121">600</span><span class="sxs-lookup"><span data-stu-id="dc00a-121">600</span></span>      |
| [<span data-ttu-id="dc00a-122">Filecost</span><span class="sxs-lookup"><span data-stu-id="dc00a-122">FileCost</span></span>](filecost-action.md)                 |                                                                 | <span data-ttu-id="dc00a-123">700</span><span class="sxs-lookup"><span data-stu-id="dc00a-123">700</span></span>      |
| [<span data-ttu-id="dc00a-124">CostFinalize secondo</span><span class="sxs-lookup"><span data-stu-id="dc00a-124">CostFinalize</span></span>](costfinalize-action.md)         |                                                                 | <span data-ttu-id="dc00a-125">800</span><span class="sxs-lookup"><span data-stu-id="dc00a-125">800</span></span>      |
| <span data-ttu-id="dc00a-126">InstallDialog</span><span class="sxs-lookup"><span data-stu-id="dc00a-126">InstallDialog</span></span>                                   | <span data-ttu-id="dc00a-127">NON [ **installato**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="dc00a-127">NOT [**Installed**](installed.md)</span></span>                              | <span data-ttu-id="dc00a-128">900</span><span class="sxs-lookup"><span data-stu-id="dc00a-128">900</span></span>      |
| <span data-ttu-id="dc00a-129">MaintenanceDialog</span><span class="sxs-lookup"><span data-stu-id="dc00a-129">MaintenanceDialog</span></span>                               | <span data-ttu-id="dc00a-130">[**Installazione**](installed.md) completata E non [ **riprendere**](resume.md)</span><span class="sxs-lookup"><span data-stu-id="dc00a-130">[**Installed**](installed.md) AND NOT [**Resume**](resume.md)</span></span> | <span data-ttu-id="dc00a-131">1000</span><span class="sxs-lookup"><span data-stu-id="dc00a-131">1000</span></span>     |
| <span data-ttu-id="dc00a-132">ActionDialog</span><span class="sxs-lookup"><span data-stu-id="dc00a-132">ActionDialog</span></span>                                    |                                                                 | <span data-ttu-id="dc00a-133">1100</span><span class="sxs-lookup"><span data-stu-id="dc00a-133">1100</span></span>     |
| [<span data-ttu-id="dc00a-134">RegisterProduct</span><span class="sxs-lookup"><span data-stu-id="dc00a-134">RegisterProduct</span></span>](registerproduct-action.md)   |                                                                 | <span data-ttu-id="dc00a-135">1200</span><span class="sxs-lookup"><span data-stu-id="dc00a-135">1200</span></span>     |
| [<span data-ttu-id="dc00a-136">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="dc00a-136">InstallValidate</span></span>](installvalidate-action.md)   |                                                                 | <span data-ttu-id="dc00a-137">1300</span><span class="sxs-lookup"><span data-stu-id="dc00a-137">1300</span></span>     |
| [<span data-ttu-id="dc00a-138">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="dc00a-138">InstallFiles</span></span>](installfiles-action.md)         |                                                                 | <span data-ttu-id="dc00a-139">1400</span><span class="sxs-lookup"><span data-stu-id="dc00a-139">1400</span></span>     |
| <span data-ttu-id="dc00a-140">MyCustomAction</span><span class="sxs-lookup"><span data-stu-id="dc00a-140">MyCustomAction</span></span>                                  | <span data-ttu-id="dc00a-141">$MyComponent > 2</span><span class="sxs-lookup"><span data-stu-id="dc00a-141">$MyComponent > 2</span></span>                                             | <span data-ttu-id="dc00a-142">1500</span><span class="sxs-lookup"><span data-stu-id="dc00a-142">1500</span></span>     |
| [<span data-ttu-id="dc00a-143">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="dc00a-143">InstallFinalize</span></span>](installfinalize-action.md)   |                                                                 | <span data-ttu-id="dc00a-144">1600</span><span class="sxs-lookup"><span data-stu-id="dc00a-144">1600</span></span>     |



 

<span data-ttu-id="dc00a-145">Le azioni seguenti in questa tabella di sequenza sono definite dal programma di installazione e sono esempi di azioni standard:</span><span class="sxs-lookup"><span data-stu-id="dc00a-145">The following actions in this sequence table are defined by the installer and are examples of standard actions:</span></span>

[<span data-ttu-id="dc00a-146">LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="dc00a-146">LaunchConditions</span></span>](launchconditions-action.md)

 

[<span data-ttu-id="dc00a-147">AppSearch</span><span class="sxs-lookup"><span data-stu-id="dc00a-147">AppSearch</span></span>](appsearch-action.md)

 

[<span data-ttu-id="dc00a-148">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="dc00a-148">CCPSearch</span></span>](ccpsearch-action.md)

 

[<span data-ttu-id="dc00a-149">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="dc00a-149">CostInitialize</span></span>](costinitialize-action.md)

 

[<span data-ttu-id="dc00a-150">Filecost</span><span class="sxs-lookup"><span data-stu-id="dc00a-150">FileCost</span></span>](filecost-action.md)

 

[<span data-ttu-id="dc00a-151">CostFinalize secondo</span><span class="sxs-lookup"><span data-stu-id="dc00a-151">CostFinalize</span></span>](costfinalize-action.md)

 

[<span data-ttu-id="dc00a-152">RegisterProduct</span><span class="sxs-lookup"><span data-stu-id="dc00a-152">RegisterProduct</span></span>](registerproduct-action.md)

 

[<span data-ttu-id="dc00a-153">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="dc00a-153">InstallFiles</span></span>](installfiles-action.md)

 

[<span data-ttu-id="dc00a-154">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="dc00a-154">InstallFiles</span></span>](installfiles-action.md)

 

[<span data-ttu-id="dc00a-155">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="dc00a-155">InstallValidate</span></span>](installvalidate-action.md)

<span data-ttu-id="dc00a-156">Le azioni seguenti sono state definite dall'autore della tabella e sono esempi di [azioni personalizzate](custom-actions.md) e devono essere elencate nella [tabella CustomAction](customaction-table.md):</span><span class="sxs-lookup"><span data-stu-id="dc00a-156">The following actions were defined by the table's author and are examples of [custom actions](custom-actions.md) and must be listed in the [CustomAction table](customaction-table.md):</span></span>

<span data-ttu-id="dc00a-157">MyCustomConfig</span><span class="sxs-lookup"><span data-stu-id="dc00a-157">MyCustomConfig</span></span>

 

<span data-ttu-id="dc00a-158">MyCustomAction</span><span class="sxs-lookup"><span data-stu-id="dc00a-158">MyCustomAction</span></span>

<span data-ttu-id="dc00a-159">Le voci rimanenti nel campo azione sono chiavi esterne nella [tabella della finestra di dialogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="dc00a-159">The remaining entries in the Action field are foreign keys into the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="dc00a-160">Specificano i nomi delle finestre di dialogo che verranno visualizzate se il campo condizione restituisce true.</span><span class="sxs-lookup"><span data-stu-id="dc00a-160">They specify the names of dialog boxes that will displayed if the condition field evaluates to True.</span></span>

<span data-ttu-id="dc00a-161">CCPDialog</span><span class="sxs-lookup"><span data-stu-id="dc00a-161">CCPDialog</span></span>

 

<span data-ttu-id="dc00a-162">InstallDialog</span><span class="sxs-lookup"><span data-stu-id="dc00a-162">InstallDialog</span></span>

 

<span data-ttu-id="dc00a-163">MaintenanceDialog</span><span class="sxs-lookup"><span data-stu-id="dc00a-163">MaintenanceDialog</span></span>

 

<span data-ttu-id="dc00a-164">ActionDialog</span><span class="sxs-lookup"><span data-stu-id="dc00a-164">ActionDialog</span></span>

<span data-ttu-id="dc00a-165">La colonna Condition impedisce al programma di installazione di ignorare l'azione se la proprietà o l'espressione in questo campo è false.</span><span class="sxs-lookup"><span data-stu-id="dc00a-165">The Condition column causes the installer to skip the action if the property or expression in this field is False.</span></span> <span data-ttu-id="dc00a-166">La proprietà [**installata**](installed.md) e la proprietà [**Resume**](resume.md) sono esempi di proprietà impostate dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="dc00a-166">The [**Installed**](installed.md) property and the [**RESUME**](resume.md) property are example of properties that are set by the installer.</span></span> <span data-ttu-id="dc00a-167">La proprietà [**installata**](installed.md) è impostata su true se il prodotto è già installato e la proprietà [**Resume**](resume.md) viene impostata in caso di ripresa di un'installazione sospesa.</span><span class="sxs-lookup"><span data-stu-id="dc00a-167">The [**Installed**](installed.md) property is set to true if the product is already installed and the [**RESUME**](resume.md) property is set if resuming a suspended installation.</span></span> <span data-ttu-id="dc00a-168">Il \_ test CCP e le \_ proprietà non \_ riuscite CCP sono esempi di proprietà che possono essere impostate dalla riga di comando dall'utente che installa l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dc00a-168">The CCP\_TEST and the NOT\_CCP\_SUCCESS properties are examples of properties that can be set at the command line by the user installing the application.</span></span>

<span data-ttu-id="dc00a-169">Tutte le azioni vengono eseguite in sequenza con i passaggi condizionali seguenti:</span><span class="sxs-lookup"><span data-stu-id="dc00a-169">All actions run in sequence with the following conditional steps:</span></span>

-   <span data-ttu-id="dc00a-170">CPPSearch viene eseguito solo se \_ è impostato il test CCP.</span><span class="sxs-lookup"><span data-stu-id="dc00a-170">The CPPSearch is run only if CCP\_TEST is set.</span></span>
-   <span data-ttu-id="dc00a-171">CCPDialog viene eseguito solo se non \_ \_ è stata impostata la funzione CCP riuscita.</span><span class="sxs-lookup"><span data-stu-id="dc00a-171">CCPDialog is run only if NOT\_CCP\_SUCCESS is set.</span></span>
-   <span data-ttu-id="dc00a-172">MaintenanceDialog viene eseguito solo se questo prodotto è già installato e se non si tratta di un'installazione che verrà ripresa dopo essere stata sospesa.</span><span class="sxs-lookup"><span data-stu-id="dc00a-172">MaintenanceDialog is run only if this product is already installed and if this is not an installation that is being resume after being suspended.</span></span>
-   <span data-ttu-id="dc00a-173">MyCustomAction viene eseguito solo se l'espressione nella colonna condizione è true.</span><span class="sxs-lookup"><span data-stu-id="dc00a-173">MyCustomAction is run only if the expression in the Condition column is True.</span></span> <span data-ttu-id="dc00a-174">L'espressione $MyComponent > 2 fa riferimento allo stato dell'azione del componente denominato "componente".</span><span class="sxs-lookup"><span data-stu-id="dc00a-174">The expression $MyComponent > 2 refers to the action state of the component called MyComponent.</span></span> <span data-ttu-id="dc00a-175">Questa condizione indica che MyCustomAction deve essere eseguito solo se il componente è impostato per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="dc00a-175">This condition indicates that MyCustomAction should only be run if MyComponent is set to be installed.</span></span> <span data-ttu-id="dc00a-176">Per altre informazioni sugli Stati delle azioni e sugli stati di selezione, vedere la proprietà [**FeatureRequestState**](session-featurerequeststate.md) , la [tabella delle funzionalità](feature-table.md)e l' [azione InstallFiles](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="dc00a-176">For more information on Action states and Selection states, see the [**FeatureRequestState**](session-featurerequeststate.md) property, the [Feature table](feature-table.md), and the [InstallFiles action](installfiles-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc00a-177">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dc00a-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc00a-178">Utilizzo delle proprietà</span><span class="sxs-lookup"><span data-stu-id="dc00a-178">Using Properties</span></span>](using-properties.md)
</dt> <dt>

[<span data-ttu-id="dc00a-179">Sintassi dell'istruzione condizionale</span><span class="sxs-lookup"><span data-stu-id="dc00a-179">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> </dl>

 

 



