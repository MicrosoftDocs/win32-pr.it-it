---
title: Elemento SizeDefinition
description: Rappresenta un modello di layout personalizzato dei controlli della barra multifunzione.
ms.assetid: f90bb469-aee2-4bba-9efe-142a39a8c1ae
keywords:
- Barra multifunzione Windows elemento SizeDefinition
topic_type:
- apiref
api_name:
- SizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bfab87f01700f8f4d36f76cbcbfe3696acfbec2
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "106299363"
---
# <a name="sizedefinition-element"></a><span data-ttu-id="e7416-104">Elemento SizeDefinition</span><span class="sxs-lookup"><span data-stu-id="e7416-104">SizeDefinition element</span></span>

<span data-ttu-id="e7416-105">Rappresenta un modello di layout personalizzato dei controlli della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="e7416-105">Represents a custom layout template of Ribbon controls.</span></span>

## <a name="usage"></a><span data-ttu-id="e7416-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="e7416-106">Usage</span></span>

``` syntax
<SizeDefinition
  Name = "xs:positiveInteger or xs:string or xs:token">
  child elements
</SizeDefinition>
```

## <a name="attributes"></a><span data-ttu-id="e7416-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="e7416-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e7416-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="e7416-108">Attribute</span></span></th>
<th><span data-ttu-id="e7416-109">Type</span><span class="sxs-lookup"><span data-stu-id="e7416-109">Type</span></span></th>
<th><span data-ttu-id="e7416-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="e7416-110">Required</span></span></th>
<th><span data-ttu-id="e7416-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7416-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e7416-112"><strong>Nome</strong></span><span class="sxs-lookup"><span data-stu-id="e7416-112"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="e7416-113">XS: positiveInteger o xs: String o xs: token</span><span class="sxs-lookup"><span data-stu-id="e7416-113">xs:positiveInteger or xs:string or xs:token</span></span><br/></td>
<td><span data-ttu-id="e7416-114">Sì</span><span class="sxs-lookup"><span data-stu-id="e7416-114">Yes</span></span><br/></td>
<td><span data-ttu-id="e7416-115">Quando <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Ribbon. SizeDefinitions</strong></a> è l'elemento padre; in caso contrario, facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e7416-115">When <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Ribbon.SizeDefinitions</strong></a> is the parent, otherwise optional.</span></span><br/> <br/><span data-ttu-id="e7416-116">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o xs: String o xs: token)</span><span class="sxs-lookup"><span data-stu-id="e7416-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string or xs:token)</span></span><br/> </dt> <dd> <span data-ttu-id="e7416-117">Stringa o valore intero compreso tra 2 e 59999, inclusivo o 0x2 e 0xea5f in formato esadecimale, inclusivo.</span><span class="sxs-lookup"><span data-stu-id="e7416-117">A string or an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="e7416-118">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="e7416-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="e7416-119">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="e7416-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="e7416-120">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="e7416-120">Child elements</span></span>



| <span data-ttu-id="e7416-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="e7416-121">Element</span></span>                                                                             | <span data-ttu-id="e7416-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7416-122">Description</span></span>                                     |
|-------------------------------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="e7416-123">**ControlNameMap**</span><span class="sxs-lookup"><span data-stu-id="e7416-123">**ControlNameMap**</span></span>](windowsribbon-element-controlnamemap.md)<br/>           | <span data-ttu-id="e7416-124">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="e7416-124">May occur at most once</span></span><br/> <br/>   |
| [<span data-ttu-id="e7416-125">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="e7416-125">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> | <span data-ttu-id="e7416-126">Deve essere presente almeno una volta</span><span class="sxs-lookup"><span data-stu-id="e7416-126">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="e7416-127">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="e7416-127">Parent elements</span></span>



| <span data-ttu-id="e7416-128">Elemento</span><span class="sxs-lookup"><span data-stu-id="e7416-128">Element</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7416-129">**Group**</span><span class="sxs-lookup"><span data-stu-id="e7416-129">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                   |
| [<span data-ttu-id="e7416-130">**Ribbon. SizeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="e7416-130">**Ribbon.SizeDefinitions**</span></span>](windowsribbon-element-ribbon-sizedefinitions.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="e7416-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7416-131">Remarks</span></span>

<span data-ttu-id="e7416-132">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e7416-132">Optional.</span></span>

<span data-ttu-id="e7416-133">Può verificarsi al massimo una volta per ogni elemento di [**gruppo**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="e7416-133">May occur at most once for each [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="e7416-134">Può essere presente una o più volte per ogni elemento [**Ribbon. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) .</span><span class="sxs-lookup"><span data-stu-id="e7416-134">May occur one or more times for each [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element.</span></span>

<span data-ttu-id="e7416-135">I [modelli di layout](windowsribbon-templates.md) del Framework della barra multifunzione predefiniti vengono specificati con l'attributo *SizeDefinition* dell'elemento di [**gruppo**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="e7416-135">Predefined Ribbon framework [layout templates](windowsribbon-templates.md) are specified with the *SizeDefinition* attribute of the [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="e7416-136">Se un elemento [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) corrispondente non viene dichiarato per ogni elemento di [**gruppo**](windowsribbon-element-group.md) in un elemento [**Tab**](windowsribbon-element-tab.md) , si verificherà un errore di convalida.</span><span class="sxs-lookup"><span data-stu-id="e7416-136">If a corresponding [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) element is not declared for each [**Group**](windowsribbon-element-group.md) element in a [**Tab**](windowsribbon-element-tab.md) element, a validation error will occur.</span></span>

## <a name="examples"></a><span data-ttu-id="e7416-137">Esempio</span><span class="sxs-lookup"><span data-stu-id="e7416-137">Examples</span></span>

<span data-ttu-id="e7416-138">Nell'esempio di codice riportato di seguito viene illustrato un modello personalizzato di base.</span><span class="sxs-lookup"><span data-stu-id="e7416-138">The following code example illustrates a basic custom template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="e7416-139">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e7416-139">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="e7416-140">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7416-140">Minimum supported system</span></span><br/> | <span data-ttu-id="e7416-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e7416-141">Windows 7</span></span> |
| <span data-ttu-id="e7416-142">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="e7416-142">Can be empty</span></span>                        | <span data-ttu-id="e7416-143">No</span><span class="sxs-lookup"><span data-stu-id="e7416-143">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="e7416-144">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e7416-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7416-145">Personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità</span><span class="sxs-lookup"><span data-stu-id="e7416-145">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





