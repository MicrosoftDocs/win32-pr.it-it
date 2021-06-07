---
title: Elemento ControlGroup
description: Rappresenta un gruppo di controlli in un modello di layout SizeDefinition.
ms.assetid: 688f3fa5-f305-4554-b16a-590983cf23b9
keywords:
- Elemento ControlGroup barra multifunzione di Windows
topic_type:
- apiref
api_name:
- ControlGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d2b49612102d03003c2f61395a56647aaef4475
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442942"
---
# <a name="controlgroup-element"></a><span data-ttu-id="bec0f-104">Elemento ControlGroup</span><span class="sxs-lookup"><span data-stu-id="bec0f-104">ControlGroup element</span></span>

<span data-ttu-id="bec0f-105">Rappresenta un gruppo di controlli in un modello di layout [**SizeDefinition.**](windowsribbon-element-sizedefinition.md)</span><span class="sxs-lookup"><span data-stu-id="bec0f-105">Represents a group of controls in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="bec0f-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="bec0f-106">Usage</span></span>

``` syntax
<ControlGroup
  SequenceNumber = "xs:positiveInteger">
  child elements
</ControlGroup>
```

## <a name="attributes"></a><span data-ttu-id="bec0f-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="bec0f-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bec0f-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="bec0f-108">Attribute</span></span></th>
<th><span data-ttu-id="bec0f-109">Type</span><span class="sxs-lookup"><span data-stu-id="bec0f-109">Type</span></span></th>
<th><span data-ttu-id="bec0f-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="bec0f-110">Required</span></span></th>
<th><span data-ttu-id="bec0f-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bec0f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bec0f-112"><strong>Sequencenumber</strong></span><span class="sxs-lookup"><span data-stu-id="bec0f-112"><strong>SequenceNumber</strong></span></span><br/></td>
<td><span data-ttu-id="bec0f-113">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="bec0f-113">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="bec0f-114">No</span><span class="sxs-lookup"><span data-stu-id="bec0f-114">No</span></span><br/></td>
<td><span data-ttu-id="bec0f-115">Valido solo quando <a href="windowsribbon-element-group.md"><strong>Group</strong></a> è l'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="bec0f-115">Valid only when <a href="windowsribbon-element-group.md"><strong>Group</strong></a> is the parent element.</span></span><br/> <span data-ttu-id="bec0f-116">Ogni <em>SequenceNumber deve</em> essere univoco all'interno di un <a href="windowsribbon-element-group.md"><strong>elemento Group.</strong></a></span><span class="sxs-lookup"><span data-stu-id="bec0f-116">Each <em>SequenceNumber</em> must be unique within a <a href="windowsribbon-element-group.md"><strong>Group</strong></a> element.</span></span> <span data-ttu-id="bec0f-117">I valori di <em>SequenceNumber</em> devono aumentare per ogni <strong>elemento Group,</strong> ma non devono essere sequenziali.</span><span class="sxs-lookup"><span data-stu-id="bec0f-117">The values for <em>SequenceNumber</em> should increase for each <strong>Group</strong> element, but do not need to be sequential.</span></span> <br/> <br/><span data-ttu-id="bec0f-118">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="bec0f-118">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="bec0f-119">Qualsiasi valore intero positivo compreso tra 1000 e 59999, inclusi.</span><span class="sxs-lookup"><span data-stu-id="bec0f-119">Any positive integer value between 1000 and 59999, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="bec0f-120">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="bec0f-120">Child elements</span></span>



| <span data-ttu-id="bec0f-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="bec0f-121">Element</span></span>                                                                                 | <span data-ttu-id="bec0f-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bec0f-122">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="bec0f-123">**Button**</span><span class="sxs-lookup"><span data-stu-id="bec0f-123">**Button**</span></span>](windowsribbon-element-button.md)<br/>                               | <span data-ttu-id="bec0f-124">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="bec0f-124">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="bec0f-125">**Casella**</span><span class="sxs-lookup"><span data-stu-id="bec0f-125">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                           | <span data-ttu-id="bec0f-126">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="bec0f-126">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="bec0f-127">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="bec0f-127">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                           | <span data-ttu-id="bec0f-128">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="bec0f-128">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="bec0f-129">**ControlSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="bec0f-129">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="bec0f-130">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="bec0f-130">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="bec0f-131">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="bec0f-131">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>               | <span data-ttu-id="bec0f-132">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="bec0f-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="bec0f-133">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="bec0f-133">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/>     | <span data-ttu-id="bec0f-134">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="bec0f-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="bec0f-135">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="bec0f-135">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>             | <span data-ttu-id="bec0f-136">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="bec0f-136">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="bec0f-137">**Controllo FontControl**</span><span class="sxs-lookup"><span data-stu-id="bec0f-137">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                     | <span data-ttu-id="bec0f-138">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="bec0f-138">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="bec0f-139">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="bec0f-139">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/>             | <span data-ttu-id="bec0f-140">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="bec0f-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="bec0f-141">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="bec0f-141">**Spinner**</span></span>](windowsribbon-element-spinner.md)<br/>                             | <span data-ttu-id="bec0f-142">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="bec0f-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="bec0f-143">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="bec0f-143">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                     | <span data-ttu-id="bec0f-144">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="bec0f-144">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="bec0f-145">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="bec0f-145">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>       | <span data-ttu-id="bec0f-146">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="bec0f-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="bec0f-147">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="bec0f-147">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                   | <span data-ttu-id="bec0f-148">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="bec0f-148">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="bec0f-149">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="bec0f-149">Parent elements</span></span>



| <span data-ttu-id="bec0f-150">Elemento</span><span class="sxs-lookup"><span data-stu-id="bec0f-150">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bec0f-151">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="bec0f-151">**ControlGroup**</span></span><br/>                                                         |
| [<span data-ttu-id="bec0f-152">**Gruppo**</span><span class="sxs-lookup"><span data-stu-id="bec0f-152">**Group**</span></span>](windowsribbon-element-group.md)<br/>                             |
| [<span data-ttu-id="bec0f-153">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="bec0f-153">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |
| [<span data-ttu-id="bec0f-154">**Riga**</span><span class="sxs-lookup"><span data-stu-id="bec0f-154">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a><span data-ttu-id="bec0f-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="bec0f-155">Remarks</span></span>

<span data-ttu-id="bec0f-156">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bec0f-156">Optional.</span></span>

<span data-ttu-id="bec0f-157">Può verificarsi una o più volte per ogni [**elemento Group**](windowsribbon-element-group.md) **o ControlGroup.**</span><span class="sxs-lookup"><span data-stu-id="bec0f-157">May occur one or more times for each [**Group**](windowsribbon-element-group.md) or **ControlGroup** element.</span></span>

<span data-ttu-id="bec0f-158">Se non vengono forniti numeri di sequenza, il rendering degli elementi viene eseguito nell'ordine specificato nel markup della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="bec0f-158">If no sequence numbers are supplied, elements are rendered in the order specified in the Ribbon markup.</span></span>

<span data-ttu-id="bec0f-159">Se [](windowsribbon-element-group.md) Group o **ControlGroup** è l'elemento padre, **ControlGroup** è vincolato ai seguenti possibili elementi figlio: [**Button,**](windowsribbon-element-button.md) [**CheckBox,**](windowsribbon-element-checkbox.md) [**ComboBox,**](windowsribbon-element-combobox.md) [**DropDownButton,**](windowsribbon-element-dropdownbutton.md) [**DropDownColorPicker,**](windowsribbon-element-dropdowncolorpicker.md) [**DropDownGallery,**](windowsribbon-element-dropdowngallery.md) [**FontControl,**](windowsribbon-element-fontcontrol.md) [**InRibbonGallery,**](windowsribbon-element-inribbongallery.md) [**Spinner,**](windowsribbon-element-spinner.md) [**SplitButton,**](windowsribbon-element-splitbutton.md) [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)o [**ToggleButton**](windowsribbon-element-togglebutton.md)</span><span class="sxs-lookup"><span data-stu-id="bec0f-159">If [**Group**](windowsribbon-element-group.md) or **ControlGroup** is the parent element then **ControlGroup** is constrained to the following possible child elements: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**InRibbonGallery**](windowsribbon-element-inribbongallery.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), or [**ToggleButton**](windowsribbon-element-togglebutton.md)</span></span>

<span data-ttu-id="bec0f-160">In caso contrario, [**quando Row**](windowsribbon-element-row.md) o [**GroupSizeDefinition è**](windowsribbon-element-groupsizedefinition.md) l'elemento padre, [**Group**](windowsribbon-element-group.md) è vincolato all'elemento figlio seguente: [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md).</span><span class="sxs-lookup"><span data-stu-id="bec0f-160">Otherwise, when [**Row**](windowsribbon-element-row.md) or [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) is the parent, [**Group**](windowsribbon-element-group.md) is constrained to the following possible child element: [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bec0f-161">Esempio</span><span class="sxs-lookup"><span data-stu-id="bec0f-161">Examples</span></span>

<span data-ttu-id="bec0f-162">L'esempio di codice seguente illustra il markup di base per un modello di layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) a quattro pulsanti personalizzato con vari [**elementi Group.**](windowsribbon-element-group.md)</span><span class="sxs-lookup"><span data-stu-id="bec0f-162">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various [**Group**](windowsribbon-element-group.md) elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="bec0f-163">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="bec0f-163">Element information</span></span>

* <span data-ttu-id="bec0f-164">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="bec0f-164">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="bec0f-165">**Può essere vuoto:** No</span><span class="sxs-lookup"><span data-stu-id="bec0f-165">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="bec0f-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bec0f-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bec0f-167">Personalizzazione di una barra multifunzione tramite definizioni delle dimensioni e criteri di ridimensionamento</span><span class="sxs-lookup"><span data-stu-id="bec0f-167">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





