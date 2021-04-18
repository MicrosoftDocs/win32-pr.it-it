---
title: Elemento ColumnBreak
description: Rappresenta un separatore verticale (visibile o nascosto) nei modelli di layout SizeDefinition personalizzati.
ms.assetid: 5979d3e6-366b-4c47-810f-90fb8039af8d
keywords:
- Barra multifunzione Windows elemento ColumnBreak
topic_type:
- apiref
api_name:
- ColumnBreak
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 00257783c0c8a7919251004a4b1996ab4d994c3c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299201"
---
# <a name="columnbreak-element"></a><span data-ttu-id="dad55-104">Elemento ColumnBreak</span><span class="sxs-lookup"><span data-stu-id="dad55-104">ColumnBreak element</span></span>

<span data-ttu-id="dad55-105">Rappresenta un separatore verticale (visibile o nascosto) nei modelli di layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) personalizzati.</span><span class="sxs-lookup"><span data-stu-id="dad55-105">Represents a vertical separator (visible or hidden) in custom [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout templates.</span></span>

## <a name="usage"></a><span data-ttu-id="dad55-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="dad55-106">Usage</span></span>

``` syntax
<ColumnBreak
  ShowSeparator = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="dad55-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="dad55-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dad55-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="dad55-108">Attribute</span></span></th>
<th><span data-ttu-id="dad55-109">Type</span><span class="sxs-lookup"><span data-stu-id="dad55-109">Type</span></span></th>
<th><span data-ttu-id="dad55-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="dad55-110">Required</span></span></th>
<th><span data-ttu-id="dad55-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dad55-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dad55-112"><strong>ShowSeparator</strong></span><span class="sxs-lookup"><span data-stu-id="dad55-112"><strong>ShowSeparator</strong></span></span><br/></td>
<td><span data-ttu-id="dad55-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="dad55-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="dad55-114">No</span><span class="sxs-lookup"><span data-stu-id="dad55-114">No</span></span><br/></td>
<td><span data-ttu-id="dad55-115">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="dad55-115">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="dad55-116">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="dad55-116">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="dad55-117">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="dad55-117">Default.</span></span> <br/> </dd> <span data-ttu-id="dad55-118"><dt><span></span><span></span><strong></strong> false</span><span class="sxs-lookup"><span data-stu-id="dad55-118"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="dad55-119">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="dad55-119">Child elements</span></span>

<span data-ttu-id="dad55-120">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="dad55-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="dad55-121">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="dad55-121">Parent elements</span></span>



| <span data-ttu-id="dad55-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="dad55-122">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="dad55-123">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="dad55-123">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="dad55-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="dad55-124">Remarks</span></span>

<span data-ttu-id="dad55-125">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="dad55-125">Optional.</span></span>

<span data-ttu-id="dad55-126">Può essere presente una o più volte per ogni elemento [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="dad55-126">May occur one or more times for each [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="dad55-127">Esempio</span><span class="sxs-lookup"><span data-stu-id="dad55-127">Examples</span></span>

<span data-ttu-id="dad55-128">Nell'esempio seguente viene illustrato il markup di base per un elemento **ColumnBreak** in un modello personalizzato di layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) a quattro pulsanti.</span><span class="sxs-lookup"><span data-stu-id="dad55-128">The following example demonstrates the basic markup for a **ColumnBreak** element in a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span> <span data-ttu-id="dad55-129">**ColumnBreak** viene specificato solo per il `Large` modello.</span><span class="sxs-lookup"><span data-stu-id="dad55-129">The **ColumnBreak** is only specified for the `Large` template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="dad55-130">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="dad55-130">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="dad55-131">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dad55-131">Minimum supported system</span></span><br/> | <span data-ttu-id="dad55-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dad55-132">Windows 7</span></span> |
| <span data-ttu-id="dad55-133">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="dad55-133">Can be empty</span></span>                        | <span data-ttu-id="dad55-134">Sì</span><span class="sxs-lookup"><span data-stu-id="dad55-134">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="dad55-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dad55-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dad55-136">Personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità</span><span class="sxs-lookup"><span data-stu-id="dad55-136">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





