---
title: Elemento ControlSizeDefinition
description: Rappresenta lo stile di layout di un gruppo di controlli in un modello personalizzato.
ms.assetid: f9b875f4-e0cf-4823-81b5-ed19c201dcbb
keywords:
- Elemento ControlSizeDefinition Nella barra multifunzione di Windows
topic_type:
- apiref
api_name:
- ControlSizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ff5217c08b4ea6da1931b0c65501f912f2cc5dc
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443412"
---
# <a name="controlsizedefinition-element"></a><span data-ttu-id="96e4d-104">Elemento ControlSizeDefinition</span><span class="sxs-lookup"><span data-stu-id="96e4d-104">ControlSizeDefinition element</span></span>

<span data-ttu-id="96e4d-105">Rappresenta lo stile di layout di un gruppo di controlli in un modello personalizzato.</span><span class="sxs-lookup"><span data-stu-id="96e4d-105">Represents the layout style of a group of controls in a custom template.</span></span>

## <a name="usage"></a><span data-ttu-id="96e4d-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="96e4d-106">Usage</span></span>

``` syntax
<ControlSizeDefinition
  ImageSize = "xs:string"
  IsLabelVisible = "Boolean"
  IsImageVisible = "Boolean"
  IsPopup = "Boolean"
  ControlName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="96e4d-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="96e4d-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="96e4d-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="96e4d-108">Attribute</span></span></th>
<th><span data-ttu-id="96e4d-109">Type</span><span class="sxs-lookup"><span data-stu-id="96e4d-109">Type</span></span></th>
<th><span data-ttu-id="96e4d-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="96e4d-110">Required</span></span></th>
<th><span data-ttu-id="96e4d-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96e4d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="96e4d-112"><strong>Nomecontrollo</strong></span><span class="sxs-lookup"><span data-stu-id="96e4d-112"><strong>ControlName</strong></span></span><br/></td>
<td><span data-ttu-id="96e4d-113">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="96e4d-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="96e4d-114">No</span><span class="sxs-lookup"><span data-stu-id="96e4d-114">No</span></span><br/></td>
<td><span data-ttu-id="96e4d-115"><dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="96e4d-115"><dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="96e4d-116">Stringa, valore intero compreso tra 2 e 59999 inclusi o valore esadecimale compreso tra 0x2 e 0xea5f inclusi.</span><span class="sxs-lookup"><span data-stu-id="96e4d-116">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="96e4d-117">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="96e4d-117">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="96e4d-118">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="96e4d-118">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96e4d-119"><strong>Imagesize</strong></span><span class="sxs-lookup"><span data-stu-id="96e4d-119"><strong>ImageSize</strong></span></span><br/></td>
<td><span data-ttu-id="96e4d-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="96e4d-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="96e4d-121">No</span><span class="sxs-lookup"><span data-stu-id="96e4d-121">No</span></span><br/></td>
<td><span data-ttu-id="96e4d-122">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="96e4d-122">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="96e4d-123">
<dt><span></span><span></span><strong></strong> (Grande)</span><span class="sxs-lookup"><span data-stu-id="96e4d-123">
<dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="96e4d-124"><dt><span></span><span></span><strong></strong> (Small)</span><span class="sxs-lookup"><span data-stu-id="96e4d-124"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="96e4d-125">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="96e4d-125">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96e4d-126"><strong>IsImageVisible</strong></span><span class="sxs-lookup"><span data-stu-id="96e4d-126"><strong>IsImageVisible</strong></span></span><br/></td>
<td><span data-ttu-id="96e4d-127">Boolean</span><span class="sxs-lookup"><span data-stu-id="96e4d-127">Boolean</span></span><br/></td>
<td><span data-ttu-id="96e4d-128">No</span><span class="sxs-lookup"><span data-stu-id="96e4d-128">No</span></span><br/></td>
<td><span data-ttu-id="96e4d-129">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="96e4d-129">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="96e4d-130">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="96e4d-130">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="96e4d-131">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="96e4d-131">Default.</span></span> <br/> </dd> <span data-ttu-id="96e4d-132"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="96e4d-132"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96e4d-133"><strong>IsLabelVisible</strong></span><span class="sxs-lookup"><span data-stu-id="96e4d-133"><strong>IsLabelVisible</strong></span></span><br/></td>
<td><span data-ttu-id="96e4d-134">Boolean</span><span class="sxs-lookup"><span data-stu-id="96e4d-134">Boolean</span></span><br/></td>
<td><span data-ttu-id="96e4d-135">No</span><span class="sxs-lookup"><span data-stu-id="96e4d-135">No</span></span><br/></td>
<td><span data-ttu-id="96e4d-136">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="96e4d-136">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="96e4d-137">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="96e4d-137">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="96e4d-138">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="96e4d-138">Default.</span></span> <br/> </dd> <span data-ttu-id="96e4d-139"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="96e4d-139"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96e4d-140"><strong>IsPopup</strong></span><span class="sxs-lookup"><span data-stu-id="96e4d-140"><strong>IsPopup</strong></span></span><br/></td>
<td><span data-ttu-id="96e4d-141">Boolean</span><span class="sxs-lookup"><span data-stu-id="96e4d-141">Boolean</span></span><br/></td>
<td><span data-ttu-id="96e4d-142">No</span><span class="sxs-lookup"><span data-stu-id="96e4d-142">No</span></span><br/></td>
<td><span data-ttu-id="96e4d-143">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="96e4d-143">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="96e4d-144">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="96e4d-144">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="96e4d-145"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="96e4d-145"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="96e4d-146">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="96e4d-146">Child elements</span></span>

<span data-ttu-id="96e4d-147">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="96e4d-147">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="96e4d-148">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="96e4d-148">Parent elements</span></span>



| <span data-ttu-id="96e4d-149">Elemento</span><span class="sxs-lookup"><span data-stu-id="96e4d-149">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="96e4d-150">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="96e4d-150">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>               |
| [<span data-ttu-id="96e4d-151">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="96e4d-151">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |
| [<span data-ttu-id="96e4d-152">**Riga**</span><span class="sxs-lookup"><span data-stu-id="96e4d-152">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a><span data-ttu-id="96e4d-153">Commenti</span><span class="sxs-lookup"><span data-stu-id="96e4d-153">Remarks</span></span>

<span data-ttu-id="96e4d-154">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="96e4d-154">Optional.</span></span>

<span data-ttu-id="96e4d-155">Può verificarsi una o più volte per [**ogni elemento ControlGroup,**](windowsribbon-element-controlgroup.md) [**Row**](windowsribbon-element-row.md) [**o SizeDefinition.**](windowsribbon-element-sizedefinition.md)</span><span class="sxs-lookup"><span data-stu-id="96e4d-155">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Row**](windowsribbon-element-row.md), or [**SizeDefinition**](windowsribbon-element-sizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="96e4d-156">Esempio</span><span class="sxs-lookup"><span data-stu-id="96e4d-156">Examples</span></span>

<span data-ttu-id="96e4d-157">L'esempio di codice seguente illustra il markup di base per un modello di layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) a quattro pulsanti personalizzato con vari **elementi ControlSizeDefinition.**</span><span class="sxs-lookup"><span data-stu-id="96e4d-157">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various **ControlSizeDefinition** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="96e4d-158">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="96e4d-158">Element information</span></span>

* <span data-ttu-id="96e4d-159">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="96e4d-159">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="96e4d-160">**Può essere vuoto:** Sì</span><span class="sxs-lookup"><span data-stu-id="96e4d-160">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="96e4d-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96e4d-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96e4d-162">Personalizzazione di una barra multifunzione tramite definizioni delle dimensioni e criteri di ridimensionamento</span><span class="sxs-lookup"><span data-stu-id="96e4d-162">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





