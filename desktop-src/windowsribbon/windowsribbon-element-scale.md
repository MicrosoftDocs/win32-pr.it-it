---
title: Elemento Scale
description: Rappresenta le dimensioni e la preferenza di layout di un gruppo di controlli tramite una coppia Group, SizeDefinition.
ms.assetid: feef3721-c779-4c64-96c6-9d951ac32277
keywords:
- Barra multifunzione di Windows per l'elemento Scale
topic_type:
- apiref
api_name:
- Scale
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3ba922b65525b92189673020f7155275bdf49f9
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111445012"
---
# <a name="scale-element"></a><span data-ttu-id="b17e2-104">Elemento Scale</span><span class="sxs-lookup"><span data-stu-id="b17e2-104">Scale element</span></span>

<span data-ttu-id="b17e2-105">Rappresenta le dimensioni e la preferenza di layout [**di un gruppo**](windowsribbon-element-group.md) di controlli tramite una coppia {**Group**, [**SizeDefinition**](windowsribbon-element-sizedefinition.md)}.</span><span class="sxs-lookup"><span data-stu-id="b17e2-105">Represents the size and layout preference of a [**Group**](windowsribbon-element-group.md) of controls through a {**Group**, [**SizeDefinition**](windowsribbon-element-sizedefinition.md)} pair.</span></span>

## <a name="usage"></a><span data-ttu-id="b17e2-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="b17e2-106">Usage</span></span>

``` syntax
<Scale
  Size = "xs:string"
  Group = "xs:positiveInteger or xs:string"
/>
```

## <a name="attributes"></a><span data-ttu-id="b17e2-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="b17e2-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b17e2-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="b17e2-108">Attribute</span></span></th>
<th><span data-ttu-id="b17e2-109">Type</span><span class="sxs-lookup"><span data-stu-id="b17e2-109">Type</span></span></th>
<th><span data-ttu-id="b17e2-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b17e2-110">Required</span></span></th>
<th><span data-ttu-id="b17e2-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b17e2-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b17e2-112"><strong>Gruppo</strong></span><span class="sxs-lookup"><span data-stu-id="b17e2-112"><strong>Group</strong></span></span><br/></td>
<td><span data-ttu-id="b17e2-113">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="b17e2-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="b17e2-114">Sì</span><span class="sxs-lookup"><span data-stu-id="b17e2-114">Yes</span></span><br/></td>
<td><span data-ttu-id="b17e2-115">Deve corrispondere a un oggetto <a href="windowsribbon-element-group.md"><strong>CommandName</strong></a> <em>di gruppo esistente.</em></span><span class="sxs-lookup"><span data-stu-id="b17e2-115">Must correspond to an existing <a href="windowsribbon-element-group.md"><strong>Group</strong></a> <em>CommandName</em>.</span></span><br/> <br/><span data-ttu-id="b17e2-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="b17e2-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="b17e2-117">Stringa o valore intero compreso tra 2 e 59999, inclusi o 0x2 e 0xea5f in formato esadecimale, inclusivo.</span><span class="sxs-lookup"><span data-stu-id="b17e2-117">A string or an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="b17e2-118">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="b17e2-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="b17e2-119">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="b17e2-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b17e2-120"><strong>Dimensioni</strong></span><span class="sxs-lookup"><span data-stu-id="b17e2-120"><strong>Size</strong></span></span><br/></td>
<td><span data-ttu-id="b17e2-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="b17e2-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="b17e2-122">Sì</span><span class="sxs-lookup"><span data-stu-id="b17e2-122">Yes</span></span><br/></td>
<td><span data-ttu-id="b17e2-123">Questo valore deve corrispondere a una delle dimensioni valide per <em>l'attributo SizeDefinition</em> del gruppo <a href="windowsribbon-element-group.md"><strong>di</strong></a> controlli associato specificato in <em>Group.</em></span><span class="sxs-lookup"><span data-stu-id="b17e2-123">This value should correspond to one of the valid sizes for the <em>SizeDefinition</em> attribute of the associated <a href="windowsribbon-element-group.md"><strong>Group</strong></a> of controls specified in <em>Group</em>.</span></span> <br/> <span data-ttu-id="b17e2-124">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="b17e2-124">Restricted to one of the following values:</span></span> <br/> <br/><span data-ttu-id="b17e2-125">
<dt><span></span><span></span><strong></strong> (Popup)</span><span class="sxs-lookup"><span data-stu-id="b17e2-125">
<dt><span></span><span></span><strong></strong> (Popup)</span></span><br/> </dt> <dd> <span data-ttu-id="b17e2-126">Layout di controllo identico <code>Large</code> a ma ospitato in un riquadro popup o a discesa.</span><span class="sxs-lookup"><span data-stu-id="b17e2-126">Identical control layout to <code>Large</code> but hosted in a pop-up or a drop-down pane.</span></span><br/> </dd> <span data-ttu-id="b17e2-127"><dt><span></span><span></span><strong></strong> (Small)</span><span class="sxs-lookup"><span data-stu-id="b17e2-127"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="b17e2-128">Modello <a href="windowsribbon-element-sizedefinition.md"><strong>Small SizeDefinition.</strong></a></span><span class="sxs-lookup"><span data-stu-id="b17e2-128">Small <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> <span data-ttu-id="b17e2-129"><dt><span></span><span></span><strong></strong> (Media)</span><span class="sxs-lookup"><span data-stu-id="b17e2-129"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd> <span data-ttu-id="b17e2-130">Modello <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> medio.</span><span class="sxs-lookup"><span data-stu-id="b17e2-130">Medium <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> <span data-ttu-id="b17e2-131"><dt><span></span><span></span><strong></strong> (Grande)</span><span class="sxs-lookup"><span data-stu-id="b17e2-131"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="b17e2-132">Modello <a href="windowsribbon-element-sizedefinition.md"><strong>Large SizeDefinition.</strong></a></span><span class="sxs-lookup"><span data-stu-id="b17e2-132">Large <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> template.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="b17e2-133">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b17e2-133">Child elements</span></span>

<span data-ttu-id="b17e2-134">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="b17e2-134">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="b17e2-135">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="b17e2-135">Parent elements</span></span>



| <span data-ttu-id="b17e2-136">Elemento</span><span class="sxs-lookup"><span data-stu-id="b17e2-136">Element</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b17e2-137">**ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="b17e2-137">**ScalingPolicy**</span></span>](windowsribbon-element-scalingpolicy.md)<br/>                       |
| [<span data-ttu-id="b17e2-138">**ScalingPolicy.IdealSizes**</span><span class="sxs-lookup"><span data-stu-id="b17e2-138">**ScalingPolicy.IdealSizes**</span></span>](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="b17e2-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="b17e2-139">Remarks</span></span>

<span data-ttu-id="b17e2-140">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b17e2-140">Optional.</span></span>

<span data-ttu-id="b17e2-141">Può verificarsi una o più volte per [**ogni oggetto ScalingPolicy**](windowsribbon-element-scalingpolicy.md) [**o ScalingPolicy.IdealSizes.**](windowsribbon-element-scalingpolicy-idealsizes.md)</span><span class="sxs-lookup"><span data-stu-id="b17e2-141">May occur one or more times for each [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) or [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md).</span></span>

<span data-ttu-id="b17e2-142">Ogni coppia di attributi (*Group*, *Size*) deve essere univoca.</span><span class="sxs-lookup"><span data-stu-id="b17e2-142">Each (*Group*, *Size*) attribute pair must be unique.</span></span>

## <a name="examples"></a><span data-ttu-id="b17e2-143">Esempio</span><span class="sxs-lookup"><span data-stu-id="b17e2-143">Examples</span></span>

<span data-ttu-id="b17e2-144">L'esempio seguente illustra come personalizzare l'aspetto dei controlli in un oggetto [**Group**](windowsribbon-element-group.md) tramite la funzionalità di layout adattivo dei modelli [**SizeDefinition della**](windowsribbon-element-sizedefinition.md) barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="b17e2-144">The following example demonstrates how the appearance of controls in a [**Group**](windowsribbon-element-group.md) can be customized through the adaptive layout functionality of Ribbon [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span>

<span data-ttu-id="b17e2-145">Il [**manifesto ScalingPolicy**](windowsribbon-element-scalingpolicy.md) in questo esempio specifica una preferenza [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) per ognuno dei quattro gruppi di controlli in una **scheda Home.** Inoltre, gli **elementi Scale** vengono specificati per influenzare il comportamento di compressione, in ordine di dimensione decrescente, di ogni gruppo.</span><span class="sxs-lookup"><span data-stu-id="b17e2-145">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest in this example specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, **Scale** elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


```XML
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
```



## <a name="element-information"></a><span data-ttu-id="b17e2-146">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b17e2-146">Element information</span></span>



* <span data-ttu-id="b17e2-147">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="b17e2-147">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="b17e2-148">**Può essere vuoto:** Sì</span><span class="sxs-lookup"><span data-stu-id="b17e2-148">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="b17e2-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b17e2-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b17e2-150">Personalizzazione di una barra multifunzione tramite definizioni delle dimensioni e criteri di ridimensionamento</span><span class="sxs-lookup"><span data-stu-id="b17e2-150">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





