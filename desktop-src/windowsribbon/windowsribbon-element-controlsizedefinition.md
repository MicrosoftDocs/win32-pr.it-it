---
title: Elemento ControlSizeDefinition
description: Rappresenta lo stile di layout di un gruppo di controlli in un modello personalizzato.
ms.assetid: f9b875f4-e0cf-4823-81b5-ed19c201dcbb
keywords:
- Barra multifunzione Windows elemento ControlSizeDefinition
topic_type:
- apiref
api_name:
- ControlSizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e35fe159bf5bafa1ebfa6119215a4265ee900ef0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334175"
---
# <a name="controlsizedefinition-element"></a><span data-ttu-id="7a816-104">Elemento ControlSizeDefinition</span><span class="sxs-lookup"><span data-stu-id="7a816-104">ControlSizeDefinition element</span></span>

<span data-ttu-id="7a816-105">Rappresenta lo stile di layout di un gruppo di controlli in un modello personalizzato.</span><span class="sxs-lookup"><span data-stu-id="7a816-105">Represents the layout style of a group of controls in a custom template.</span></span>

## <a name="usage"></a><span data-ttu-id="7a816-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="7a816-106">Usage</span></span>

``` syntax
<ControlSizeDefinition
  ImageSize = "xs:string"
  IsLabelVisible = "Boolean"
  IsImageVisible = "Boolean"
  IsPopup = "Boolean"
  ControlName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="7a816-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="7a816-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7a816-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="7a816-108">Attribute</span></span></th>
<th><span data-ttu-id="7a816-109">Type</span><span class="sxs-lookup"><span data-stu-id="7a816-109">Type</span></span></th>
<th><span data-ttu-id="7a816-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="7a816-110">Required</span></span></th>
<th><span data-ttu-id="7a816-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a816-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7a816-112"><strong>ControlName</strong></span><span class="sxs-lookup"><span data-stu-id="7a816-112"><strong>ControlName</strong></span></span><br/></td>
<td><span data-ttu-id="7a816-113">XS: positiveInteger o xs: String</span><span class="sxs-lookup"><span data-stu-id="7a816-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="7a816-114">No</span><span class="sxs-lookup"><span data-stu-id="7a816-114">No</span></span><br/></td>
<td><span data-ttu-id="7a816-115"><dt><span></span><span></span><strong></strong> (XS: positiveInteger o xs: String)</span><span class="sxs-lookup"><span data-stu-id="7a816-115"><dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="7a816-116">Stringa, valore intero compreso tra 2 e 59999, inclusivo o un valore esadecimale compreso tra 0x2 e 0xea5f, inclusi.</span><span class="sxs-lookup"><span data-stu-id="7a816-116">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="7a816-117">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="7a816-117">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="7a816-118">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="7a816-118">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a816-119"><strong>ImageSize</strong></span><span class="sxs-lookup"><span data-stu-id="7a816-119"><strong>ImageSize</strong></span></span><br/></td>
<td><span data-ttu-id="7a816-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="7a816-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="7a816-121">No</span><span class="sxs-lookup"><span data-stu-id="7a816-121">No</span></span><br/></td>
<td><span data-ttu-id="7a816-122">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="7a816-122">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="7a816-123">
<dt><span></span><span></span><strong></strong> Grandi dimensioni</span><span class="sxs-lookup"><span data-stu-id="7a816-123">
<dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="7a816-124"><dt><span></span><span></span><strong></strong> Piccolo</span><span class="sxs-lookup"><span data-stu-id="7a816-124"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="7a816-125">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="7a816-125">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a816-126"><strong>IsImageVisible</strong></span><span class="sxs-lookup"><span data-stu-id="7a816-126"><strong>IsImageVisible</strong></span></span><br/></td>
<td><span data-ttu-id="7a816-127">Boolean</span><span class="sxs-lookup"><span data-stu-id="7a816-127">Boolean</span></span><br/></td>
<td><span data-ttu-id="7a816-128">No</span><span class="sxs-lookup"><span data-stu-id="7a816-128">No</span></span><br/></td>
<td><span data-ttu-id="7a816-129">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="7a816-129">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="7a816-130">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="7a816-130">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="7a816-131">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="7a816-131">Default.</span></span> <br/> </dd> <span data-ttu-id="7a816-132"><dt><span></span><span></span><strong></strong> false</span><span class="sxs-lookup"><span data-stu-id="7a816-132"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a816-133"><strong>IsLabelVisible</strong></span><span class="sxs-lookup"><span data-stu-id="7a816-133"><strong>IsLabelVisible</strong></span></span><br/></td>
<td><span data-ttu-id="7a816-134">Boolean</span><span class="sxs-lookup"><span data-stu-id="7a816-134">Boolean</span></span><br/></td>
<td><span data-ttu-id="7a816-135">No</span><span class="sxs-lookup"><span data-stu-id="7a816-135">No</span></span><br/></td>
<td><span data-ttu-id="7a816-136">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="7a816-136">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="7a816-137">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="7a816-137">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="7a816-138">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="7a816-138">Default.</span></span> <br/> </dd> <span data-ttu-id="7a816-139"><dt><span></span><span></span><strong></strong> false</span><span class="sxs-lookup"><span data-stu-id="7a816-139"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a816-140"><strong>Popup</strong></span><span class="sxs-lookup"><span data-stu-id="7a816-140"><strong>IsPopup</strong></span></span><br/></td>
<td><span data-ttu-id="7a816-141">Boolean</span><span class="sxs-lookup"><span data-stu-id="7a816-141">Boolean</span></span><br/></td>
<td><span data-ttu-id="7a816-142">No</span><span class="sxs-lookup"><span data-stu-id="7a816-142">No</span></span><br/></td>
<td><span data-ttu-id="7a816-143">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="7a816-143">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="7a816-144">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="7a816-144">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="7a816-145"><dt><span></span><span></span><strong></strong> false</span><span class="sxs-lookup"><span data-stu-id="7a816-145"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="7a816-146">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="7a816-146">Child elements</span></span>

<span data-ttu-id="7a816-147">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="7a816-147">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="7a816-148">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="7a816-148">Parent elements</span></span>



| <span data-ttu-id="7a816-149">Elemento</span><span class="sxs-lookup"><span data-stu-id="7a816-149">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="7a816-150">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="7a816-150">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>               |
| [<span data-ttu-id="7a816-151">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="7a816-151">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |
| [<span data-ttu-id="7a816-152">**Riga**</span><span class="sxs-lookup"><span data-stu-id="7a816-152">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a><span data-ttu-id="7a816-153">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a816-153">Remarks</span></span>

<span data-ttu-id="7a816-154">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="7a816-154">Optional.</span></span>

<span data-ttu-id="7a816-155">Può essere presente una o più volte per ogni elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Row**](windowsribbon-element-row.md)o [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="7a816-155">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Row**](windowsribbon-element-row.md), or [**SizeDefinition**](windowsribbon-element-sizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="7a816-156">Esempio</span><span class="sxs-lookup"><span data-stu-id="7a816-156">Examples</span></span>

<span data-ttu-id="7a816-157">Nell'esempio di codice seguente viene illustrato il markup di base per un modello di layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) personalizzato a quattro pulsanti con vari elementi **ControlSizeDefinition** .</span><span class="sxs-lookup"><span data-stu-id="7a816-157">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various **ControlSizeDefinition** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="7a816-158">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7a816-158">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="7a816-159">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a816-159">Minimum supported system</span></span><br/> | <span data-ttu-id="7a816-160">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7a816-160">Windows 7</span></span> |
| <span data-ttu-id="7a816-161">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="7a816-161">Can be empty</span></span>                        | <span data-ttu-id="7a816-162">Sì</span><span class="sxs-lookup"><span data-stu-id="7a816-162">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="7a816-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a816-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a816-164">Personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità</span><span class="sxs-lookup"><span data-stu-id="7a816-164">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





