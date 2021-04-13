---
title: Group - elemento
description: Rappresenta un controllo gruppo che funge da contenitore per un gruppo di elementi.
ms.assetid: b0d3fcda-7165-40f4-9e57-c7ab88b31711
keywords:
- Barra multifunzione Windows elemento gruppo
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a42e9efb30397862037426041420d96be8fd387
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399350"
---
# <a name="group-element"></a><span data-ttu-id="6dc7b-104">Group - elemento</span><span class="sxs-lookup"><span data-stu-id="6dc7b-104">Group element</span></span>

<span data-ttu-id="6dc7b-105">Rappresenta un controllo [gruppo](windowsribbon-controls-group.md) che funge da contenitore per un gruppo di elementi.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-105">Represents a [Group](windowsribbon-controls-group.md) control that functions as a container for a group of elements.</span></span>

## <a name="usage"></a><span data-ttu-id="6dc7b-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="6dc7b-106">Usage</span></span>

``` syntax
<Group
  SizeDefinition = "xs:string"
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Group>
```

## <a name="attributes"></a><span data-ttu-id="6dc7b-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="6dc7b-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc7b-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="6dc7b-108">Attribute</span></span></th>
<th><span data-ttu-id="6dc7b-109">Type</span><span class="sxs-lookup"><span data-stu-id="6dc7b-109">Type</span></span></th>
<th><span data-ttu-id="6dc7b-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="6dc7b-110">Required</span></span></th>
<th><span data-ttu-id="6dc7b-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6dc7b-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dc7b-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="6dc7b-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="6dc7b-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="6dc7b-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="6dc7b-114">No</span><span class="sxs-lookup"><span data-stu-id="6dc7b-114">No</span></span><br/></td>
<td><span data-ttu-id="6dc7b-115"><dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="6dc7b-115"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="6dc7b-116">Stringa che contiene un elenco delimitato da virgole di numeri interi compresi tra 0 e 31.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-116">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="6dc7b-117">Gli spazi vuoti sono validi e vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-117">White space is valid and ignored.</span></span><br/> <span data-ttu-id="6dc7b-118">Lunghezza massima: 250 caratteri.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-118">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dc7b-119"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="6dc7b-119"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="6dc7b-120">XS: positiveInteger o xs: String</span><span class="sxs-lookup"><span data-stu-id="6dc7b-120">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="6dc7b-121">No</span><span class="sxs-lookup"><span data-stu-id="6dc7b-121">No</span></span><br/></td>
<td><span data-ttu-id="6dc7b-122">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-122">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="6dc7b-123">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o xs: String)</span><span class="sxs-lookup"><span data-stu-id="6dc7b-123">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="6dc7b-124">Stringa, valore intero compreso tra 2 e 59999, inclusivo o un valore esadecimale compreso tra 0x2 e 0xea5f, inclusi.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-124">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="6dc7b-125">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-125">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="6dc7b-126">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-126">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6dc7b-127"><strong>SizeDefinition</strong></span><span class="sxs-lookup"><span data-stu-id="6dc7b-127"><strong>SizeDefinition</strong></span></span><br/></td>
<td><span data-ttu-id="6dc7b-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="6dc7b-128">xs:string</span></span><br/></td>
<td><span data-ttu-id="6dc7b-129">No</span><span class="sxs-lookup"><span data-stu-id="6dc7b-129">No</span></span><br/></td>
<td><span data-ttu-id="6dc7b-130">Quando specificato, il valore di <em>SizeDefinition</em> è vincolato a uno dei modelli di <a href="windowsribbon-templates.md">layout</a> definiti dal framework della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-130">When specified, the value of <em>SizeDefinition</em> is constrained to one of the <a href="windowsribbon-templates.md">layout templates</a> defined by the Ribbon framework.</span></span> <br/> <br/><span data-ttu-id="6dc7b-131">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="6dc7b-131">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="6dc7b-132">Qualsiasi sequenza di zero o più caratteri.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-132">Any sequence of zero or more characters.</span></span><br/> <span data-ttu-id="6dc7b-133">La lunghezza massima è unbounded.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-133">The maximum length is unbounded.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="6dc7b-134">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="6dc7b-134">Child elements</span></span>



| <span data-ttu-id="6dc7b-135">Elemento</span><span class="sxs-lookup"><span data-stu-id="6dc7b-135">Element</span></span>                                                                             | <span data-ttu-id="6dc7b-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6dc7b-136">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="6dc7b-137">**Button**</span><span class="sxs-lookup"><span data-stu-id="6dc7b-137">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="6dc7b-138">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="6dc7b-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="6dc7b-139">**Casella**</span><span class="sxs-lookup"><span data-stu-id="6dc7b-139">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="6dc7b-140">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="6dc7b-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="6dc7b-141">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="6dc7b-141">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="6dc7b-142">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="6dc7b-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="6dc7b-143">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="6dc7b-143">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>               | <span data-ttu-id="6dc7b-144">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="6dc7b-144">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="6dc7b-145">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="6dc7b-145">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>           | <span data-ttu-id="6dc7b-146">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="6dc7b-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="6dc7b-147">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="6dc7b-147">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="6dc7b-148">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="6dc7b-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="6dc7b-149">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="6dc7b-149">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="6dc7b-150">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="6dc7b-150">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="6dc7b-151">**FontControl**</span><span class="sxs-lookup"><span data-stu-id="6dc7b-151">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                 | <span data-ttu-id="6dc7b-152">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="6dc7b-152">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="6dc7b-153">**Inribbongallery**</span><span class="sxs-lookup"><span data-stu-id="6dc7b-153">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/>         | <span data-ttu-id="6dc7b-154">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="6dc7b-154">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="6dc7b-155">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="6dc7b-155">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/>           | <span data-ttu-id="6dc7b-156">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="6dc7b-156">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="6dc7b-157">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="6dc7b-157">**Spinner**</span></span>](windowsribbon-element-spinner.md)<br/>                         | <span data-ttu-id="6dc7b-158">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="6dc7b-158">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="6dc7b-159">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="6dc7b-159">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="6dc7b-160">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="6dc7b-160">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="6dc7b-161">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="6dc7b-161">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="6dc7b-162">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="6dc7b-162">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="6dc7b-163">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="6dc7b-163">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="6dc7b-164">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="6dc7b-164">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="6dc7b-165">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="6dc7b-165">Parent elements</span></span>



| <span data-ttu-id="6dc7b-166">Elemento</span><span class="sxs-lookup"><span data-stu-id="6dc7b-166">Element</span></span>                                             |
|-----------------------------------------------------|
| [<span data-ttu-id="6dc7b-167">**Scheda**</span><span class="sxs-lookup"><span data-stu-id="6dc7b-167">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="6dc7b-168">Commenti</span><span class="sxs-lookup"><span data-stu-id="6dc7b-168">Remarks</span></span>

<span data-ttu-id="6dc7b-169">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-169">Optional.</span></span>

<span data-ttu-id="6dc7b-170">Può essere presente una o più volte per ogni elemento di [**tabulazione**](windowsribbon-element-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="6dc7b-170">May occur one or more times for each [**Tab**](windowsribbon-element-tab.md) element.</span></span>

<span data-ttu-id="6dc7b-171">[**Tab**](windowsribbon-element-tab.md) supporta le [modalità di applicazione](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="6dc7b-171">[**Tab**](windowsribbon-element-tab.md) supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="6dc7b-172">Il markup della barra multifunzione è valido solo quando gli elementi figlio del **gruppo** corrispondono al modello specificato per *SizeDefinition*.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-172">The Ribbon markup is valid only when the child elements of **Group** correspond to the template specified for *SizeDefinition*.</span></span>

## <a name="examples"></a><span data-ttu-id="6dc7b-173">Esempio</span><span class="sxs-lookup"><span data-stu-id="6dc7b-173">Examples</span></span>

<span data-ttu-id="6dc7b-174">Nell'esempio di codice riportato di seguito viene illustrato l'utilizzo di un modello personalizzato in un **gruppo**.</span><span class="sxs-lookup"><span data-stu-id="6dc7b-174">The following code example illustrates the use of a custom template in a **Group**.</span></span>


```
<Group CommandName="cmdCustomGroup1" SizeDefinition="CustomTemplate">
  <Button CommandName="cmdCommand1" />
</Group>
```



## <a name="element-information"></a><span data-ttu-id="6dc7b-175">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="6dc7b-175">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="6dc7b-176">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6dc7b-176">Minimum supported system</span></span><br/> | <span data-ttu-id="6dc7b-177">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6dc7b-177">Windows 7</span></span> |
| <span data-ttu-id="6dc7b-178">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="6dc7b-178">Can be empty</span></span>                        | <span data-ttu-id="6dc7b-179">No</span><span class="sxs-lookup"><span data-stu-id="6dc7b-179">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="6dc7b-180">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="6dc7b-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dc7b-181">Personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità</span><span class="sxs-lookup"><span data-stu-id="6dc7b-181">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> <dt>

[<span data-ttu-id="6dc7b-182">Controllo gruppo</span><span class="sxs-lookup"><span data-stu-id="6dc7b-182">Group control</span></span>](windowsribbon-controls-group.md)
</dt> <dt>

[<span data-ttu-id="6dc7b-183">**Modalità selettore**</span><span class="sxs-lookup"><span data-stu-id="6dc7b-183">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

