---
title: Elemento Row
description: Rappresenta una riga di controlli in un modello di layout SizeDefinition personalizzato.
ms.assetid: c3dac35f-3537-4eb7-b378-501ea88813f5
keywords:
- Barra multifunzione di Windows dell'elemento Row
topic_type:
- apiref
api_name:
- Row
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d642cd209b3e00e2c63f7376e321132a1c0e686
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111445022"
---
# <a name="row-element"></a><span data-ttu-id="5c41e-104">Elemento Row</span><span class="sxs-lookup"><span data-stu-id="5c41e-104">Row element</span></span>

<span data-ttu-id="5c41e-105">Rappresenta una riga di controlli in un modello di layout SizeDefinition personalizzato.</span><span class="sxs-lookup"><span data-stu-id="5c41e-105">Represents a row of controls in a custom SizeDefinition layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="5c41e-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="5c41e-106">Usage</span></span>

``` syntax
<Row>
  child elements
</Row>
```

## <a name="attributes"></a><span data-ttu-id="5c41e-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="5c41e-107">Attributes</span></span>

<span data-ttu-id="5c41e-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="5c41e-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="5c41e-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="5c41e-109">Child elements</span></span>



| <span data-ttu-id="5c41e-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="5c41e-110">Element</span></span>                                                                                 | <span data-ttu-id="5c41e-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c41e-111">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="5c41e-112">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="5c41e-112">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                   | <span data-ttu-id="5c41e-113">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="5c41e-113">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="5c41e-114">**ControlSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="5c41e-114">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="5c41e-115">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="5c41e-115">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="5c41e-116">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="5c41e-116">Parent elements</span></span>



| <span data-ttu-id="5c41e-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="5c41e-117">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c41e-118">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="5c41e-118">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="5c41e-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c41e-119">Remarks</span></span>

<span data-ttu-id="5c41e-120">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5c41e-120">Optional.</span></span>

<span data-ttu-id="5c41e-121">Può verificarsi una o più volte per ogni [**elemento GroupSizeDefinition.**](windowsribbon-element-groupsizedefinition.md)</span><span class="sxs-lookup"><span data-stu-id="5c41e-121">May occur one or more times for each [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="5c41e-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="5c41e-122">Examples</span></span>

<span data-ttu-id="5c41e-123">L'esempio di codice seguente illustra il markup di base per un modello di layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) a quattro pulsanti personalizzato con vari **elementi Row.**</span><span class="sxs-lookup"><span data-stu-id="5c41e-123">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various **Row** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="5c41e-124">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5c41e-124">Element information</span></span>




* <span data-ttu-id="5c41e-125">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="5c41e-125">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="5c41e-126">**Può essere vuoto:** No</span><span class="sxs-lookup"><span data-stu-id="5c41e-126">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="5c41e-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c41e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c41e-128">Personalizzazione di una barra multifunzione tramite definizioni di dimensioni e criteri di ridimensionamento</span><span class="sxs-lookup"><span data-stu-id="5c41e-128">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





