---
title: Proprietà inribbongallery. MenuGroups
description: Rappresenta un contenitore per il set di voci di menu a discesa di un controllo raccolta In-Ribbon.
ms.assetid: 6b9ded25-4e8e-4e30-a349-f7c091dbfe7a
keywords:
- Proprietà inribbongallery. MenuGroups barra multifunzione di Windows
topic_type:
- apiref
api_name:
- InRibbonGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd447b66dada74b1a9b909b3030e080198143b12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048424"
---
# <a name="inribbongallerymenugroups-property"></a><span data-ttu-id="fbd2e-104">Proprietà inribbongallery. MenuGroups</span><span class="sxs-lookup"><span data-stu-id="fbd2e-104">InRibbonGallery.MenuGroups property</span></span>

<span data-ttu-id="fbd2e-105">Rappresenta un contenitore per il set di voci di menu a discesa di un controllo [raccolta nella barra multifunzione](windowsribbon-controls-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="fbd2e-105">Represents a container for the set of drop-down menu items of an [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="fbd2e-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="fbd2e-106">Usage</span></span>

``` syntax
<InRibbonGallery.MenuGroups>
  child elements
</InRibbonGallery.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="fbd2e-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="fbd2e-107">Attributes</span></span>

<span data-ttu-id="fbd2e-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="fbd2e-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="fbd2e-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="fbd2e-109">Child elements</span></span>



| <span data-ttu-id="fbd2e-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="fbd2e-110">Element</span></span>                                                         | <span data-ttu-id="fbd2e-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fbd2e-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="fbd2e-112">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="fbd2e-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="fbd2e-113">Deve essere presente almeno una volta</span><span class="sxs-lookup"><span data-stu-id="fbd2e-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="fbd2e-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="fbd2e-114">Parent elements</span></span>



| <span data-ttu-id="fbd2e-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="fbd2e-115">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="fbd2e-116">**Inribbongallery**</span><span class="sxs-lookup"><span data-stu-id="fbd2e-116">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="fbd2e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="fbd2e-117">Remarks</span></span>

<span data-ttu-id="fbd2e-118">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fbd2e-118">Optional.</span></span>

<span data-ttu-id="fbd2e-119">Può verificarsi al massimo una volta per ogni elemento [**inribbongallery**](windowsribbon-element-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="fbd2e-119">May occur at most once for each [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="fbd2e-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="fbd2e-120">Examples</span></span>

<span data-ttu-id="fbd2e-121">Nell'esempio seguente viene illustrato il markup di base per un controllo [della raccolta della barra multifunzione](windowsribbon-controls-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="fbd2e-121">The following example demonstrates the basic markup for an [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control.</span></span>

<span data-ttu-id="fbd2e-122">Questa sezione di codice mostra la dichiarazione di controllo **inribbongallery. MenuGroups** .</span><span class="sxs-lookup"><span data-stu-id="fbd2e-122">This section of code shows the **InRibbonGallery.MenuGroups** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="fbd2e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fbd2e-123">Requirements</span></span>



| <span data-ttu-id="fbd2e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbd2e-124">Requirement</span></span> | <span data-ttu-id="fbd2e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="fbd2e-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="fbd2e-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fbd2e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fbd2e-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fbd2e-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="fbd2e-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fbd2e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fbd2e-129">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="fbd2e-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fbd2e-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fbd2e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbd2e-131">Controllo raccolta nella barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="fbd2e-131">In-Ribbon Gallery control</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="fbd2e-132">Uso delle raccolte</span><span class="sxs-lookup"><span data-stu-id="fbd2e-132">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="fbd2e-133">Personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità</span><span class="sxs-lookup"><span data-stu-id="fbd2e-133">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





