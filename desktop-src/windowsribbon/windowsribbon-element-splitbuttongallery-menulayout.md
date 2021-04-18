---
title: Proprietà SplitButtonGallery. MenuLayout
description: Rappresenta un contenitore per i layout del menu a discesa della raccolta dei pulsanti di menu combinato.
ms.assetid: 4bebdff6-16ea-4cf3-adc7-9b86ea200e81
keywords:
- Barra multifunzione di Windows SplitButtonGallery. MenuLayout
topic_type:
- apiref
api_name:
- SplitButtonGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04428c14b5e47795da47e5c03970610cd08a6e8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301188"
---
# <a name="splitbuttongallerymenulayout-property"></a><span data-ttu-id="fd506-104">Proprietà SplitButtonGallery. MenuLayout</span><span class="sxs-lookup"><span data-stu-id="fd506-104">SplitButtonGallery.MenuLayout property</span></span>

<span data-ttu-id="fd506-105">Rappresenta un contenitore per i layout del menu a discesa della [raccolta dei pulsanti](windowsribbon-controls-splitbuttongallery.md) di menu combinato.</span><span class="sxs-lookup"><span data-stu-id="fd506-105">Represents a container for [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) drop-down menu layouts.</span></span>

## <a name="usage"></a><span data-ttu-id="fd506-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="fd506-106">Usage</span></span>

``` syntax
<SplitButtonGallery.MenuLayout>
  child elements
</SplitButtonGallery.MenuLayout>
```

## <a name="attributes"></a><span data-ttu-id="fd506-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="fd506-107">Attributes</span></span>

<span data-ttu-id="fd506-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="fd506-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="fd506-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="fd506-109">Child elements</span></span>



| <span data-ttu-id="fd506-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="fd506-110">Element</span></span>                                                                           | <span data-ttu-id="fd506-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd506-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="fd506-112">**FlowMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="fd506-112">**FlowMenuLayout**</span></span>](windowsribbon-element-flowmenulayout.md)<br/>         | <span data-ttu-id="fd506-113">Deve verificarsi esattamente una volta</span><span class="sxs-lookup"><span data-stu-id="fd506-113">Must occur exactly once</span></span><br/> <br/> |
| [<span data-ttu-id="fd506-114">**VerticalMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="fd506-114">**VerticalMenuLayout**</span></span>](windowsribbon-element-verticalmenulayout.md)<br/> | <span data-ttu-id="fd506-115">Deve verificarsi esattamente una volta</span><span class="sxs-lookup"><span data-stu-id="fd506-115">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="fd506-116">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="fd506-116">Parent elements</span></span>



| <span data-ttu-id="fd506-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="fd506-117">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="fd506-118">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="fd506-118">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="fd506-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd506-119">Remarks</span></span>

<span data-ttu-id="fd506-120">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fd506-120">Optional.</span></span>

<span data-ttu-id="fd506-121">Può verificarsi al massimo una volta per ogni elemento [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="fd506-121">May occur at most once for each [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="fd506-122">È consentito un massimo di un elemento figlio ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) o [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)).</span><span class="sxs-lookup"><span data-stu-id="fd506-122">A maximum of one child element ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) is allowed.</span></span>

 

## <a name="examples"></a><span data-ttu-id="fd506-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="fd506-123">Examples</span></span>

<span data-ttu-id="fd506-124">Nell'esempio seguente viene illustrato il markup di base per la [raccolta dei pulsanti di suddivisione](windowsribbon-controls-splitbuttongallery.md).</span><span class="sxs-lookup"><span data-stu-id="fd506-124">The following example demonstrates the basic markup for the [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md).</span></span>

<span data-ttu-id="fd506-125">Questa sezione di codice mostra la dichiarazione di controllo **SplitButtonGallery. MenuLayout** .</span><span class="sxs-lookup"><span data-stu-id="fd506-125">This section of code shows the **SplitButtonGallery.MenuLayout** control declaration.</span></span>


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="fd506-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd506-126">Requirements</span></span>



| <span data-ttu-id="fd506-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd506-127">Requirement</span></span> | <span data-ttu-id="fd506-128">Valore</span><span class="sxs-lookup"><span data-stu-id="fd506-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="fd506-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd506-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fd506-130">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fd506-130">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="fd506-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd506-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fd506-132">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="fd506-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fd506-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd506-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd506-134">Controllo raccolta pulsanti di suddivisione</span><span class="sxs-lookup"><span data-stu-id="fd506-134">Split Button Gallery control</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="fd506-135">Uso delle raccolte</span><span class="sxs-lookup"><span data-stu-id="fd506-135">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





