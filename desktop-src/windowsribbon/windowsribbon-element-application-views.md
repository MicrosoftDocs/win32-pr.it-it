---
title: Proprietà Application. views
description: Rappresenta un contenitore per ogni visualizzazione del Framework della barra multifunzione, in particolare la barra multifunzione e l'ContextPopup.
ms.assetid: e7549b8b-0f95-477a-9024-1a99ee1412c2
keywords:
- Proprietà Application. views-barra multifunzione di Windows
topic_type:
- apiref
api_name:
- Application.Views
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e7d106d346a790ee3bd8879b2367f38341f0a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301712"
---
# <a name="applicationviews-property"></a><span data-ttu-id="d21f8-104">Proprietà Application. views</span><span class="sxs-lookup"><span data-stu-id="d21f8-104">Application.Views property</span></span>

<span data-ttu-id="d21f8-105">Rappresenta un contenitore per ogni visualizzazione del Framework della barra multifunzione, in particolare la [**barra multifunzione**](windowsribbon-element-ribbon.md) e l' [**ContextPopup**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="d21f8-105">Represents a container for each Ribbon framework View, specifically the [**Ribbon**](windowsribbon-element-ribbon.md) and the [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

## <a name="usage"></a><span data-ttu-id="d21f8-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="d21f8-106">Usage</span></span>

``` syntax
<Application.Views>
  child elements
</Application.Views>
```

## <a name="attributes"></a><span data-ttu-id="d21f8-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="d21f8-107">Attributes</span></span>

<span data-ttu-id="d21f8-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="d21f8-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d21f8-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="d21f8-109">Child elements</span></span>



| <span data-ttu-id="d21f8-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="d21f8-110">Element</span></span>                                                               | <span data-ttu-id="d21f8-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d21f8-111">Description</span></span>                                        |
|-----------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="d21f8-112">**ContextPopup**</span><span class="sxs-lookup"><span data-stu-id="d21f8-112">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)<br/> | <span data-ttu-id="d21f8-113">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="d21f8-113">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d21f8-114">**Barra multifunzione**</span><span class="sxs-lookup"><span data-stu-id="d21f8-114">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/>             | <span data-ttu-id="d21f8-115">Deve verificarsi esattamente una volta</span><span class="sxs-lookup"><span data-stu-id="d21f8-115">Must occur exactly once</span></span><br/> <br/>     |



## <a name="parent-elements"></a><span data-ttu-id="d21f8-116">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="d21f8-116">Parent elements</span></span>



| <span data-ttu-id="d21f8-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="d21f8-117">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="d21f8-118">**Applicazione**</span><span class="sxs-lookup"><span data-stu-id="d21f8-118">**Application**</span></span>](windowsribbon-element-application.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="d21f8-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="d21f8-119">Remarks</span></span>

<span data-ttu-id="d21f8-120">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d21f8-120">Required.</span></span>

<span data-ttu-id="d21f8-121">Deve essere eseguita esattamente una volta per ogni elemento [**dell'applicazione**](windowsribbon-element-application.md) .</span><span class="sxs-lookup"><span data-stu-id="d21f8-121">Must occur exactly once for each [**Application**](windowsribbon-element-application.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="d21f8-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="d21f8-122">Examples</span></span>

<span data-ttu-id="d21f8-123">Nell'esempio seguente viene illustrato un elemento **Application. views** che contiene un manifesto di controlli della barra multifunzione, ognuno con un riferimento a un comando dichiarato nell'elemento [**Application. Commands**](windowsribbon-element-application-commands.md) .</span><span class="sxs-lookup"><span data-stu-id="d21f8-123">The following example shows an **Application.Views** element that contains a manifest of Ribbon controls, each with a reference to a Command declared in the [**Application.Commands**](windowsribbon-element-application-commands.md) element.</span></span>


```C++
<Application.Views>
  <Ribbon Name="ScenicRibbonSampleApp">
    <Ribbon.Tabs>
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
    </Ribbon.Tabs>
  </Ribbon>
</Application.Views>
```



## <a name="requirements"></a><span data-ttu-id="d21f8-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d21f8-124">Requirements</span></span>



| <span data-ttu-id="d21f8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d21f8-125">Requirement</span></span> | <span data-ttu-id="d21f8-126">Valore</span><span class="sxs-lookup"><span data-stu-id="d21f8-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="d21f8-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d21f8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d21f8-128">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d21f8-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="d21f8-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d21f8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d21f8-130">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d21f8-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d21f8-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d21f8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d21f8-132">**Application. Commands**</span><span class="sxs-lookup"><span data-stu-id="d21f8-132">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)
</dt> </dl>

 

 





