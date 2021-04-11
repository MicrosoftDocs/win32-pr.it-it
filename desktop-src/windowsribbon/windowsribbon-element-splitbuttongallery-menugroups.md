---
title: Proprietà SplitButtonGallery. MenuGroups
description: Rappresenta un contenitore per un set di voci di menu a discesa in un controllo SplitButtonGallery.
ms.assetid: e30fcf9a-488b-423a-8bc4-fccbc78f74de
keywords:
- Barra multifunzione di Windows SplitButtonGallery. MenuGroups
topic_type:
- apiref
api_name:
- SplitButtonGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72176e7d7e79b076c3a7cf4d1fd847aa4f4e0561
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119746"
---
# <a name="splitbuttongallerymenugroups-property"></a><span data-ttu-id="ed64d-104">Proprietà SplitButtonGallery. MenuGroups</span><span class="sxs-lookup"><span data-stu-id="ed64d-104">SplitButtonGallery.MenuGroups property</span></span>

<span data-ttu-id="ed64d-105">Rappresenta un contenitore per un set di voci di menu a discesa in un controllo [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="ed64d-105">Represents a container for a set of drop-down menu items in a [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="ed64d-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="ed64d-106">Usage</span></span>

``` syntax
<SplitButtonGallery.MenuGroups>
  child elements
</SplitButtonGallery.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="ed64d-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="ed64d-107">Attributes</span></span>

<span data-ttu-id="ed64d-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="ed64d-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ed64d-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="ed64d-109">Child elements</span></span>



| <span data-ttu-id="ed64d-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="ed64d-110">Element</span></span>                                                         | <span data-ttu-id="ed64d-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed64d-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="ed64d-112">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="ed64d-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="ed64d-113">Deve essere presente almeno una volta</span><span class="sxs-lookup"><span data-stu-id="ed64d-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ed64d-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="ed64d-114">Parent elements</span></span>



| <span data-ttu-id="ed64d-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="ed64d-115">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="ed64d-116">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="ed64d-116">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ed64d-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed64d-117">Remarks</span></span>

<span data-ttu-id="ed64d-118">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ed64d-118">Required.</span></span>

<span data-ttu-id="ed64d-119">Deve essere eseguita esattamente una volta per ogni elemento [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="ed64d-119">Must occur exactly once for each [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="ed64d-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="ed64d-120">Examples</span></span>

<span data-ttu-id="ed64d-121">Nell'esempio seguente viene illustrato il markup di base per l'elemento **SplitButtonGallery. MenuGroups** .</span><span class="sxs-lookup"><span data-stu-id="ed64d-121">The following example demonstrates the basic markup for the **SplitButtonGallery.MenuGroups** element.</span></span>

<span data-ttu-id="ed64d-122">Questa sezione di codice mostra la dichiarazione di controllo **SplitButtonGallery. MenuGroups** .</span><span class="sxs-lookup"><span data-stu-id="ed64d-122">This section of code shows the **SplitButtonGallery.MenuGroups** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="ed64d-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed64d-123">Requirements</span></span>



| <span data-ttu-id="ed64d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed64d-124">Requirement</span></span> | <span data-ttu-id="ed64d-125">Valore</span><span class="sxs-lookup"><span data-stu-id="ed64d-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ed64d-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed64d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ed64d-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ed64d-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ed64d-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed64d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ed64d-129">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ed64d-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ed64d-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed64d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed64d-131">Controllo raccolta pulsanti di suddivisione</span><span class="sxs-lookup"><span data-stu-id="ed64d-131">Split Button Gallery control</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="ed64d-132">Uso delle raccolte</span><span class="sxs-lookup"><span data-stu-id="ed64d-132">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





