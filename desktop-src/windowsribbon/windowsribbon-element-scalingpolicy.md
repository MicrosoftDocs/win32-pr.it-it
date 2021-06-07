---
title: Elemento ScalingPolicy
description: Rappresenta un contenitore per le specifiche di ridimensionamento.
ms.assetid: 133e7994-9901-43e8-82b0-3d910cf8758e
keywords:
- Elemento ScalingPolicy barra multifunzione di Windows
topic_type:
- apiref
api_name:
- ScalingPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 812256b0ff329073eb516c6ab2eb7501db8de40d
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444992"
---
# <a name="scalingpolicy-element"></a><span data-ttu-id="94c60-104">Elemento ScalingPolicy</span><span class="sxs-lookup"><span data-stu-id="94c60-104">ScalingPolicy element</span></span>

<span data-ttu-id="94c60-105">Rappresenta un contenitore per le specifiche di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="94c60-105">Represents a container for scaling specifications.</span></span>

## <a name="usage"></a><span data-ttu-id="94c60-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="94c60-106">Usage</span></span>

``` syntax
<ScalingPolicy>
  child elements
</ScalingPolicy>
```

## <a name="attributes"></a><span data-ttu-id="94c60-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="94c60-107">Attributes</span></span>

<span data-ttu-id="94c60-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="94c60-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="94c60-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="94c60-109">Child elements</span></span>



| <span data-ttu-id="94c60-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="94c60-110">Element</span></span>                                                                                       | <span data-ttu-id="94c60-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94c60-111">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="94c60-112">**Scalabilità**</span><span class="sxs-lookup"><span data-stu-id="94c60-112">**Scale**</span></span>](windowsribbon-element-scale.md)<br/>                                       | <span data-ttu-id="94c60-113">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="94c60-113">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="94c60-114">**ScalingPolicy.IdealSizes**</span><span class="sxs-lookup"><span data-stu-id="94c60-114">**ScalingPolicy.IdealSizes**</span></span>](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> | <span data-ttu-id="94c60-115">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="94c60-115">May occur at most once</span></span><br/> <br/>      |



## <a name="parent-elements"></a><span data-ttu-id="94c60-116">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="94c60-116">Parent elements</span></span>



| <span data-ttu-id="94c60-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="94c60-117">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="94c60-118">**Tab.ScalingPolicy**</span><span class="sxs-lookup"><span data-stu-id="94c60-118">**Tab.ScalingPolicy**</span></span>](windowsribbon-element-tab-scalingpolicy.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="94c60-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="94c60-119">Remarks</span></span>

<span data-ttu-id="94c60-120">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="94c60-120">Required.</span></span>

<span data-ttu-id="94c60-121">Deve verificarsi una sola volta per [**ogni Tab.ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="94c60-121">Must occur once for each [**Tab.ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md).</span></span>

<span data-ttu-id="94c60-122">**L'elemento ScalingPolicy** contiene un manifesto di [**dichiarazioni ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) e [**Scale**](windowsribbon-element-scale.md) che specificano le preferenze di layout adattive per uno o più elementi [**Group**](windowsribbon-element-group.md) quando la barra multifunzione viene ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="94c60-122">The **ScalingPolicy** element contains a manifest of [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) and [**Scale**](windowsribbon-element-scale.md) declarations that specify adaptive layout preferences for one or more [**Group**](windowsribbon-element-group.md) elements when the Ribbon is resized.</span></span>

<span data-ttu-id="94c60-123">L'elenco [**di dichiarazioni Scale**](windowsribbon-element-scale.md) deve essere in ordine decrescente di dimensioni valide (Large, Medium, Small, Popup) per l'elemento [**SizeDefinition**](windowsribbon-element-sizedefinition.md) associato all'elemento [**Group.**](windowsribbon-element-group.md)</span><span class="sxs-lookup"><span data-stu-id="94c60-123">The list of [**Scale**](windowsribbon-element-scale.md) declarations must be in descending order of valid sizes (Large, Medium, Small, Popup) for the [**SizeDefinition**](windowsribbon-element-sizedefinition.md) associated with the [**Group**](windowsribbon-element-group.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="94c60-124">È consigliabile che siano specificati dettagli adeguati dei criteri di ridimensionamento in modo che una barra multifunzione sia in grado di eseguire il rendering senza barre di scorrimento quando viene ridimensionata a una larghezza di 300 pixel a 96 punti per pollice (dpi).</span><span class="sxs-lookup"><span data-stu-id="94c60-124">It is highly recommended that adequate scaling policy detail be specified such that a Ribbon is able to render without scroll bars when resized to a width of 300 pixels at 96 dots per inch (dpi).</span></span>

 

## <a name="examples"></a><span data-ttu-id="94c60-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="94c60-125">Examples</span></span>

<span data-ttu-id="94c60-126">L'esempio seguente illustra come personalizzare l'aspetto dei controlli in [**un**](windowsribbon-element-group.md) gruppo tramite la funzionalità di layout adattivo dei modelli [**SizeDefinition della**](windowsribbon-element-sizedefinition.md) barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="94c60-126">The following example demonstrates how the appearance of controls in a [**Group**](windowsribbon-element-group.md) can be customized through the adaptive layout functionality of Ribbon [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span>

<span data-ttu-id="94c60-127">Il **manifesto ScalingPolicy** in questo esempio specifica una preferenza [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) per ognuno dei quattro gruppi di controlli in una **scheda** Home. Inoltre, gli [**elementi Scale**](windowsribbon-element-scale.md) vengono specificati per influire sul comportamento di compressione, in ordine decrescente, di ogni gruppo.</span><span class="sxs-lookup"><span data-stu-id="94c60-127">The **ScalingPolicy** manifest in this example specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="94c60-128">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="94c60-128">Element information</span></span>

- <span data-ttu-id="94c60-129">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="94c60-129">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="94c60-130">**Può essere vuoto:** No</span><span class="sxs-lookup"><span data-stu-id="94c60-130">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="94c60-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94c60-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94c60-132">Personalizzazione di una barra multifunzione tramite definizioni delle dimensioni e criteri di ridimensionamento</span><span class="sxs-lookup"><span data-stu-id="94c60-132">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





