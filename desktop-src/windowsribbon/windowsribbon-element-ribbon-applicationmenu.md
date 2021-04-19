---
title: Ribbon. ApplicationMenu, proprietà
description: Rappresenta il menu dell'applicazione. | Ribbon. ApplicationMenu, proprietà
ms.assetid: 6945e976-8ac8-40fa-8e71-31812871b496
keywords:
- Barra multifunzione di Windows della proprietà Ribbon. ApplicationMenu
topic_type:
- apiref
api_name:
- Ribbon.ApplicationMenu
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71263a19057d3f66747b1a40aaa2d0a46528e9b6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321966"
---
# <a name="ribbonapplicationmenu-property"></a><span data-ttu-id="20d63-105">Ribbon. ApplicationMenu, proprietà</span><span class="sxs-lookup"><span data-stu-id="20d63-105">Ribbon.ApplicationMenu property</span></span>

<span data-ttu-id="20d63-106">Rappresenta il menu dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="20d63-106">Represents the Application Menu.</span></span>

## <a name="usage"></a><span data-ttu-id="20d63-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="20d63-107">Usage</span></span>

``` syntax
<Ribbon.ApplicationMenu>
  child elements
</Ribbon.ApplicationMenu>
```

## <a name="attributes"></a><span data-ttu-id="20d63-108">Attributi</span><span class="sxs-lookup"><span data-stu-id="20d63-108">Attributes</span></span>

<span data-ttu-id="20d63-109">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="20d63-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="20d63-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="20d63-110">Child elements</span></span>



| <span data-ttu-id="20d63-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="20d63-111">Element</span></span>                                                                     | <span data-ttu-id="20d63-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20d63-112">Description</span></span>                                    |
|-----------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="20d63-113">**ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="20d63-113">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md)<br/> | <span data-ttu-id="20d63-114">Deve verificarsi esattamente una volta</span><span class="sxs-lookup"><span data-stu-id="20d63-114">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="20d63-115">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="20d63-115">Parent elements</span></span>



| <span data-ttu-id="20d63-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="20d63-116">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="20d63-117">**Barra multifunzione**</span><span class="sxs-lookup"><span data-stu-id="20d63-117">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="20d63-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="20d63-118">Remarks</span></span>

<span data-ttu-id="20d63-119">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="20d63-119">Required.</span></span>

<span data-ttu-id="20d63-120">Può essere presente al massimo una volta per ogni [**barra multifunzione**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="20d63-120">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="20d63-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="20d63-121">Examples</span></span>

<span data-ttu-id="20d63-122">Nell'esempio seguente viene illustrato il markup di base per l'elemento **Ribbon. ApplicationMenu** .</span><span class="sxs-lookup"><span data-stu-id="20d63-122">The following example demonstrates the basic markup for the **Ribbon.ApplicationMenu** element.</span></span>

<span data-ttu-id="20d63-123">Questa sezione di codice mostra la dichiarazione di controllo **Ribbon. ApplicationMenu** .</span><span class="sxs-lookup"><span data-stu-id="20d63-123">This section of code shows the **Ribbon.ApplicationMenu** control declaration.</span></span>


```XML
<!-- Control declarations for Application Menu items. -->
<Ribbon.ApplicationMenu>
  <ApplicationMenu CommandName="cmdFileMenu">
    <!-- Most recently used items collection. -->
    <ApplicationMenu.RecentItems>
      <RecentItems CommandName="cmdMRUItems"/>
    </ApplicationMenu.RecentItems>
    <!-- Menu items collection. -->
    <MenuGroup>
      <Button CommandName="cmdNew" />
      <Button CommandName="cmdOpen" />
      <Button CommandName="cmdSave" />
    </MenuGroup>
    <MenuGroup>
      <Button CommandName="cmdPrint" />
      <Button CommandName="cmdExit" />
    </MenuGroup>
  </ApplicationMenu>
</Ribbon.ApplicationMenu>
```



## <a name="requirements"></a><span data-ttu-id="20d63-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20d63-124">Requirements</span></span>



| <span data-ttu-id="20d63-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="20d63-125">Requirement</span></span> | <span data-ttu-id="20d63-126">Valore</span><span class="sxs-lookup"><span data-stu-id="20d63-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="20d63-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20d63-127">Minimum supported client</span></span><br/> | <span data-ttu-id="20d63-128">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="20d63-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="20d63-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20d63-129">Minimum supported server</span></span><br/> | <span data-ttu-id="20d63-130">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="20d63-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





