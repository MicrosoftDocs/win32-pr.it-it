---
title: Proprietà SplitButton. ButtonItem
description: Rappresenta un contenitore per un pulsante o interruttore che espone il comando predefinito di un pulsante di suddivisione.
ms.assetid: 3d46d606-238d-46d4-b92e-dfd759951770
keywords:
- Barra multifunzione di Windows SplitButton. ButtonItem
topic_type:
- apiref
api_name:
- SplitButton.ButtonItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bf1e1cb908ce9a86f23f75d17bf2e76797997db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475766"
---
# <a name="splitbuttonbuttonitem-property"></a><span data-ttu-id="3643c-104">Proprietà SplitButton. ButtonItem</span><span class="sxs-lookup"><span data-stu-id="3643c-104">SplitButton.ButtonItem property</span></span>

<span data-ttu-id="3643c-105">Rappresenta un contenitore per un [pulsante](windowsribbon-controls-button.md) o [interruttore](windowsribbon-controls-togglebutton.md) che espone il comando predefinito di un pulsante di [suddivisione](windowsribbon-controls-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="3643c-105">Represents a container for a [Button](windowsribbon-controls-button.md) or [Toggle Button](windowsribbon-controls-togglebutton.md) that exposes the default Command of a [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

## <a name="usage"></a><span data-ttu-id="3643c-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="3643c-106">Usage</span></span>

``` syntax
<SplitButton.ButtonItem>
  child elements
</SplitButton.ButtonItem>
```

## <a name="attributes"></a><span data-ttu-id="3643c-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="3643c-107">Attributes</span></span>

<span data-ttu-id="3643c-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="3643c-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3643c-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="3643c-109">Child elements</span></span>



| <span data-ttu-id="3643c-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="3643c-110">Element</span></span>                                                               | <span data-ttu-id="3643c-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3643c-111">Description</span></span>                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="3643c-112">**Button**</span><span class="sxs-lookup"><span data-stu-id="3643c-112">**Button**</span></span>](windowsribbon-element-button.md)<br/>             | <span data-ttu-id="3643c-113">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="3643c-113">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="3643c-114">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="3643c-114">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/> | <span data-ttu-id="3643c-115">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="3643c-115">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="3643c-116">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="3643c-116">Parent elements</span></span>



| <span data-ttu-id="3643c-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="3643c-117">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="3643c-118">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="3643c-118">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="3643c-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="3643c-119">Remarks</span></span>

<span data-ttu-id="3643c-120">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="3643c-120">Optional.</span></span>

<span data-ttu-id="3643c-121">Può essere presente al massimo una volta per ogni [**SplitButton**](windowsribbon-element-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="3643c-121">May occur at most once for each [**SplitButton**](windowsribbon-element-splitbutton.md).</span></span>

<span data-ttu-id="3643c-122">Ogni **SplitButton. ButtonItem** può contenere solo un [**pulsante**](windowsribbon-element-button.md) o un elemento figlio [**ToggleButton**](windowsribbon-element-togglebutton.md) .</span><span class="sxs-lookup"><span data-stu-id="3643c-122">Each **SplitButton.ButtonItem** can contain only one [**Button**](windowsribbon-element-button.md) or [**ToggleButton**](windowsribbon-element-togglebutton.md) child element.</span></span>

## <a name="examples"></a><span data-ttu-id="3643c-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="3643c-123">Examples</span></span>

<span data-ttu-id="3643c-124">Nell'esempio seguente viene illustrato il markup di base per il [pulsante di suddivisione](windowsribbon-controls-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="3643c-124">The following example demonstrates the basic markup for the [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

<span data-ttu-id="3643c-125">In questa sezione del codice vengono illustrate le dichiarazioni di comando [**SplitButton**](windowsribbon-element-splitbutton.md) e **SplitButton. ButtonItem** , con un [**gruppo**](windowsribbon-element-group.md) associato che funge da contenitore padre per l'elemento **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="3643c-125">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.ButtonItem** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButton** element.</span></span>


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



<span data-ttu-id="3643c-126">In questa sezione del codice vengono illustrate le dichiarazioni di controllo [**SplitButton**](windowsribbon-element-splitbutton.md) e **SplitButton. ButtonItem** .</span><span class="sxs-lookup"><span data-stu-id="3643c-126">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.ButtonItem** control declarations.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="3643c-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3643c-127">Requirements</span></span>



| <span data-ttu-id="3643c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3643c-128">Requirement</span></span> | <span data-ttu-id="3643c-129">Valore</span><span class="sxs-lookup"><span data-stu-id="3643c-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="3643c-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3643c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3643c-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3643c-131">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="3643c-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3643c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3643c-133">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3643c-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3643c-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3643c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3643c-135">Controllo pulsante combinato</span><span class="sxs-lookup"><span data-stu-id="3643c-135">Split Button control</span></span>](windowsribbon-controls-splitbutton.md)
</dt> </dl>

 

 





