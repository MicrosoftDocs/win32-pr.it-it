---
title: Ribbon. QuickAccessToolbar, proprietà
description: Rappresenta un contenitore per la barra di accesso rapido (QAT).
ms.assetid: 8a873a48-4f8b-439d-acad-7da2081fbf40
keywords:
- Barra multifunzione di Windows della proprietà Ribbon. QuickAccessToolbar
topic_type:
- apiref
api_name:
- Ribbon.QuickAccessToolbar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0e09b220bd60b60ccbb8ee05c2da9c4317ba78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400264"
---
# <a name="ribbonquickaccesstoolbar-property"></a><span data-ttu-id="0627f-104">Ribbon. QuickAccessToolbar, proprietà</span><span class="sxs-lookup"><span data-stu-id="0627f-104">Ribbon.QuickAccessToolbar property</span></span>

<span data-ttu-id="0627f-105">Rappresenta un contenitore per la barra di accesso rapido (QAT).</span><span class="sxs-lookup"><span data-stu-id="0627f-105">Represents a container for the Quick Access Toolbar (QAT).</span></span>

## <a name="usage"></a><span data-ttu-id="0627f-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="0627f-106">Usage</span></span>

``` syntax
<Ribbon.QuickAccessToolbar>
  child elements
</Ribbon.QuickAccessToolbar>
```

## <a name="attributes"></a><span data-ttu-id="0627f-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="0627f-107">Attributes</span></span>

<span data-ttu-id="0627f-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="0627f-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0627f-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0627f-109">Child elements</span></span>



| <span data-ttu-id="0627f-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="0627f-110">Element</span></span>                                                                           | <span data-ttu-id="0627f-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0627f-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="0627f-112">**QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="0627f-112">**QuickAccessToolbar**</span></span>](windowsribbon-element-quickaccesstoolbar.md)<br/> | <span data-ttu-id="0627f-113">Deve verificarsi esattamente una volta</span><span class="sxs-lookup"><span data-stu-id="0627f-113">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="0627f-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="0627f-114">Parent elements</span></span>



| <span data-ttu-id="0627f-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="0627f-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="0627f-116">**Barra multifunzione**</span><span class="sxs-lookup"><span data-stu-id="0627f-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="0627f-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="0627f-117">Remarks</span></span>

<span data-ttu-id="0627f-118">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0627f-118">Required.</span></span>

<span data-ttu-id="0627f-119">Può verificarsi una o più volte per ogni [**barra multifunzione**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="0627f-119">May occur one or more times for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0627f-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="0627f-120">Examples</span></span>

<span data-ttu-id="0627f-121">Nell'esempio seguente viene illustrato il markup di base per l'elemento **Ribbon. QuickAccessToolBar** .</span><span class="sxs-lookup"><span data-stu-id="0627f-121">The following example demonstrates the basic markup for the **Ribbon.QuickAccessToolbar** element.</span></span>


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="requirements"></a><span data-ttu-id="0627f-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0627f-122">Requirements</span></span>



| <span data-ttu-id="0627f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0627f-123">Requirement</span></span> | <span data-ttu-id="0627f-124">Valore</span><span class="sxs-lookup"><span data-stu-id="0627f-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="0627f-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0627f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0627f-126">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0627f-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="0627f-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0627f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0627f-128">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0627f-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





