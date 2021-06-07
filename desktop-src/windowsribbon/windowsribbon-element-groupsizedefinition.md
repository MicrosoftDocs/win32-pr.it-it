---
title: Elemento GroupSizeDefinition
description: Rappresenta una dimensione di layout per un gruppo di controlli in un modello personalizzato.
ms.assetid: c0e20c80-16af-41d5-81e1-0dc32e92e3fa
keywords:
- Elemento GroupSizeDefinition nella barra multifunzione di Windows
topic_type:
- apiref
api_name:
- GroupSizeDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 650301a29ace2c6df9316a315d4cdbad448e5573
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443382"
---
# <a name="groupsizedefinition-element"></a><span data-ttu-id="43ef5-104">Elemento GroupSizeDefinition</span><span class="sxs-lookup"><span data-stu-id="43ef5-104">GroupSizeDefinition element</span></span>

<span data-ttu-id="43ef5-105">Rappresenta una dimensione di layout per un gruppo di controlli in un modello personalizzato.</span><span class="sxs-lookup"><span data-stu-id="43ef5-105">Represents a layout size for a group of controls in a custom template.</span></span>

## <a name="usage"></a><span data-ttu-id="43ef5-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="43ef5-106">Usage</span></span>

``` syntax
<GroupSizeDefinition
  Size = "xs:string">
  child elements
</GroupSizeDefinition>
```

## <a name="attributes"></a><span data-ttu-id="43ef5-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="43ef5-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="43ef5-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="43ef5-108">Attribute</span></span></th>
<th><span data-ttu-id="43ef5-109">Type</span><span class="sxs-lookup"><span data-stu-id="43ef5-109">Type</span></span></th>
<th><span data-ttu-id="43ef5-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="43ef5-110">Required</span></span></th>
<th><span data-ttu-id="43ef5-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43ef5-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="43ef5-112"><strong>Dimensioni</strong></span><span class="sxs-lookup"><span data-stu-id="43ef5-112"><strong>Size</strong></span></span><br/></td>
<td><span data-ttu-id="43ef5-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="43ef5-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="43ef5-114">No</span><span class="sxs-lookup"><span data-stu-id="43ef5-114">No</span></span><br/></td>
<td><span data-ttu-id="43ef5-115">Limitato a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="43ef5-115">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="43ef5-116">
<dt><span></span><span></span><strong></strong> (Grande)</span><span class="sxs-lookup"><span data-stu-id="43ef5-116">
<dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="43ef5-117">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="43ef5-117">Default.</span></span> <br/> </dd> <span data-ttu-id="43ef5-118"><dt><span></span><span></span><strong></strong> (Media)</span><span class="sxs-lookup"><span data-stu-id="43ef5-118"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="43ef5-119"><dt><span></span><span></span><strong></strong> (Small)</span><span class="sxs-lookup"><span data-stu-id="43ef5-119"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="43ef5-120">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="43ef5-120">Child elements</span></span>



| <span data-ttu-id="43ef5-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="43ef5-121">Element</span></span>                                                                                 | <span data-ttu-id="43ef5-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43ef5-122">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="43ef5-123">**Interruzione di colonna**</span><span class="sxs-lookup"><span data-stu-id="43ef5-123">**ColumnBreak**</span></span>](windowsribbon-element-columnbreak.md)<br/>                     | <span data-ttu-id="43ef5-124">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="43ef5-124">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="43ef5-125">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="43ef5-125">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                   | <span data-ttu-id="43ef5-126">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="43ef5-126">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="43ef5-127">**ControlSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="43ef5-127">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="43ef5-128">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="43ef5-128">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="43ef5-129">**Riga**</span><span class="sxs-lookup"><span data-stu-id="43ef5-129">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                     | <span data-ttu-id="43ef5-130">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="43ef5-130">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="43ef5-131">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="43ef5-131">Parent elements</span></span>



| <span data-ttu-id="43ef5-132">Elemento</span><span class="sxs-lookup"><span data-stu-id="43ef5-132">Element</span></span>                                                                   |
|---------------------------------------------------------------------------|
| [<span data-ttu-id="43ef5-133">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="43ef5-133">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="43ef5-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="43ef5-134">Remarks</span></span>

<span data-ttu-id="43ef5-135">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="43ef5-135">Optional.</span></span>

<span data-ttu-id="43ef5-136">Può verificarsi fino a tre volte per ogni [**elemento SizeDefinition**](windowsribbon-element-sizedefinition.md) (una volta per ogni *size).*</span><span class="sxs-lookup"><span data-stu-id="43ef5-136">May occur up to three times for each [**SizeDefinition**](windowsribbon-element-sizedefinition.md) element (one time for each *Size*).</span></span>

## <a name="examples"></a><span data-ttu-id="43ef5-137">Esempio</span><span class="sxs-lookup"><span data-stu-id="43ef5-137">Examples</span></span>

<span data-ttu-id="43ef5-138">L'esempio di codice seguente illustra un modello personalizzato di base che include le tre dimensioni del layout di gruppo che devono essere definite con **l'elemento GroupSizeDefinition** durante la creazione di un modello personalizzato.</span><span class="sxs-lookup"><span data-stu-id="43ef5-138">The following code example illustrates a basic custom template that includes the three group layout sizes that must be defined with the **GroupSizeDefinition** element when creating a custom template.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="43ef5-139">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="43ef5-139">Element information</span></span>

* <span data-ttu-id="43ef5-140">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="43ef5-140">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="43ef5-141">**Può essere vuoto:** No</span><span class="sxs-lookup"><span data-stu-id="43ef5-141">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="43ef5-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43ef5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43ef5-143">Personalizzazione di una barra multifunzione tramite definizioni delle dimensioni e criteri di ridimensionamento</span><span class="sxs-lookup"><span data-stu-id="43ef5-143">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





