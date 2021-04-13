---
title: Proprietà Ribbon. Tabs
description: Rappresenta un contenitore per tutte le schede principali in una barra multifunzione.
ms.assetid: b43d0544-c110-4785-85d7-935842b8f03e
keywords:
- Barra multifunzione di Windows della proprietà Ribbon. Tabs
topic_type:
- apiref
api_name:
- Ribbon.Tabs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4300a2385b6ada64e05e16671802460930cc2a7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475418"
---
# <a name="ribbontabs-property"></a><span data-ttu-id="42360-104">Proprietà Ribbon. Tabs</span><span class="sxs-lookup"><span data-stu-id="42360-104">Ribbon.Tabs property</span></span>

<span data-ttu-id="42360-105">Rappresenta un contenitore per tutte le schede principali in una barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="42360-105">Represents a container for all core tabs in a Ribbon.</span></span>

## <a name="usage"></a><span data-ttu-id="42360-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="42360-106">Usage</span></span>

``` syntax
<Ribbon.Tabs>
  child elements
</Ribbon.Tabs>
```

## <a name="attributes"></a><span data-ttu-id="42360-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="42360-107">Attributes</span></span>

<span data-ttu-id="42360-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="42360-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="42360-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="42360-109">Child elements</span></span>



| <span data-ttu-id="42360-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="42360-110">Element</span></span>                                             | <span data-ttu-id="42360-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42360-111">Description</span></span>                                     |
|-----------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="42360-112">**Scheda**</span><span class="sxs-lookup"><span data-stu-id="42360-112">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> | <span data-ttu-id="42360-113">Deve essere presente almeno una volta</span><span class="sxs-lookup"><span data-stu-id="42360-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="42360-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="42360-114">Parent elements</span></span>



| <span data-ttu-id="42360-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="42360-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="42360-116">**Barra multifunzione**</span><span class="sxs-lookup"><span data-stu-id="42360-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="42360-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="42360-117">Remarks</span></span>

<span data-ttu-id="42360-118">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="42360-118">Required.</span></span>

<span data-ttu-id="42360-119">Può verificarsi una o più volte per ogni [**barra multifunzione**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="42360-119">May occur one or more times for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="42360-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="42360-120">Examples</span></span>

<span data-ttu-id="42360-121">Nell'esempio seguente viene illustrato il markup di base per un elemento **Ribbon. Tabs** con una dichiarazione di [**scheda**](windowsribbon-element-tab.md) **Home** .</span><span class="sxs-lookup"><span data-stu-id="42360-121">The following example demonstrates the basic markup for a **Ribbon.Tabs** element with a **Home** [**Tab**](windowsribbon-element-tab.md) declaration.</span></span>


```C++
<Ribbon Name="ScenicRibbonSampleApp">
  <Ribbon.QuickAccessToolbar>
  ...
  </Ribbon.QuickAccessToolbar>
  <Ribbon.ApplicationMenu>
  ...
  </Ribbon.ApplicationMenu>
  <Ribbon.SizeDefinitions>
  ...
  </Ribbon.SizeDefinitions>
  <Ribbon.Tabs>
  ...
```




```C++
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```




```C++
  ...
  </Ribbon.Tabs>
  <Ribbon.ContextualTabs>
  ...
  </Ribbon.ContextualTabs>
  <Ribbon.HelpButton>
  ...
  </Ribbon.HelpButton>
</Ribbon>
```



## <a name="requirements"></a><span data-ttu-id="42360-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42360-122">Requirements</span></span>



| <span data-ttu-id="42360-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="42360-123">Requirement</span></span> | <span data-ttu-id="42360-124">Valore</span><span class="sxs-lookup"><span data-stu-id="42360-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="42360-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42360-125">Minimum supported client</span></span><br/> | <span data-ttu-id="42360-126">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="42360-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="42360-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42360-127">Minimum supported server</span></span><br/> | <span data-ttu-id="42360-128">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="42360-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="42360-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42360-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42360-130">**Ribbon. ContextualTabs**</span><span class="sxs-lookup"><span data-stu-id="42360-130">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)
</dt> </dl>

 

 





