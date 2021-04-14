---
title: Tab. ScalingPolicy, proprietà
description: Rappresenta un contenitore per le specifiche di ridimensionamento delle schede.
ms.assetid: cc1e4a35-9348-459b-a2f1-25c34d49e5e8
keywords:
- Tab. ScalingPolicy proprietà barra multifunzione di Windows
topic_type:
- apiref
api_name:
- Tab.ScalingPolicy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46528e7b5957415db55f1a51dd6dafed7e1da98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478605"
---
# <a name="tabscalingpolicy-property"></a><span data-ttu-id="5eeec-104">Tab. ScalingPolicy, proprietà</span><span class="sxs-lookup"><span data-stu-id="5eeec-104">Tab.ScalingPolicy property</span></span>

<span data-ttu-id="5eeec-105">Rappresenta un contenitore per le specifiche di ridimensionamento delle [schede](windowsribbon-controls-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="5eeec-105">Represents a container for [Tab](windowsribbon-controls-tab.md) scaling specifications.</span></span>

## <a name="usage"></a><span data-ttu-id="5eeec-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="5eeec-106">Usage</span></span>

``` syntax
<Tab.ScalingPolicy>
  child elements
</Tab.ScalingPolicy>
```

## <a name="attributes"></a><span data-ttu-id="5eeec-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="5eeec-107">Attributes</span></span>

<span data-ttu-id="5eeec-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="5eeec-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="5eeec-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="5eeec-109">Child elements</span></span>



| <span data-ttu-id="5eeec-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="5eeec-110">Element</span></span>                                                                 | <span data-ttu-id="5eeec-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5eeec-111">Description</span></span>                                    |
|-------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="5eeec-112">**ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="5eeec-112">**ScalingPolicy**</span></span>](windowsribbon-element-scalingpolicy.md)<br/> | <span data-ttu-id="5eeec-113">Deve verificarsi esattamente una volta</span><span class="sxs-lookup"><span data-stu-id="5eeec-113">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="5eeec-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="5eeec-114">Parent elements</span></span>



| <span data-ttu-id="5eeec-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="5eeec-115">Element</span></span>                                             |
|-----------------------------------------------------|
| [<span data-ttu-id="5eeec-116">**Scheda**</span><span class="sxs-lookup"><span data-stu-id="5eeec-116">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="5eeec-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="5eeec-117">Remarks</span></span>

<span data-ttu-id="5eeec-118">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5eeec-118">Optional.</span></span>

<span data-ttu-id="5eeec-119">Può essere presente al massimo una volta per ogni [**scheda**](windowsribbon-element-tab.md).</span><span class="sxs-lookup"><span data-stu-id="5eeec-119">May occur at most once for each [**Tab**](windowsribbon-element-tab.md).</span></span>

<span data-ttu-id="5eeec-120">Le specifiche di ridimensionamento descrivono le dimensioni e il comportamento del layout per i controlli in una [scheda](windowsribbon-controls-tab.md) quando la barra multifunzione viene ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="5eeec-120">Scaling specifications describe the size and layout behavior for the controls in a [Tab](windowsribbon-controls-tab.md) when the Ribbon is resized.</span></span>

## <a name="examples"></a><span data-ttu-id="5eeec-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="5eeec-121">Examples</span></span>

<span data-ttu-id="5eeec-122">Nell'esempio di codice seguente viene illustrato un manifesto [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) che specifica una preferenza [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) per ognuno dei quattro gruppi di controlli in una scheda **Home** . Inoltre, gli elementi di [**scala**](windowsribbon-element-scale.md) vengono specificati per influenzare il comportamento di compressione, in ordine di ridimensionamento decrescente, di ogni gruppo.</span><span class="sxs-lookup"><span data-stu-id="5eeec-122">The following code example demonstrates a [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest that specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="5eeec-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5eeec-123">Requirements</span></span>



| <span data-ttu-id="5eeec-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5eeec-124">Requirement</span></span> | <span data-ttu-id="5eeec-125">Valore</span><span class="sxs-lookup"><span data-stu-id="5eeec-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="5eeec-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5eeec-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5eeec-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5eeec-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="5eeec-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5eeec-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5eeec-129">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5eeec-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5eeec-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5eeec-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eeec-131">Personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità</span><span class="sxs-lookup"><span data-stu-id="5eeec-131">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





