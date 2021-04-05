---
title: Proprietà SplitButton. MenuGroups
description: Rappresenta un contenitore per un set di voci di menu a discesa in un controllo pulsante di menu combinato standard.
ms.assetid: 6328ad49-037b-4cd5-90f6-b91646e260ee
keywords:
- Barra multifunzione di Windows SplitButton. MenuGroups
topic_type:
- apiref
api_name:
- SplitButton.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b8af4639040d6b6302b4d2b5761d750074389a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741463"
---
# <a name="splitbuttonmenugroups-property"></a><span data-ttu-id="a9063-104">Proprietà SplitButton. MenuGroups</span><span class="sxs-lookup"><span data-stu-id="a9063-104">SplitButton.MenuGroups property</span></span>

<span data-ttu-id="a9063-105">Rappresenta un contenitore per un set di voci di menu a discesa in un controllo [pulsante](windowsribbon-controls-splitbutton.md) di menu combinato standard.</span><span class="sxs-lookup"><span data-stu-id="a9063-105">Represents a container for a set of drop-down menu items in a standard [Split Button](windowsribbon-controls-splitbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="a9063-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="a9063-106">Usage</span></span>

``` syntax
<SplitButton.MenuGroups>
  child elements
</SplitButton.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="a9063-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="a9063-107">Attributes</span></span>

<span data-ttu-id="a9063-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="a9063-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a9063-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a9063-109">Child elements</span></span>



| <span data-ttu-id="a9063-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="a9063-110">Element</span></span>                                                         | <span data-ttu-id="a9063-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9063-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="a9063-112">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="a9063-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="a9063-113">Deve essere presente almeno una volta</span><span class="sxs-lookup"><span data-stu-id="a9063-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="a9063-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="a9063-114">Parent elements</span></span>



| <span data-ttu-id="a9063-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="a9063-115">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="a9063-116">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="a9063-116">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a9063-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9063-117">Remarks</span></span>

<span data-ttu-id="a9063-118">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a9063-118">Optional.</span></span>

<span data-ttu-id="a9063-119">Può essere presente al massimo una volta per ogni [**SplitButton**](windowsribbon-element-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="a9063-119">May occur at most once for each [**SplitButton**](windowsribbon-element-splitbutton.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a9063-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="a9063-120">Examples</span></span>

<span data-ttu-id="a9063-121">Nell'esempio seguente viene illustrato il markup di base per il [pulsante di suddivisione](windowsribbon-controls-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="a9063-121">The following example demonstrates the basic markup for the [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

<span data-ttu-id="a9063-122">In questa sezione del codice vengono illustrate le dichiarazioni di comando [**SplitButton**](windowsribbon-element-splitbutton.md) e **SplitButton. MenuGroups** , con un [**gruppo**](windowsribbon-element-group.md) associato che funge da contenitore padre per l'elemento **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="a9063-122">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.MenuGroups** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButton** element.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



<span data-ttu-id="a9063-123">In questa sezione del codice vengono illustrate le dichiarazioni di controllo [**SplitButton**](windowsribbon-element-splitbutton.md) e **SplitButton. MenuGroups** .</span><span class="sxs-lookup"><span data-stu-id="a9063-123">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.MenuGroups** control declarations.</span></span>


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="a9063-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9063-124">Requirements</span></span>



| <span data-ttu-id="a9063-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9063-125">Requirement</span></span> | <span data-ttu-id="a9063-126">Valore</span><span class="sxs-lookup"><span data-stu-id="a9063-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="a9063-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9063-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a9063-128">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a9063-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="a9063-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9063-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a9063-130">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a9063-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a9063-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9063-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9063-132">Controllo pulsante combinato</span><span class="sxs-lookup"><span data-stu-id="a9063-132">Split Button control</span></span>](windowsribbon-controls-splitbutton.md)
</dt> </dl>

 

 





