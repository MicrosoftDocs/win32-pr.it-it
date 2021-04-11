---
title: Elemento ControlNameDefinition
description: Rappresenta il nome di un controllo in un modello di layout SizeDefinition personalizzato.
ms.assetid: 94b724bd-a4e3-40e0-9cf0-3cc6a71100d2
keywords:
- Barra multifunzione Windows elemento ControlNameDefinition
topic_type:
- apiref
api_name:
- ControlNameDefinition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14ec269ce51b0074b9a03f78aea218b482955d1b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334180"
---
# <a name="controlnamedefinition-element"></a><span data-ttu-id="31604-104">Elemento ControlNameDefinition</span><span class="sxs-lookup"><span data-stu-id="31604-104">ControlNameDefinition element</span></span>

<span data-ttu-id="31604-105">Rappresenta il nome di un controllo in un modello di layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) personalizzato.</span><span class="sxs-lookup"><span data-stu-id="31604-105">Represents a name of a control in a custom [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="31604-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="31604-106">Usage</span></span>

``` syntax
<ControlNameDefinition
  Name = "xs:positiveInteger or xs:string">
  child elements
</ControlNameDefinition>
```

## <a name="attributes"></a><span data-ttu-id="31604-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="31604-107">Attributes</span></span>



| <span data-ttu-id="31604-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="31604-108">Attribute</span></span>           | <span data-ttu-id="31604-109">Type</span><span class="sxs-lookup"><span data-stu-id="31604-109">Type</span></span>                                       | <span data-ttu-id="31604-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="31604-110">Required</span></span>      | <span data-ttu-id="31604-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31604-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------|--------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31604-112">**Nome**</span><span class="sxs-lookup"><span data-stu-id="31604-112">**Name**</span></span><br/> | <span data-ttu-id="31604-113">XS: positiveInteger o xs: String</span><span class="sxs-lookup"><span data-stu-id="31604-113">xs:positiveInteger or xs:string</span></span><br/> | <span data-ttu-id="31604-114">No</span><span class="sxs-lookup"><span data-stu-id="31604-114">No</span></span><br/> | <span data-ttu-id="31604-115"><dt> (XS: positiveInteger o xs: String)</span><span class="sxs-lookup"><span data-stu-id="31604-115"><dt> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="31604-116">Stringa, valore intero compreso tra 2 e 59999, inclusivo o un valore esadecimale compreso tra 0x2 e 0xea5f, inclusi.</span><span class="sxs-lookup"><span data-stu-id="31604-116">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="31604-117">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="31604-117">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="31604-118">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="31604-118">Maximum length: 100 characters.</span></span> <br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="31604-119">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="31604-119">Child elements</span></span>



| <span data-ttu-id="31604-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="31604-120">Element</span></span>                              | <span data-ttu-id="31604-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31604-121">Description</span></span>                                        |
|--------------------------------------|----------------------------------------------------|
| <span data-ttu-id="31604-122">**ControlNameDefinition**</span><span class="sxs-lookup"><span data-stu-id="31604-122">**ControlNameDefinition**</span></span><br/> | <span data-ttu-id="31604-123">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="31604-123">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="31604-124">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="31604-124">Parent elements</span></span>



| <span data-ttu-id="31604-125">Elemento</span><span class="sxs-lookup"><span data-stu-id="31604-125">Element</span></span>                                                                   |
|---------------------------------------------------------------------------|
| [<span data-ttu-id="31604-126">**ControlNameMap**</span><span class="sxs-lookup"><span data-stu-id="31604-126">**ControlNameMap**</span></span>](windowsribbon-element-controlnamemap.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="31604-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="31604-127">Remarks</span></span>

<span data-ttu-id="31604-128">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="31604-128">Optional.</span></span>

<span data-ttu-id="31604-129">Può essere presente una o più volte per ogni elemento [**ControlNameMap**](windowsribbon-element-controlnamemap.md) .</span><span class="sxs-lookup"><span data-stu-id="31604-129">May occur one or more times for each [**ControlNameMap**](windowsribbon-element-controlnamemap.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="31604-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="31604-130">Examples</span></span>

<span data-ttu-id="31604-131">Nell'esempio di codice seguente viene illustrato il markup di base per un modello di layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) personalizzato a quattro pulsanti con quattro elementi **ControlNameDefinition** .</span><span class="sxs-lookup"><span data-stu-id="31604-131">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with four **ControlNameDefinition** elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="31604-132">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="31604-132">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="31604-133">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31604-133">Minimum supported system</span></span><br/> | <span data-ttu-id="31604-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="31604-134">Windows 7</span></span> |
| <span data-ttu-id="31604-135">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="31604-135">Can be empty</span></span>                        | <span data-ttu-id="31604-136">No</span><span class="sxs-lookup"><span data-stu-id="31604-136">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="31604-137">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="31604-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31604-138">Personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità</span><span class="sxs-lookup"><span data-stu-id="31604-138">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





