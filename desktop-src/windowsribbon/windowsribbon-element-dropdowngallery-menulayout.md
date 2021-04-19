---
title: Proprietà DropDownGallery. MenuLayout
description: Rappresenta un contenitore per i layout del menu a discesa DropDownGallery.
ms.assetid: 7251e889-377d-4d7f-b049-bd81a202774d
keywords:
- Barra multifunzione di Windows DropDownGallery. MenuLayout
topic_type:
- apiref
api_name:
- DropDownGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1b6ad3f07f369dfef90b1e6c52c34793e60520
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302374"
---
# <a name="dropdowngallerymenulayout-property"></a><span data-ttu-id="5b151-104">Proprietà DropDownGallery. MenuLayout</span><span class="sxs-lookup"><span data-stu-id="5b151-104">DropDownGallery.MenuLayout property</span></span>

<span data-ttu-id="5b151-105">Rappresenta un contenitore per i layout del menu a discesa [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) .</span><span class="sxs-lookup"><span data-stu-id="5b151-105">Represents a container for [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) drop-down menu layouts.</span></span>

## <a name="usage"></a><span data-ttu-id="5b151-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="5b151-106">Usage</span></span>

``` syntax
<DropDownGallery.MenuLayout>
  child elements
</DropDownGallery.MenuLayout>
```

## <a name="attributes"></a><span data-ttu-id="5b151-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="5b151-107">Attributes</span></span>

<span data-ttu-id="5b151-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="5b151-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="5b151-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="5b151-109">Child elements</span></span>



| <span data-ttu-id="5b151-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="5b151-110">Element</span></span>                                                                           | <span data-ttu-id="5b151-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b151-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="5b151-112">**FlowMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="5b151-112">**FlowMenuLayout**</span></span>](windowsribbon-element-flowmenulayout.md)<br/>         | <span data-ttu-id="5b151-113">Deve verificarsi esattamente una volta</span><span class="sxs-lookup"><span data-stu-id="5b151-113">Must occur exactly once</span></span><br/> <br/> |
| [<span data-ttu-id="5b151-114">**VerticalMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="5b151-114">**VerticalMenuLayout**</span></span>](windowsribbon-element-verticalmenulayout.md)<br/> | <span data-ttu-id="5b151-115">Deve verificarsi esattamente una volta</span><span class="sxs-lookup"><span data-stu-id="5b151-115">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="5b151-116">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="5b151-116">Parent elements</span></span>



| <span data-ttu-id="5b151-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="5b151-117">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="5b151-118">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="5b151-118">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="5b151-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b151-119">Remarks</span></span>

<span data-ttu-id="5b151-120">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5b151-120">Optional.</span></span>

<span data-ttu-id="5b151-121">Può verificarsi al massimo una volta per ogni elemento [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) .</span><span class="sxs-lookup"><span data-stu-id="5b151-121">May occur at most once for each [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="5b151-122">È consentito un massimo di un elemento figlio ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) o [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)).</span><span class="sxs-lookup"><span data-stu-id="5b151-122">A maximum of one child element ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) is allowed.</span></span>

 

## <a name="examples"></a><span data-ttu-id="5b151-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="5b151-123">Examples</span></span>

<span data-ttu-id="5b151-124">Nell'esempio seguente viene illustrato il markup di base per [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span><span class="sxs-lookup"><span data-stu-id="5b151-124">The following example demonstrates the basic markup for the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span></span>

<span data-ttu-id="5b151-125">Questa sezione di codice mostra la dichiarazione di controllo **DropDownGallery. MenuLayout** .</span><span class="sxs-lookup"><span data-stu-id="5b151-125">This section of code shows the **DropDownGallery.MenuLayout** control declaration.</span></span>


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="5b151-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b151-126">Requirements</span></span>



| <span data-ttu-id="5b151-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b151-127">Requirement</span></span> | <span data-ttu-id="5b151-128">Valore</span><span class="sxs-lookup"><span data-stu-id="5b151-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="5b151-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b151-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5b151-130">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5b151-130">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="5b151-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b151-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5b151-132">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5b151-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5b151-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b151-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b151-134">**Controllo raccolta a discesa**</span><span class="sxs-lookup"><span data-stu-id="5b151-134">**Drop-Down Gallery control**</span></span>](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="5b151-135">Uso delle raccolte</span><span class="sxs-lookup"><span data-stu-id="5b151-135">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





