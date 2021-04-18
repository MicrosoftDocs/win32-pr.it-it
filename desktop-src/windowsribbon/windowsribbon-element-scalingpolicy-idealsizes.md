---
title: Proprietà ScalingPolicy. IdealSizes
description: Rappresenta un contenitore di specifiche di ridimensionamento per il modello SizeDefinition preferito, in base alle dimensioni della barra multifunzione.
ms.assetid: a4aa2642-160d-4d81-9df9-29277911aa5a
keywords:
- Barra multifunzione di Windows ScalingPolicy. IdealSizes
topic_type:
- apiref
api_name:
- ScalingPolicy.IdealSizes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7bf62cd0388b523f444c4a9cca226b58187212b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302306"
---
# <a name="scalingpolicyidealsizes-property"></a><span data-ttu-id="d74f0-104">Proprietà ScalingPolicy. IdealSizes</span><span class="sxs-lookup"><span data-stu-id="d74f0-104">ScalingPolicy.IdealSizes property</span></span>

<span data-ttu-id="d74f0-105">Rappresenta un contenitore di specifiche di ridimensionamento per il modello [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preferito, in base alle dimensioni della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="d74f0-105">Represents a container of scaling specifications for the preferred [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template, based on Ribbon size.</span></span>

## <a name="usage"></a><span data-ttu-id="d74f0-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="d74f0-106">Usage</span></span>

``` syntax
<ScalingPolicy.IdealSizes>
  child elements
</ScalingPolicy.IdealSizes>
```

## <a name="attributes"></a><span data-ttu-id="d74f0-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="d74f0-107">Attributes</span></span>

<span data-ttu-id="d74f0-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="d74f0-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d74f0-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="d74f0-109">Child elements</span></span>



| <span data-ttu-id="d74f0-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="d74f0-110">Element</span></span>                                                 | <span data-ttu-id="d74f0-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d74f0-111">Description</span></span>                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="d74f0-112">**Scalabilità**</span><span class="sxs-lookup"><span data-stu-id="d74f0-112">**Scale**</span></span>](windowsribbon-element-scale.md)<br/> | <span data-ttu-id="d74f0-113">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="d74f0-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="d74f0-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="d74f0-114">Parent elements</span></span>



| <span data-ttu-id="d74f0-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="d74f0-115">Element</span></span>                                                                 |
|-------------------------------------------------------------------------|
| [<span data-ttu-id="d74f0-116">**ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="d74f0-116">**ScalingPolicy**</span></span>](windowsribbon-element-scalingpolicy.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="d74f0-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="d74f0-117">Remarks</span></span>

<span data-ttu-id="d74f0-118">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d74f0-118">Optional.</span></span>

<span data-ttu-id="d74f0-119">Può essere presente al massimo una volta per ogni [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="d74f0-119">May occur at most once for each [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md).</span></span>

<span data-ttu-id="d74f0-120">Se è definito **ScalingPolicy. IdealSizes** , deve essere presente una voce di [**scala**](windowsribbon-element-scale.md) per ogni elemento di [**gruppo**](windowsribbon-element-group.md) in un elemento [**Tab**](windowsribbon-element-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="d74f0-120">If **ScalingPolicy.IdealSizes** is defined, then a [**Scale**](windowsribbon-element-scale.md) entry for each [**Group**](windowsribbon-element-group.md) element in a [**Tab**](windowsribbon-element-tab.md) element must be present.</span></span>

<span data-ttu-id="d74f0-121">**ScalingPolicy. IdealSizes** sono i layout [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preferiti per un [**gruppo**](windowsribbon-element-group.md) di controlli.</span><span class="sxs-lookup"><span data-stu-id="d74f0-121">**ScalingPolicy.IdealSizes** are the preferred [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layouts for a [**Group**](windowsribbon-element-group.md) of controls.</span></span>

## <a name="examples"></a><span data-ttu-id="d74f0-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="d74f0-122">Examples</span></span>

<span data-ttu-id="d74f0-123">Nell'esempio seguente viene illustrato come è possibile personalizzare l'aspetto dei controlli in un [**gruppo**](windowsribbon-element-group.md) tramite la funzionalità di layout adattivo dei modelli [**SizeDefinition**](windowsribbon-element-sizedefinition.md) della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="d74f0-123">The following example demonstrates how the appearance of controls in a [**Group**](windowsribbon-element-group.md) can be customized through the adaptive layout functionality of Ribbon [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span>

<span data-ttu-id="d74f0-124">Il manifesto [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) in questo esempio specifica una preferenza **ScalingPolicy. IdealSizes** [**SizeDefinition**](windowsribbon-element-sizedefinition.md) per ognuno dei quattro gruppi di controlli in una scheda **Home** . Inoltre, gli elementi di [**scala**](windowsribbon-element-scale.md) vengono specificati per influenzare il comportamento di compressione, in ordine di ridimensionamento decrescente, di ogni gruppo.</span><span class="sxs-lookup"><span data-stu-id="d74f0-124">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest in this example specifies a **ScalingPolicy.IdealSizes** [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


```C++
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



## <a name="requirements"></a><span data-ttu-id="d74f0-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d74f0-125">Requirements</span></span>



| <span data-ttu-id="d74f0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d74f0-126">Requirement</span></span> | <span data-ttu-id="d74f0-127">Valore</span><span class="sxs-lookup"><span data-stu-id="d74f0-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="d74f0-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d74f0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d74f0-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d74f0-129">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="d74f0-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d74f0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d74f0-131">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d74f0-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d74f0-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d74f0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d74f0-133">Personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità</span><span class="sxs-lookup"><span data-stu-id="d74f0-133">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





