---
title: Group - elemento
description: Rappresenta un controllo Group che funziona come contenitore per un gruppo di elementi.
ms.assetid: b0d3fcda-7165-40f4-9e57-c7ab88b31711
keywords:
- Elemento Group della barra multifunzione di Windows
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1162055491f61ae6feffa385bbc5015e4f1b66f0
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442872"
---
# <a name="group-element"></a><span data-ttu-id="f6330-104">Group - elemento</span><span class="sxs-lookup"><span data-stu-id="f6330-104">Group element</span></span>

<span data-ttu-id="f6330-105">Rappresenta un [controllo Group](windowsribbon-controls-group.md) che funziona come contenitore per un gruppo di elementi.</span><span class="sxs-lookup"><span data-stu-id="f6330-105">Represents a [Group](windowsribbon-controls-group.md) control that functions as a container for a group of elements.</span></span>

## <a name="usage"></a><span data-ttu-id="f6330-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="f6330-106">Usage</span></span>

``` syntax
<Group
  SizeDefinition = "xs:string"
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Group>
```

## <a name="attributes"></a><span data-ttu-id="f6330-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="f6330-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f6330-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="f6330-108">Attribute</span></span></th>
<th><span data-ttu-id="f6330-109">Type</span><span class="sxs-lookup"><span data-stu-id="f6330-109">Type</span></span></th>
<th><span data-ttu-id="f6330-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f6330-110">Required</span></span></th>
<th><span data-ttu-id="f6330-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6330-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f6330-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="f6330-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="f6330-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="f6330-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="f6330-114">No</span><span class="sxs-lookup"><span data-stu-id="f6330-114">No</span></span><br/></td>
<td><span data-ttu-id="f6330-115"><dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="f6330-115"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="f6330-116">Stringa che contiene un elenco delimitato da virgole di numeri interi compresi tra 0 e 31.</span><span class="sxs-lookup"><span data-stu-id="f6330-116">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="f6330-117">Gli spazi vuoti sono validi e ignorati.</span><span class="sxs-lookup"><span data-stu-id="f6330-117">White space is valid and ignored.</span></span><br/> <span data-ttu-id="f6330-118">Lunghezza massima: 250 caratteri.</span><span class="sxs-lookup"><span data-stu-id="f6330-118">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f6330-119"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="f6330-119"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="f6330-120">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="f6330-120">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="f6330-121">No</span><span class="sxs-lookup"><span data-stu-id="f6330-121">No</span></span><br/></td>
<td><span data-ttu-id="f6330-122">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command.</strong></a></span><span class="sxs-lookup"><span data-stu-id="f6330-122">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="f6330-123">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="f6330-123">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="f6330-124">Stringa, valore intero compreso tra 2 e 59999 inclusi o valore esadecimale compreso tra 0x2 e 0xea5f inclusi.</span><span class="sxs-lookup"><span data-stu-id="f6330-124">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="f6330-125">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="f6330-125">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="f6330-126">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="f6330-126">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f6330-127"><strong>SizeDefinition</strong></span><span class="sxs-lookup"><span data-stu-id="f6330-127"><strong>SizeDefinition</strong></span></span><br/></td>
<td><span data-ttu-id="f6330-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="f6330-128">xs:string</span></span><br/></td>
<td><span data-ttu-id="f6330-129">No</span><span class="sxs-lookup"><span data-stu-id="f6330-129">No</span></span><br/></td>
<td><span data-ttu-id="f6330-130">Se specificato, il valore di <em>SizeDefinition</em> è vincolato a uno dei modelli <a href="windowsribbon-templates.md">di layout</a> definiti dal framework della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="f6330-130">When specified, the value of <em>SizeDefinition</em> is constrained to one of the <a href="windowsribbon-templates.md">layout templates</a> defined by the Ribbon framework.</span></span> <br/> <br/><span data-ttu-id="f6330-131">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="f6330-131">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="f6330-132">Qualsiasi sequenza di zero o più caratteri.</span><span class="sxs-lookup"><span data-stu-id="f6330-132">Any sequence of zero or more characters.</span></span><br/> <span data-ttu-id="f6330-133">La lunghezza massima è illimitata.</span><span class="sxs-lookup"><span data-stu-id="f6330-133">The maximum length is unbounded.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="f6330-134">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f6330-134">Child elements</span></span>



| <span data-ttu-id="f6330-135">Elemento</span><span class="sxs-lookup"><span data-stu-id="f6330-135">Element</span></span>                                                                             | <span data-ttu-id="f6330-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6330-136">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="f6330-137">**Button**</span><span class="sxs-lookup"><span data-stu-id="f6330-137">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="f6330-138">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="f6330-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f6330-139">**Casella**</span><span class="sxs-lookup"><span data-stu-id="f6330-139">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="f6330-140">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="f6330-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f6330-141">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="f6330-141">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="f6330-142">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="f6330-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f6330-143">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="f6330-143">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>               | <span data-ttu-id="f6330-144">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="f6330-144">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f6330-145">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="f6330-145">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>           | <span data-ttu-id="f6330-146">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="f6330-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f6330-147">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="f6330-147">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="f6330-148">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="f6330-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f6330-149">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="f6330-149">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="f6330-150">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="f6330-150">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f6330-151">**Controllo FontControl**</span><span class="sxs-lookup"><span data-stu-id="f6330-151">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                 | <span data-ttu-id="f6330-152">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="f6330-152">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="f6330-153">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="f6330-153">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/>         | <span data-ttu-id="f6330-154">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="f6330-154">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f6330-155">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="f6330-155">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/>           | <span data-ttu-id="f6330-156">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="f6330-156">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="f6330-157">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="f6330-157">**Spinner**</span></span>](windowsribbon-element-spinner.md)<br/>                         | <span data-ttu-id="f6330-158">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="f6330-158">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f6330-159">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="f6330-159">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="f6330-160">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="f6330-160">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f6330-161">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="f6330-161">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="f6330-162">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="f6330-162">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f6330-163">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="f6330-163">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="f6330-164">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="f6330-164">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="f6330-165">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="f6330-165">Parent elements</span></span>



| <span data-ttu-id="f6330-166">Elemento</span><span class="sxs-lookup"><span data-stu-id="f6330-166">Element</span></span>                                             |
|-----------------------------------------------------|
| [<span data-ttu-id="f6330-167">**Scheda**</span><span class="sxs-lookup"><span data-stu-id="f6330-167">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="f6330-168">Commenti</span><span class="sxs-lookup"><span data-stu-id="f6330-168">Remarks</span></span>

<span data-ttu-id="f6330-169">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f6330-169">Optional.</span></span>

<span data-ttu-id="f6330-170">Può verificarsi una o più volte per ogni [**elemento Tab.**](windowsribbon-element-tab.md)</span><span class="sxs-lookup"><span data-stu-id="f6330-170">May occur one or more times for each [**Tab**](windowsribbon-element-tab.md) element.</span></span>

<span data-ttu-id="f6330-171">[**Tab**](windowsribbon-element-tab.md) supporta le [modalità dell'applicazione](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="f6330-171">[**Tab**](windowsribbon-element-tab.md) supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="f6330-172">Il markup della barra multifunzione è valido solo quando gli elementi figlio di **Group** corrispondono al modello specificato per *SizeDefinition.*</span><span class="sxs-lookup"><span data-stu-id="f6330-172">The Ribbon markup is valid only when the child elements of **Group** correspond to the template specified for *SizeDefinition*.</span></span>

## <a name="examples"></a><span data-ttu-id="f6330-173">Esempio</span><span class="sxs-lookup"><span data-stu-id="f6330-173">Examples</span></span>

<span data-ttu-id="f6330-174">Nell'esempio di codice seguente viene illustrato l'utilizzo di un modello personalizzato in un **oggetto Group.**</span><span class="sxs-lookup"><span data-stu-id="f6330-174">The following code example illustrates the use of a custom template in a **Group**.</span></span>


```
<Group CommandName="cmdCustomGroup1" SizeDefinition="CustomTemplate">
  <Button CommandName="cmdCommand1" />
</Group>
```



## <a name="element-information"></a><span data-ttu-id="f6330-175">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f6330-175">Element information</span></span>

* <span data-ttu-id="f6330-176">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="f6330-176">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="f6330-177">**Può essere vuoto:** No</span><span class="sxs-lookup"><span data-stu-id="f6330-177">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="f6330-178">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6330-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6330-179">Personalizzazione di una barra multifunzione tramite definizioni delle dimensioni e criteri di ridimensionamento</span><span class="sxs-lookup"><span data-stu-id="f6330-179">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> <dt>

[<span data-ttu-id="f6330-180">Controllo Group</span><span class="sxs-lookup"><span data-stu-id="f6330-180">Group control</span></span>](windowsribbon-controls-group.md)
</dt> <dt>

[<span data-ttu-id="f6330-181">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="f6330-181">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

