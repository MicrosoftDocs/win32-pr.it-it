---
title: Elemento ControlGroup
description: Rappresenta un gruppo di controlli in un modello di layout SizeDefinition.
ms.assetid: 688f3fa5-f305-4554-b16a-590983cf23b9
keywords:
- Barra multifunzione Windows elemento ControlGroup
topic_type:
- apiref
api_name:
- ControlGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd6df69f788efe01b9eb2c7ffe0aaddd98bd7198
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "104398488"
---
# <a name="controlgroup-element"></a><span data-ttu-id="f583e-104">Elemento ControlGroup</span><span class="sxs-lookup"><span data-stu-id="f583e-104">ControlGroup element</span></span>

<span data-ttu-id="f583e-105">Rappresenta un gruppo di controlli in un modello di layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="f583e-105">Represents a group of controls in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="f583e-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="f583e-106">Usage</span></span>

``` syntax
<ControlGroup
  SequenceNumber = "xs:positiveInteger">
  child elements
</ControlGroup>
```

## <a name="attributes"></a><span data-ttu-id="f583e-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="f583e-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f583e-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="f583e-108">Attribute</span></span></th>
<th><span data-ttu-id="f583e-109">Type</span><span class="sxs-lookup"><span data-stu-id="f583e-109">Type</span></span></th>
<th><span data-ttu-id="f583e-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f583e-110">Required</span></span></th>
<th><span data-ttu-id="f583e-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f583e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f583e-112"><strong>SequenceNumber</strong></span><span class="sxs-lookup"><span data-stu-id="f583e-112"><strong>SequenceNumber</strong></span></span><br/></td>
<td><span data-ttu-id="f583e-113">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="f583e-113">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="f583e-114">No</span><span class="sxs-lookup"><span data-stu-id="f583e-114">No</span></span><br/></td>
<td><span data-ttu-id="f583e-115">Valido solo quando il <a href="windowsribbon-element-group.md"><strong>gruppo</strong></a> è l'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="f583e-115">Valid only when <a href="windowsribbon-element-group.md"><strong>Group</strong></a> is the parent element.</span></span><br/> <span data-ttu-id="f583e-116">Ogni <em>SequenceNumber</em> deve essere univoco all'interno di un elemento di <a href="windowsribbon-element-group.md"><strong>gruppo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f583e-116">Each <em>SequenceNumber</em> must be unique within a <a href="windowsribbon-element-group.md"><strong>Group</strong></a> element.</span></span> <span data-ttu-id="f583e-117">I valori per <em>SequenceNumber</em> dovrebbero aumentare per ogni elemento di <strong>gruppo</strong> , ma non devono essere sequenziali.</span><span class="sxs-lookup"><span data-stu-id="f583e-117">The values for <em>SequenceNumber</em> should increase for each <strong>Group</strong> element, but do not need to be sequential.</span></span> <br/> <br/><span data-ttu-id="f583e-118">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="f583e-118">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="f583e-119">Qualsiasi valore intero positivo compreso tra 1000 e 59999 inclusi.</span><span class="sxs-lookup"><span data-stu-id="f583e-119">Any positive integer value between 1000 and 59999, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="f583e-120">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f583e-120">Child elements</span></span>



| <span data-ttu-id="f583e-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="f583e-121">Element</span></span>                                                                                 | <span data-ttu-id="f583e-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f583e-122">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="f583e-123">**Button**</span><span class="sxs-lookup"><span data-stu-id="f583e-123">**Button**</span></span>](windowsribbon-element-button.md)<br/>                               | <span data-ttu-id="f583e-124">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="f583e-124">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f583e-125">**Casella**</span><span class="sxs-lookup"><span data-stu-id="f583e-125">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                           | <span data-ttu-id="f583e-126">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="f583e-126">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f583e-127">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="f583e-127">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                           | <span data-ttu-id="f583e-128">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="f583e-128">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f583e-129">**ControlSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="f583e-129">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="f583e-130">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="f583e-130">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f583e-131">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="f583e-131">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>               | <span data-ttu-id="f583e-132">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="f583e-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f583e-133">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="f583e-133">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/>     | <span data-ttu-id="f583e-134">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="f583e-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f583e-135">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="f583e-135">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>             | <span data-ttu-id="f583e-136">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="f583e-136">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f583e-137">**FontControl**</span><span class="sxs-lookup"><span data-stu-id="f583e-137">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                     | <span data-ttu-id="f583e-138">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="f583e-138">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="f583e-139">**Inribbongallery**</span><span class="sxs-lookup"><span data-stu-id="f583e-139">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/>             | <span data-ttu-id="f583e-140">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="f583e-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f583e-141">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="f583e-141">**Spinner**</span></span>](windowsribbon-element-spinner.md)<br/>                             | <span data-ttu-id="f583e-142">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="f583e-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f583e-143">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="f583e-143">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                     | <span data-ttu-id="f583e-144">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="f583e-144">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f583e-145">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="f583e-145">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>       | <span data-ttu-id="f583e-146">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="f583e-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f583e-147">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="f583e-147">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                   | <span data-ttu-id="f583e-148">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="f583e-148">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="f583e-149">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="f583e-149">Parent elements</span></span>



| <span data-ttu-id="f583e-150">Elemento</span><span class="sxs-lookup"><span data-stu-id="f583e-150">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f583e-151">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="f583e-151">**ControlGroup**</span></span><br/>                                                         |
| [<span data-ttu-id="f583e-152">**Group**</span><span class="sxs-lookup"><span data-stu-id="f583e-152">**Group**</span></span>](windowsribbon-element-group.md)<br/>                             |
| [<span data-ttu-id="f583e-153">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="f583e-153">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |
| [<span data-ttu-id="f583e-154">**Riga**</span><span class="sxs-lookup"><span data-stu-id="f583e-154">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a><span data-ttu-id="f583e-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="f583e-155">Remarks</span></span>

<span data-ttu-id="f583e-156">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f583e-156">Optional.</span></span>

<span data-ttu-id="f583e-157">Può essere presente una o più volte per ogni elemento [**Group**](windowsribbon-element-group.md) o **ControlGroup** .</span><span class="sxs-lookup"><span data-stu-id="f583e-157">May occur one or more times for each [**Group**](windowsribbon-element-group.md) or **ControlGroup** element.</span></span>

<span data-ttu-id="f583e-158">Se non viene fornito alcun numero di sequenza, viene eseguito il rendering degli elementi nell'ordine specificato nel markup della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="f583e-158">If no sequence numbers are supplied, elements are rendered in the order specified in the Ribbon markup.</span></span>

<span data-ttu-id="f583e-159">Se [**Group**](windowsribbon-element-group.md) o **ControlGroup** è l'elemento padre, **ControlGroup** è vincolato ai seguenti elementi figlio possibili: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**inribbongallery**](windowsribbon-element-inribbongallery.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)o [**ToggleButton**](windowsribbon-element-togglebutton.md)</span><span class="sxs-lookup"><span data-stu-id="f583e-159">If [**Group**](windowsribbon-element-group.md) or **ControlGroup** is the parent element then **ControlGroup** is constrained to the following possible child elements: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**InRibbonGallery**](windowsribbon-element-inribbongallery.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), or [**ToggleButton**](windowsribbon-element-togglebutton.md)</span></span>

<span data-ttu-id="f583e-160">In caso contrario, quando [**Row**](windowsribbon-element-row.md) o [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) è il padre, il [**gruppo**](windowsribbon-element-group.md) è vincolato al seguente elemento figlio possibile: [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md).</span><span class="sxs-lookup"><span data-stu-id="f583e-160">Otherwise, when [**Row**](windowsribbon-element-row.md) or [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) is the parent, [**Group**](windowsribbon-element-group.md) is constrained to the following possible child element: [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f583e-161">Esempio</span><span class="sxs-lookup"><span data-stu-id="f583e-161">Examples</span></span>

<span data-ttu-id="f583e-162">Nell'esempio di codice seguente viene illustrato il markup di base per un modello di layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) personalizzato a quattro pulsanti con vari elementi di [**gruppo**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="f583e-162">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various [**Group**](windowsribbon-element-group.md) elements.</span></span>


```XML
<Group CommandName="cmdButtonGroup2">
  <SizeDefinition>
    <ControlNameMap>
      <ControlNameDefinition Name="button1"/>
      <ControlNameDefinition Name="button2"/>
      <ControlNameDefinition Name="button3"/>
      <ControlNameDefinition Name="button4"/>
    </ControlNameMap>
    <GroupSizeDefinition Size="Large">
      <ControlGroup>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Large"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Large"
                               IsLabelVisible="true" />
      </ControlGroup>
      <ColumnBreak ShowSeparator="true"/>
      <ControlGroup>
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Large"
                              IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                              ImageSize="Large"
                              IsLabelVisible="true" />
      </ControlGroup>
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <Row>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Small"
                               IsLabelVisible="true" />
      </Row>
      <Row>
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                               ImageSize="Small"
                               IsLabelVisible="true" />
      </Row>
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <Row>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Small"
                               IsLabelVisible="false" />
      </Row>
      <Row>
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                               ImageSize="Small"
                               IsLabelVisible="false" />
      </Row>
    </GroupSizeDefinition>
  </SizeDefinition>
  <Button CommandName="cmdButtonG21"></Button>
  <Button CommandName="cmdButtonG22"></Button>
  <Button CommandName="cmdButtonG23"></Button>
  <Button CommandName="cmdButtonG24"></Button>
</Group>
<Group CommandName="cmdCheckBoxGroup">
  <CheckBox CommandName="cmdCheckBox"></CheckBox>
</Group>
<Group CommandName="cmdToggleButtonGroup"
       SizeDefinition="OneButton">
  <ToggleButton CommandName="cmdToggleButton"></ToggleButton>
</Group>
<Group CommandName="cmdButtonGroup"
       SizeDefinition="ThreeButtons">
  <Button CommandName="cmdButton1"></Button>
  <Button CommandName="cmdButton2"></Button>
  <Button CommandName="cmdButton3"></Button>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="f583e-163">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f583e-163">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="f583e-164">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f583e-164">Minimum supported system</span></span><br/> | <span data-ttu-id="f583e-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f583e-165">Windows 7</span></span> |
| <span data-ttu-id="f583e-166">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="f583e-166">Can be empty</span></span>                        | <span data-ttu-id="f583e-167">No</span><span class="sxs-lookup"><span data-stu-id="f583e-167">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="f583e-168">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f583e-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f583e-169">Personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità</span><span class="sxs-lookup"><span data-stu-id="f583e-169">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





