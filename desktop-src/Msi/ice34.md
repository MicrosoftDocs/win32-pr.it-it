---
description: ICE34 verifica che ogni pulsante di opzione in ogni controllo RadioButtonGroup disponga di una proprietà nella colonna proprietà della tabella RadioButton che specifica il gruppo di pulsanti di opzione.
ms.assetid: 23a88a5a-89e9-47bc-9c0a-6101ce03123c
title: ICE34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7723cb530397eae66374b0f218db9ad8505195a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314220"
---
# <a name="ice34"></a><span data-ttu-id="b25b1-103">ICE34</span><span class="sxs-lookup"><span data-stu-id="b25b1-103">ICE34</span></span>

<span data-ttu-id="b25b1-104">ICE34 verifica che ogni pulsante di opzione in ogni [controllo RadioButtonGroup](radiobuttongroup-control.md) disponga di una proprietà nella colonna proprietà della [tabella RadioButton](radiobutton-table.md) che specifica il gruppo di pulsanti di opzione.</span><span class="sxs-lookup"><span data-stu-id="b25b1-104">ICE34 validates that each radio button on every [RadioButtonGroup Control](radiobuttongroup-control.md) has a property in the Property column of the [RadioButton table](radiobutton-table.md) that specifies its radio button group.</span></span> <span data-ttu-id="b25b1-105">ICE34 verifica che questa proprietà esista e che sia impostata su un valore predefinito nella [tabella delle proprietà](property-table.md) , che è uguale a uno dei valori dei pulsanti di opzione del gruppo nella colonna valore della tabella RadioButton.</span><span class="sxs-lookup"><span data-stu-id="b25b1-105">ICE34 validates that this property exists and is set to a default value in the [Property table](property-table.md) which is equal to one of the group's radio button values in the Value column of the RadioButton table.</span></span>

<span data-ttu-id="b25b1-106">Un gruppo di pulsanti di opzione deve avere un valore predefinito per consentire agli utenti di selezionare una scelta usando il tasto TAB.</span><span class="sxs-lookup"><span data-stu-id="b25b1-106">A radio button group must have a default for users to be able to select a choice using the TAB key.</span></span> <span data-ttu-id="b25b1-107">Questa operazione è necessaria per l'accessibilità utente corretta.</span><span class="sxs-lookup"><span data-stu-id="b25b1-107">This is required for proper user accessibility.</span></span>

<span data-ttu-id="b25b1-108">ICE34 segnala le tabelle mancanti.</span><span class="sxs-lookup"><span data-stu-id="b25b1-108">ICE34 reports missing tables.</span></span>

## <a name="result"></a><span data-ttu-id="b25b1-109">Risultato</span><span class="sxs-lookup"><span data-stu-id="b25b1-109">Result</span></span>

<span data-ttu-id="b25b1-110">ICE34 pubblica un messaggio di errore se è presente un pulsante di opzione che specifica una proprietà non valida.</span><span class="sxs-lookup"><span data-stu-id="b25b1-110">ICE34 post an error message if there is a radio button that specifies an invalid property.</span></span>

## <a name="example"></a><span data-ttu-id="b25b1-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="b25b1-111">Example</span></span>

<span data-ttu-id="b25b1-112">ICE34 segnala gli errori seguenti per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="b25b1-112">ICE34 reports the following errors for the example shown.</span></span>



| <span data-ttu-id="b25b1-113">Errore ICE34</span><span class="sxs-lookup"><span data-stu-id="b25b1-113">ICE34 error</span></span>                                                                                                                                                                | <span data-ttu-id="b25b1-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b25b1-114">Description</span></span>                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b25b1-115">Il controllo dialoga. Controllo2 deve avere una proprietà perché è di tipo RadioButtonGroup.</span><span class="sxs-lookup"><span data-stu-id="b25b1-115">Control DialogA.Control2 must have a property because it is of type RadioButtonGroup.</span></span>                                                                                      | <span data-ttu-id="b25b1-116">È presente un [controllo RadioButtonGroup](radiobuttongroup-control.md), senza il bit del [controllo indiretto](indirect-control-attribute.md) impostato nella colonna attributi della [tabella dei controlli](control-table.md), che non dispone di una proprietà elencata nella colonna proprietà.</span><span class="sxs-lookup"><span data-stu-id="b25b1-116">There is a [RadioButtonGroup control](radiobuttongroup-control.md), without the [Indirect control](indirect-control-attribute.md) bit set in the Attributes column of the [Control table](control-table.md), that does not have a property listed in the Property column.</span></span> |
| <span data-ttu-id="b25b1-117">Probabilmente non è un valore predefinito valido per RadioButtonGroup usando la proprietà Property3.</span><span class="sxs-lookup"><span data-stu-id="b25b1-117">Maybe is not a valid default value for the RadioButtonGroup using property Property3.</span></span> <span data-ttu-id="b25b1-118">Il valore deve essere elencato come opzione nella tabella RadioButtonGroup.</span><span class="sxs-lookup"><span data-stu-id="b25b1-118">The value must be listed as an option in the RadioButtonGroup table.</span></span>                 | <span data-ttu-id="b25b1-119">È presente un valore predefinito per una proprietà specificata nella colonna valore della tabella delle [Proprietà](property-table.md) che non è uno dei valori per il gruppo di pulsanti di opzione specificato nella colonna valore della [tabella RadioButton](radiobutton-table.md).</span><span class="sxs-lookup"><span data-stu-id="b25b1-119">There is a default value for a property specified in the Value column of the [Property table](property-table.md) that is not one of the values for the radio button group specified in the Value column of the [RadioButton table](radiobutton-table.md).</span></span>                  |
| <span data-ttu-id="b25b1-120">È necessario definire la proprietà PropertyB perché si tratta di una proprietà indiretta di un controllo RadioButtonGroup dialoga. Control4</span><span class="sxs-lookup"><span data-stu-id="b25b1-120">Property PropertyB must be defined because it is an indirect property of a RadioButtonGroup control DialogA.Control4</span></span>                                                       | <span data-ttu-id="b25b1-121">La proprietà a cui fa riferimento questo gruppo RadioButton è una proprietà indiretta e il valore della proprietà indiretta non è una delle scelte per il gruppo RadioButton.</span><span class="sxs-lookup"><span data-stu-id="b25b1-121">The property referenced by this RadioButton group is an indirect property, and the value of the indirect property is not one of the choices for the RadioButton group.</span></span>                                                                                                       |
| <span data-ttu-id="b25b1-122">Probabilmente non è un valore predefinito valido per la proprietà PropertyA.</span><span class="sxs-lookup"><span data-stu-id="b25b1-122">Maybe is not a valid default value for the property PropertyA.</span></span> <span data-ttu-id="b25b1-123">La proprietà è una proprietà RadioButtonGroup indiretta del controllo dialoga. Control5 (tramite la proprietà property5).</span><span class="sxs-lookup"><span data-stu-id="b25b1-123">The property is an indirect RadioButtonGroup property of control DialogA.Control5 (via property Property5).</span></span> | <span data-ttu-id="b25b1-124">Il valore della proprietà indiretta a cui viene fatto riferimento tramite il controllo non è uno dei valori predefiniti per tale RadioButtonGroup.</span><span class="sxs-lookup"><span data-stu-id="b25b1-124">The value of the indirect property referenced via the control is not one of the default values for that RadioButtonGroup.</span></span>                                                                                                                                                    |



 

<span data-ttu-id="b25b1-125">[Tabella di controllo](control-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="b25b1-125">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="b25b1-126">Finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="b25b1-126">Dialog</span></span>  | <span data-ttu-id="b25b1-127">Control</span><span class="sxs-lookup"><span data-stu-id="b25b1-127">Control</span></span>  | <span data-ttu-id="b25b1-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="b25b1-128">Type</span></span>             | <span data-ttu-id="b25b1-129">Attributi</span><span class="sxs-lookup"><span data-stu-id="b25b1-129">Attributes</span></span> | <span data-ttu-id="b25b1-130">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b25b1-130">Property</span></span>  |
|---------|----------|------------------|------------|-----------|
| <span data-ttu-id="b25b1-131">Finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="b25b1-131">DialogA</span></span> | <span data-ttu-id="b25b1-132">Control1</span><span class="sxs-lookup"><span data-stu-id="b25b1-132">Control1</span></span> | <span data-ttu-id="b25b1-133">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="b25b1-133">RadioButtonGroup</span></span> | <span data-ttu-id="b25b1-134">0</span><span class="sxs-lookup"><span data-stu-id="b25b1-134">0</span></span>          | <span data-ttu-id="b25b1-135">Property1</span><span class="sxs-lookup"><span data-stu-id="b25b1-135">Property1</span></span> |
| <span data-ttu-id="b25b1-136">Finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="b25b1-136">DialogA</span></span> | <span data-ttu-id="b25b1-137">Controllo2</span><span class="sxs-lookup"><span data-stu-id="b25b1-137">Control2</span></span> | <span data-ttu-id="b25b1-138">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="b25b1-138">RadioButtonGroup</span></span> | <span data-ttu-id="b25b1-139">0</span><span class="sxs-lookup"><span data-stu-id="b25b1-139">0</span></span>          |           |
| <span data-ttu-id="b25b1-140">Finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="b25b1-140">DialogA</span></span> | <span data-ttu-id="b25b1-141">Control3</span><span class="sxs-lookup"><span data-stu-id="b25b1-141">Control3</span></span> | <span data-ttu-id="b25b1-142">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="b25b1-142">RadioButtonGroup</span></span> | <span data-ttu-id="b25b1-143">0</span><span class="sxs-lookup"><span data-stu-id="b25b1-143">0</span></span>          | <span data-ttu-id="b25b1-144">Property3</span><span class="sxs-lookup"><span data-stu-id="b25b1-144">Property3</span></span> |
| <span data-ttu-id="b25b1-145">Finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="b25b1-145">DialogA</span></span> | <span data-ttu-id="b25b1-146">Control4</span><span class="sxs-lookup"><span data-stu-id="b25b1-146">Control4</span></span> | <span data-ttu-id="b25b1-147">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="b25b1-147">RadioButtonGroup</span></span> | <span data-ttu-id="b25b1-148">8</span><span class="sxs-lookup"><span data-stu-id="b25b1-148">8</span></span>          | <span data-ttu-id="b25b1-149">Property4</span><span class="sxs-lookup"><span data-stu-id="b25b1-149">Property4</span></span> |
| <span data-ttu-id="b25b1-150">Finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="b25b1-150">DialogA</span></span> | <span data-ttu-id="b25b1-151">Control5</span><span class="sxs-lookup"><span data-stu-id="b25b1-151">Control5</span></span> | <span data-ttu-id="b25b1-152">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="b25b1-152">RadioButtonGroup</span></span> | <span data-ttu-id="b25b1-153">8</span><span class="sxs-lookup"><span data-stu-id="b25b1-153">8</span></span>          | <span data-ttu-id="b25b1-154">Property5</span><span class="sxs-lookup"><span data-stu-id="b25b1-154">Property5</span></span> |



 

<span data-ttu-id="b25b1-155">[Tabella delle proprietà](property-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="b25b1-155">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="b25b1-156">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b25b1-156">Property</span></span>  | <span data-ttu-id="b25b1-157">Valore</span><span class="sxs-lookup"><span data-stu-id="b25b1-157">Value</span></span>     |
|-----------|-----------|
| <span data-ttu-id="b25b1-158">Property1</span><span class="sxs-lookup"><span data-stu-id="b25b1-158">Property1</span></span> | <span data-ttu-id="b25b1-159">Sì</span><span class="sxs-lookup"><span data-stu-id="b25b1-159">Yes</span></span>       |
| <span data-ttu-id="b25b1-160">Property3</span><span class="sxs-lookup"><span data-stu-id="b25b1-160">Property3</span></span> | <span data-ttu-id="b25b1-161">È possibile</span><span class="sxs-lookup"><span data-stu-id="b25b1-161">Maybe</span></span>     |
| <span data-ttu-id="b25b1-162">Property4</span><span class="sxs-lookup"><span data-stu-id="b25b1-162">Property4</span></span> | <span data-ttu-id="b25b1-163">PropertyB</span><span class="sxs-lookup"><span data-stu-id="b25b1-163">PropertyB</span></span> |
| <span data-ttu-id="b25b1-164">Property5</span><span class="sxs-lookup"><span data-stu-id="b25b1-164">Property5</span></span> | <span data-ttu-id="b25b1-165">PropertyA</span><span class="sxs-lookup"><span data-stu-id="b25b1-165">PropertyA</span></span> |
| <span data-ttu-id="b25b1-166">PropertyA</span><span class="sxs-lookup"><span data-stu-id="b25b1-166">PropertyA</span></span> | <span data-ttu-id="b25b1-167">È possibile</span><span class="sxs-lookup"><span data-stu-id="b25b1-167">Maybe</span></span>     |



 

<span data-ttu-id="b25b1-168">[Tabella RadioButton](radiobutton-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="b25b1-168">[RadioButton Table](radiobutton-table.md) (partial)</span></span>



| <span data-ttu-id="b25b1-169">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b25b1-169">Property</span></span>  | <span data-ttu-id="b25b1-170">JSON</span><span class="sxs-lookup"><span data-stu-id="b25b1-170">Order</span></span> | <span data-ttu-id="b25b1-171">Valore</span><span class="sxs-lookup"><span data-stu-id="b25b1-171">Value</span></span> |
|-----------|-------|-------|
| <span data-ttu-id="b25b1-172">Property1</span><span class="sxs-lookup"><span data-stu-id="b25b1-172">Property1</span></span> | <span data-ttu-id="b25b1-173">1</span><span class="sxs-lookup"><span data-stu-id="b25b1-173">1</span></span>     | <span data-ttu-id="b25b1-174">Sì</span><span class="sxs-lookup"><span data-stu-id="b25b1-174">Yes</span></span>   |
| <span data-ttu-id="b25b1-175">Property1</span><span class="sxs-lookup"><span data-stu-id="b25b1-175">Property1</span></span> | <span data-ttu-id="b25b1-176">2</span><span class="sxs-lookup"><span data-stu-id="b25b1-176">2</span></span>     | <span data-ttu-id="b25b1-177">Adesso</span><span class="sxs-lookup"><span data-stu-id="b25b1-177">Now</span></span>   |
| <span data-ttu-id="b25b1-178">Property2</span><span class="sxs-lookup"><span data-stu-id="b25b1-178">Property2</span></span> | <span data-ttu-id="b25b1-179">1</span><span class="sxs-lookup"><span data-stu-id="b25b1-179">1</span></span>     | <span data-ttu-id="b25b1-180">Sì</span><span class="sxs-lookup"><span data-stu-id="b25b1-180">Yes</span></span>   |
| <span data-ttu-id="b25b1-181">Property2</span><span class="sxs-lookup"><span data-stu-id="b25b1-181">Property2</span></span> | <span data-ttu-id="b25b1-182">2</span><span class="sxs-lookup"><span data-stu-id="b25b1-182">2</span></span>     | <span data-ttu-id="b25b1-183">No</span><span class="sxs-lookup"><span data-stu-id="b25b1-183">No</span></span>    |
| <span data-ttu-id="b25b1-184">Property3</span><span class="sxs-lookup"><span data-stu-id="b25b1-184">Property3</span></span> | <span data-ttu-id="b25b1-185">1</span><span class="sxs-lookup"><span data-stu-id="b25b1-185">1</span></span>     | <span data-ttu-id="b25b1-186">Sì</span><span class="sxs-lookup"><span data-stu-id="b25b1-186">Yes</span></span>   |
| <span data-ttu-id="b25b1-187">Property3</span><span class="sxs-lookup"><span data-stu-id="b25b1-187">Property3</span></span> | <span data-ttu-id="b25b1-188">2</span><span class="sxs-lookup"><span data-stu-id="b25b1-188">2</span></span>     | <span data-ttu-id="b25b1-189">No</span><span class="sxs-lookup"><span data-stu-id="b25b1-189">No</span></span>    |
| <span data-ttu-id="b25b1-190">Property4</span><span class="sxs-lookup"><span data-stu-id="b25b1-190">Property4</span></span> | <span data-ttu-id="b25b1-191">1</span><span class="sxs-lookup"><span data-stu-id="b25b1-191">1</span></span>     | <span data-ttu-id="b25b1-192">Sì</span><span class="sxs-lookup"><span data-stu-id="b25b1-192">Yes</span></span>   |
| <span data-ttu-id="b25b1-193">Property4</span><span class="sxs-lookup"><span data-stu-id="b25b1-193">Property4</span></span> | <span data-ttu-id="b25b1-194">2</span><span class="sxs-lookup"><span data-stu-id="b25b1-194">2</span></span>     | <span data-ttu-id="b25b1-195">No</span><span class="sxs-lookup"><span data-stu-id="b25b1-195">No</span></span>    |
| <span data-ttu-id="b25b1-196">PropertyA</span><span class="sxs-lookup"><span data-stu-id="b25b1-196">PropertyA</span></span> | <span data-ttu-id="b25b1-197">1</span><span class="sxs-lookup"><span data-stu-id="b25b1-197">1</span></span>     | <span data-ttu-id="b25b1-198">Sì</span><span class="sxs-lookup"><span data-stu-id="b25b1-198">Yes</span></span>   |
| <span data-ttu-id="b25b1-199">PropertyA</span><span class="sxs-lookup"><span data-stu-id="b25b1-199">PropertyA</span></span> | <span data-ttu-id="b25b1-200">2</span><span class="sxs-lookup"><span data-stu-id="b25b1-200">2</span></span>     | <span data-ttu-id="b25b1-201">No</span><span class="sxs-lookup"><span data-stu-id="b25b1-201">No</span></span>    |
| <span data-ttu-id="b25b1-202">PropertyB</span><span class="sxs-lookup"><span data-stu-id="b25b1-202">PropertyB</span></span> | <span data-ttu-id="b25b1-203">1</span><span class="sxs-lookup"><span data-stu-id="b25b1-203">1</span></span>     | <span data-ttu-id="b25b1-204">Sì</span><span class="sxs-lookup"><span data-stu-id="b25b1-204">Yes</span></span>   |
| <span data-ttu-id="b25b1-205">PropertyB</span><span class="sxs-lookup"><span data-stu-id="b25b1-205">PropertyB</span></span> | <span data-ttu-id="b25b1-206">2</span><span class="sxs-lookup"><span data-stu-id="b25b1-206">2</span></span>     | <span data-ttu-id="b25b1-207">No</span><span class="sxs-lookup"><span data-stu-id="b25b1-207">No</span></span>    |



 

<span data-ttu-id="b25b1-208">Per correggere gli errori segnalati da questo ICE, controllare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="b25b1-208">To fix the errors reported by this ICE, check the following:</span></span>

-   <span data-ttu-id="b25b1-209">Che ogni voce di controllo RadioButton senza il set di attributi indiretto disponga di una proprietà elencata nella colonna proprietà:</span><span class="sxs-lookup"><span data-stu-id="b25b1-209">That every RadioButton control entry without the indirect attribute set has a property listed in the Property column:</span></span>
-   <span data-ttu-id="b25b1-210">Ogni proprietà di questo tipo contiene almeno una voce corrispondente nella tabella RadioButton.</span><span class="sxs-lookup"><span data-stu-id="b25b1-210">That every such property has at least one corresponding entry in the RadioButton table.</span></span>
-   <span data-ttu-id="b25b1-211">Ogni proprietà di questo tipo è definita nella tabella delle proprietà, con un valore che corrisponde a una delle scelte della tabella RadioButton.</span><span class="sxs-lookup"><span data-stu-id="b25b1-211">That every such property is defined in the Property table, with a value that is one of the choices from the RadioButton table.</span></span>
-   <span data-ttu-id="b25b1-212">Ogni proprietà a cui viene fatto riferimento nella colonna delle proprietà di un controllo RadioButton con il set di attributi indiretto viene definita nella tabella delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="b25b1-212">That every property referenced in the Property column of a RadioButton control with the indirect attribute set is defined in the Property table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b25b1-213">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b25b1-213">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b25b1-214">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="b25b1-214">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



