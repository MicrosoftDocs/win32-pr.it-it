---
title: Elemento SizeDefinition
description: Rappresenta un modello di layout personalizzato dei controlli barra multifunzione.
ms.assetid: f90bb469-aee2-4bba-9efe-142a39a8c1ae
keywords:
- Barra multifunzione di Windows per l'elemento SizeDefinition
topic_type:
- apiref
api_name:
- SizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cc68ac032459bed77d402ebd860886398748c874
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444802"
---
# <a name="sizedefinition-element"></a><span data-ttu-id="13521-104">Elemento SizeDefinition</span><span class="sxs-lookup"><span data-stu-id="13521-104">SizeDefinition element</span></span>

<span data-ttu-id="13521-105">Rappresenta un modello di layout personalizzato dei controlli barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="13521-105">Represents a custom layout template of Ribbon controls.</span></span>

## <a name="usage"></a><span data-ttu-id="13521-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="13521-106">Usage</span></span>

``` syntax
<SizeDefinition
  Name = "xs:positiveInteger or xs:string or xs:token">
  child elements
</SizeDefinition>
```

## <a name="attributes"></a><span data-ttu-id="13521-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="13521-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="13521-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="13521-108">Attribute</span></span></th>
<th><span data-ttu-id="13521-109">Type</span><span class="sxs-lookup"><span data-stu-id="13521-109">Type</span></span></th>
<th><span data-ttu-id="13521-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="13521-110">Required</span></span></th>
<th><span data-ttu-id="13521-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13521-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="13521-112"><strong>Nome</strong></span><span class="sxs-lookup"><span data-stu-id="13521-112"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="13521-113">xs:positiveInteger o xs:string o xs:token</span><span class="sxs-lookup"><span data-stu-id="13521-113">xs:positiveInteger or xs:string or xs:token</span></span><br/></td>
<td><span data-ttu-id="13521-114">Sì</span><span class="sxs-lookup"><span data-stu-id="13521-114">Yes</span></span><br/></td>
<td><span data-ttu-id="13521-115">Quando <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Ribbon.SizeDefinitions è</strong></a> l'elemento padre, in caso contrario facoltativo.</span><span class="sxs-lookup"><span data-stu-id="13521-115">When <a href="windowsribbon-element-ribbon-sizedefinitions.md"><strong>Ribbon.SizeDefinitions</strong></a> is the parent, otherwise optional.</span></span><br/> <br/><span data-ttu-id="13521-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string o xs:token)</span><span class="sxs-lookup"><span data-stu-id="13521-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string or xs:token)</span></span><br/> </dt> <dd> <span data-ttu-id="13521-117">Stringa o valore intero compreso tra 2 e 59999, inclusivo o 0x2 e 0xea5f in formato esadecimale, inclusivo.</span><span class="sxs-lookup"><span data-stu-id="13521-117">A string or an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="13521-118">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="13521-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="13521-119">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="13521-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="13521-120">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="13521-120">Child elements</span></span>



| <span data-ttu-id="13521-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="13521-121">Element</span></span>                                                                             | <span data-ttu-id="13521-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13521-122">Description</span></span>                                     |
|-------------------------------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="13521-123">**ControlNameMap**</span><span class="sxs-lookup"><span data-stu-id="13521-123">**ControlNameMap**</span></span>](windowsribbon-element-controlnamemap.md)<br/>           | <span data-ttu-id="13521-124">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="13521-124">May occur at most once</span></span><br/> <br/>   |
| [<span data-ttu-id="13521-125">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="13521-125">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> | <span data-ttu-id="13521-126">Deve verificarsi almeno una volta</span><span class="sxs-lookup"><span data-stu-id="13521-126">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="13521-127">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="13521-127">Parent elements</span></span>



| <span data-ttu-id="13521-128">Elemento</span><span class="sxs-lookup"><span data-stu-id="13521-128">Element</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="13521-129">**Gruppo**</span><span class="sxs-lookup"><span data-stu-id="13521-129">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                   |
| [<span data-ttu-id="13521-130">**Ribbon.SizeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="13521-130">**Ribbon.SizeDefinitions**</span></span>](windowsribbon-element-ribbon-sizedefinitions.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="13521-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="13521-131">Remarks</span></span>

<span data-ttu-id="13521-132">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="13521-132">Optional.</span></span>

<span data-ttu-id="13521-133">Può verificarsi al massimo una volta per ogni [**elemento**](windowsribbon-element-group.md) Group.</span><span class="sxs-lookup"><span data-stu-id="13521-133">May occur at most once for each [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="13521-134">Può verificarsi una o più volte per [**ogni elemento Ribbon.SizeDefinitions.**](windowsribbon-element-ribbon-sizedefinitions.md)</span><span class="sxs-lookup"><span data-stu-id="13521-134">May occur one or more times for each [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element.</span></span>

<span data-ttu-id="13521-135">I modelli di layout predefiniti del framework [della](windowsribbon-templates.md) barra multifunzione vengono specificati con *l'attributo SizeDefinition* dell'elemento [**Group.**](windowsribbon-element-group.md)</span><span class="sxs-lookup"><span data-stu-id="13521-135">Predefined Ribbon framework [layout templates](windowsribbon-templates.md) are specified with the *SizeDefinition* attribute of the [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="13521-136">Se un elemento [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) corrispondente non viene dichiarato per ogni [**elemento Group**](windowsribbon-element-group.md) in un elemento [**Tab,**](windowsribbon-element-tab.md) si verificherà un errore di convalida.</span><span class="sxs-lookup"><span data-stu-id="13521-136">If a corresponding [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) element is not declared for each [**Group**](windowsribbon-element-group.md) element in a [**Tab**](windowsribbon-element-tab.md) element, a validation error will occur.</span></span>

## <a name="examples"></a><span data-ttu-id="13521-137">Esempio</span><span class="sxs-lookup"><span data-stu-id="13521-137">Examples</span></span>

<span data-ttu-id="13521-138">L'esempio di codice seguente illustra un modello personalizzato di base.</span><span class="sxs-lookup"><span data-stu-id="13521-138">The following code example illustrates a basic custom template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="13521-139">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="13521-139">Element information</span></span>


- <span data-ttu-id="13521-140">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="13521-140">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="13521-141">**Può essere vuoto:** No</span><span class="sxs-lookup"><span data-stu-id="13521-141">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="13521-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13521-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13521-143">Personalizzazione di una barra multifunzione tramite definizioni di dimensioni e criteri di ridimensionamento</span><span class="sxs-lookup"><span data-stu-id="13521-143">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





