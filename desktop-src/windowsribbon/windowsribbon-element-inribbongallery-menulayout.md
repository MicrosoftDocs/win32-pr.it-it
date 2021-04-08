---
title: Proprietà inribbongallery. MenuLayout
description: Rappresenta un contenitore per i layout del menu a discesa della raccolta In-Ribbon.
ms.assetid: 89e0eb39-2790-4571-a661-ab3ebafbb13f
keywords:
- Proprietà inribbongallery. MenuLayout barra multifunzione di Windows
topic_type:
- apiref
api_name:
- InRibbonGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2fc5e0eab5d8dbc35cd9cb3be96e5d5d351416
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047948"
---
# <a name="inribbongallerymenulayout-property"></a><span data-ttu-id="3fab5-104">Proprietà inribbongallery. MenuLayout</span><span class="sxs-lookup"><span data-stu-id="3fab5-104">InRibbonGallery.MenuLayout property</span></span>

<span data-ttu-id="3fab5-105">Rappresenta un contenitore per i layout [del menu a discesa della raccolta della barra multifunzione](windowsribbon-controls-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="3fab5-105">Represents a container for [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) drop-down menu layouts.</span></span>

## <a name="usage"></a><span data-ttu-id="3fab5-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="3fab5-106">Usage</span></span>

``` syntax
<InRibbonGallery.MenuLayout>
  child elements
</InRibbonGallery.MenuLayout>
```

## <a name="attributes"></a><span data-ttu-id="3fab5-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="3fab5-107">Attributes</span></span>

<span data-ttu-id="3fab5-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="3fab5-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3fab5-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="3fab5-109">Child elements</span></span>



| <span data-ttu-id="3fab5-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="3fab5-110">Element</span></span>                                                                           | <span data-ttu-id="3fab5-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3fab5-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="3fab5-112">**FlowMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="3fab5-112">**FlowMenuLayout**</span></span>](windowsribbon-element-flowmenulayout.md)<br/>         | <span data-ttu-id="3fab5-113">Deve verificarsi esattamente una volta</span><span class="sxs-lookup"><span data-stu-id="3fab5-113">Must occur exactly once</span></span><br/> <br/> |
| [<span data-ttu-id="3fab5-114">**VerticalMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="3fab5-114">**VerticalMenuLayout**</span></span>](windowsribbon-element-verticalmenulayout.md)<br/> | <span data-ttu-id="3fab5-115">Deve verificarsi esattamente una volta</span><span class="sxs-lookup"><span data-stu-id="3fab5-115">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="3fab5-116">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="3fab5-116">Parent elements</span></span>



| <span data-ttu-id="3fab5-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="3fab5-117">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="3fab5-118">**Inribbongallery**</span><span class="sxs-lookup"><span data-stu-id="3fab5-118">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="3fab5-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="3fab5-119">Remarks</span></span>

<span data-ttu-id="3fab5-120">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="3fab5-120">Optional.</span></span>

<span data-ttu-id="3fab5-121">Può verificarsi al massimo una volta per ogni elemento [**inribbongallery**](windowsribbon-element-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="3fab5-121">May occur at most once for each [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="3fab5-122">È consentito un massimo di un elemento figlio ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) o [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)).</span><span class="sxs-lookup"><span data-stu-id="3fab5-122">A maximum of one child element ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) is allowed.</span></span>

 

## <a name="examples"></a><span data-ttu-id="3fab5-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="3fab5-123">Examples</span></span>

<span data-ttu-id="3fab5-124">Nell'esempio seguente viene illustrato il markup di base per la [raccolta della barra multifunzione](windowsribbon-controls-inribbongallery.md).</span><span class="sxs-lookup"><span data-stu-id="3fab5-124">The following example demonstrates the basic markup for the [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md).</span></span>

<span data-ttu-id="3fab5-125">Questa sezione di codice mostra la dichiarazione di controllo **inribbongallery. MenuLayout** .</span><span class="sxs-lookup"><span data-stu-id="3fab5-125">This section of code shows the **InRibbonGallery.MenuLayout** control declaration.</span></span>


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="3fab5-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fab5-126">Requirements</span></span>



| <span data-ttu-id="3fab5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fab5-127">Requirement</span></span> | <span data-ttu-id="3fab5-128">Valore</span><span class="sxs-lookup"><span data-stu-id="3fab5-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="3fab5-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fab5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3fab5-130">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3fab5-130">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="3fab5-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fab5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3fab5-132">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3fab5-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3fab5-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3fab5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fab5-134">Controllo raccolta nella barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="3fab5-134">In-Ribbon Gallery control</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="3fab5-135">Uso delle raccolte</span><span class="sxs-lookup"><span data-stu-id="3fab5-135">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





