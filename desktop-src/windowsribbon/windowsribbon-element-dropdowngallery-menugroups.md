---
title: Proprietà DropDownGallery. MenuGroups
description: Rappresenta un contenitore per un set di voci di menu a discesa in un controllo raccolta Drop-Down.
ms.assetid: 594f6ae5-760e-456d-98cd-04ecae0bae99
keywords:
- Barra multifunzione di Windows DropDownGallery. MenuGroups
topic_type:
- apiref
api_name:
- DropDownGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67fcaeb81020cf4c317bf065c25a770d2a77e21f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302375"
---
# <a name="dropdowngallerymenugroups-property"></a><span data-ttu-id="f5ba4-104">Proprietà DropDownGallery. MenuGroups</span><span class="sxs-lookup"><span data-stu-id="f5ba4-104">DropDownGallery.MenuGroups property</span></span>

<span data-ttu-id="f5ba4-105">Rappresenta un contenitore per un set di voci di menu a discesa in un controllo [raccolta a discesa](windowsribbon-controls-dropdowngallery.md) .</span><span class="sxs-lookup"><span data-stu-id="f5ba4-105">Represents a container for a set of drop-down menu items in a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="f5ba4-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="f5ba4-106">Usage</span></span>

``` syntax
<DropDownGallery.MenuGroups>
  child elements
</DropDownGallery.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="f5ba4-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="f5ba4-107">Attributes</span></span>

<span data-ttu-id="f5ba4-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="f5ba4-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f5ba4-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f5ba4-109">Child elements</span></span>



| <span data-ttu-id="f5ba4-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="f5ba4-110">Element</span></span>                                                         | <span data-ttu-id="f5ba4-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5ba4-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="f5ba4-112">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="f5ba4-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="f5ba4-113">Deve essere presente almeno una volta</span><span class="sxs-lookup"><span data-stu-id="f5ba4-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="f5ba4-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="f5ba4-114">Parent elements</span></span>



| <span data-ttu-id="f5ba4-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="f5ba4-115">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="f5ba4-116">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="f5ba4-116">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="f5ba4-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5ba4-117">Remarks</span></span>

<span data-ttu-id="f5ba4-118">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f5ba4-118">Required.</span></span>

<span data-ttu-id="f5ba4-119">Deve essere eseguita esattamente una volta per ogni elemento [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) .</span><span class="sxs-lookup"><span data-stu-id="f5ba4-119">Must occur exactly once for each [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="f5ba4-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="f5ba4-120">Examples</span></span>

<span data-ttu-id="f5ba4-121">Nell'esempio seguente viene illustrato il markup di base per l'elemento **DropDownGallery. MenuGroups** .</span><span class="sxs-lookup"><span data-stu-id="f5ba4-121">The following example demonstrates the basic markup for the **DropDownGallery.MenuGroups** element.</span></span>

<span data-ttu-id="f5ba4-122">Questa sezione di codice mostra la dichiarazione di controllo **DropDownGallery. MenuGroups** in uno spazio dei comandi della [raccolta a discesa](windowsribbon-controls-dropdowngallery.md) .</span><span class="sxs-lookup"><span data-stu-id="f5ba4-122">This section of code shows the **DropDownGallery.MenuGroups** control declaration in a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) Command Space.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="f5ba4-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5ba4-123">Requirements</span></span>



| <span data-ttu-id="f5ba4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5ba4-124">Requirement</span></span> | <span data-ttu-id="f5ba4-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f5ba4-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="f5ba4-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5ba4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f5ba4-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f5ba4-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f5ba4-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5ba4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f5ba4-129">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f5ba4-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f5ba4-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5ba4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5ba4-131">**Controllo raccolta a discesa**</span><span class="sxs-lookup"><span data-stu-id="f5ba4-131">**Drop-Down Gallery control**</span></span>](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="f5ba4-132">Uso delle raccolte</span><span class="sxs-lookup"><span data-stu-id="f5ba4-132">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





