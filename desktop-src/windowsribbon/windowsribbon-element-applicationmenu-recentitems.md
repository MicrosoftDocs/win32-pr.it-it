---
title: Proprietà ApplicationMenu. RecentItems
description: Rappresenta un contenitore per il controllo degli elementi recenti nel menu dell'applicazione.
ms.assetid: 26ed38b6-17de-423f-a113-ccbaf3780a91
keywords:
- Barra multifunzione di Windows ApplicationMenu. RecentItems
topic_type:
- apiref
api_name:
- ApplicationMenu.RecentItems
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 473ab6436eabd7fcbbbfb533a8ae4afc07098c81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400659"
---
# <a name="applicationmenurecentitems-property"></a><span data-ttu-id="95ea5-104">Proprietà ApplicationMenu. RecentItems</span><span class="sxs-lookup"><span data-stu-id="95ea5-104">ApplicationMenu.RecentItems property</span></span>

<span data-ttu-id="95ea5-105">Rappresenta un contenitore per il controllo [degli elementi recenti](windowsribbon-controls-recentitems.md) nel [menu dell'applicazione](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="95ea5-105">Represents a container for the [Recent Items](windowsribbon-controls-recentitems.md) control in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="95ea5-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="95ea5-106">Usage</span></span>

``` syntax
<ApplicationMenu.RecentItems
  CommandName = "xs:positiveInteger or xs:string"
>
  child elements
</ApplicationMenu.RecentItems>
```

## <a name="attributes"></a><span data-ttu-id="95ea5-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="95ea5-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="95ea5-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="95ea5-108">Attribute</span></span></th>
<th><span data-ttu-id="95ea5-109">Type</span><span class="sxs-lookup"><span data-stu-id="95ea5-109">Type</span></span></th>
<th><span data-ttu-id="95ea5-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="95ea5-110">Required</span></span></th>
<th><span data-ttu-id="95ea5-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95ea5-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="95ea5-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="95ea5-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="95ea5-113">XS: positiveInteger o xs: String</span><span class="sxs-lookup"><span data-stu-id="95ea5-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="95ea5-114">No</span><span class="sxs-lookup"><span data-stu-id="95ea5-114">No</span></span><br/></td>
<td><span data-ttu-id="95ea5-115">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="95ea5-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="95ea5-116">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o xs: String)</span><span class="sxs-lookup"><span data-stu-id="95ea5-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="95ea5-117">Stringa, valore intero compreso tra 2 e 59999, inclusivo o un valore esadecimale compreso tra 0x2 e 0xea5f, inclusi.</span><span class="sxs-lookup"><span data-stu-id="95ea5-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="95ea5-118">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="95ea5-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="95ea5-119">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="95ea5-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="95ea5-120">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="95ea5-120">Child elements</span></span>



| <span data-ttu-id="95ea5-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="95ea5-121">Element</span></span>                                                             | <span data-ttu-id="95ea5-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95ea5-122">Description</span></span>                                    |
|---------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="95ea5-123">**RecentItems**</span><span class="sxs-lookup"><span data-stu-id="95ea5-123">**RecentItems**</span></span>](windowsribbon-element-recentitems.md)<br/> | <span data-ttu-id="95ea5-124">Deve verificarsi esattamente una volta</span><span class="sxs-lookup"><span data-stu-id="95ea5-124">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="95ea5-125">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="95ea5-125">Parent elements</span></span>



| <span data-ttu-id="95ea5-126">Elemento</span><span class="sxs-lookup"><span data-stu-id="95ea5-126">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="95ea5-127">**ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="95ea5-127">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="95ea5-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="95ea5-128">Remarks</span></span>

<span data-ttu-id="95ea5-129">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="95ea5-129">Optional.</span></span>

<span data-ttu-id="95ea5-130">Può verificarsi al massimo una volta per ogni elemento [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) .</span><span class="sxs-lookup"><span data-stu-id="95ea5-130">May occur at most once for each [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) element.</span></span>

<span data-ttu-id="95ea5-131">Il controllo [elementi recenti](windowsribbon-controls-recentitems.md) consente di visualizzare l'elenco degli elementi usati di recente (MRU) dell'applicazione della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="95ea5-131">The [Recent Items](windowsribbon-controls-recentitems.md) control displays the most recently used (MRU) items list of the Ribbon application.</span></span>

## <a name="examples"></a><span data-ttu-id="95ea5-132">Esempio</span><span class="sxs-lookup"><span data-stu-id="95ea5-132">Examples</span></span>

<span data-ttu-id="95ea5-133">Nell'esempio seguente viene illustrato il markup di base per il controllo [degli elementi recenti](windowsribbon-controls-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="95ea5-133">The following example demonstrates the basic markup for the [Recent Items](windowsribbon-controls-recentitems.md) control.</span></span>

<span data-ttu-id="95ea5-134">Nell'esempio seguente viene illustrata una dichiarazione di comando [**RecentItems**](windowsribbon-element-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="95ea5-134">The following example shows a [**RecentItems**](windowsribbon-element-recentitems.md) Command declaration.</span></span>


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



<span data-ttu-id="95ea5-135">Nell'esempio seguente viene illustrata la Dichiarazione **ApplicationMenu. RecentItems** e [**RecentItems**](windowsribbon-element-recentitems.md) Controls associata.</span><span class="sxs-lookup"><span data-stu-id="95ea5-135">The following example shows the associated **ApplicationMenu.RecentItems** and [**RecentItems**](windowsribbon-element-recentitems.md) controls declaration.</span></span>


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="requirements"></a><span data-ttu-id="95ea5-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95ea5-136">Requirements</span></span>



| <span data-ttu-id="95ea5-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="95ea5-137">Requirement</span></span> | <span data-ttu-id="95ea5-138">Valore</span><span class="sxs-lookup"><span data-stu-id="95ea5-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="95ea5-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95ea5-139">Minimum supported client</span></span><br/> | <span data-ttu-id="95ea5-140">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="95ea5-140">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="95ea5-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95ea5-141">Minimum supported server</span></span><br/> | <span data-ttu-id="95ea5-142">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="95ea5-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="95ea5-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="95ea5-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95ea5-144">Controllo menu applicazione</span><span class="sxs-lookup"><span data-stu-id="95ea5-144">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[<span data-ttu-id="95ea5-145">Controllo elementi recenti</span><span class="sxs-lookup"><span data-stu-id="95ea5-145">Recent Items control</span></span>](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





