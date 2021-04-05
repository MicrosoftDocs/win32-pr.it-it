---
title: Elemento RecentItems
description: Rappresenta il controllo degli elementi recenti nel menu dell'applicazione.
ms.assetid: a3df0bb0-e0f8-413a-879d-8e39164535d0
keywords:
- Barra multifunzione Windows elemento RecentItems
topic_type:
- apiref
api_name:
- RecentItems
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17269342521a5da5db8d7a852a985c29ed7e2e98
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "104046251"
---
# <a name="recentitems-element"></a><span data-ttu-id="098a8-104">Elemento RecentItems</span><span class="sxs-lookup"><span data-stu-id="098a8-104">RecentItems element</span></span>

<span data-ttu-id="098a8-105">Rappresenta il controllo [degli elementi recenti](windowsribbon-controls-recentitems.md) nel [menu dell'applicazione](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="098a8-105">Represents the [Recent Items](windowsribbon-controls-recentitems.md) control in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="098a8-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="098a8-106">Usage</span></span>

``` syntax
<RecentItems
  CommandName = "xs:positiveInteger or xs:string"
  MaxCount = "xs:nonNegativeInteger"
  EnablePinning = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="098a8-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="098a8-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="098a8-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="098a8-108">Attribute</span></span></th>
<th><span data-ttu-id="098a8-109">Type</span><span class="sxs-lookup"><span data-stu-id="098a8-109">Type</span></span></th>
<th><span data-ttu-id="098a8-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="098a8-110">Required</span></span></th>
<th><span data-ttu-id="098a8-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="098a8-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="098a8-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="098a8-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="098a8-113">XS: positiveInteger o xs: String</span><span class="sxs-lookup"><span data-stu-id="098a8-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="098a8-114">No</span><span class="sxs-lookup"><span data-stu-id="098a8-114">No</span></span><br/></td>
<td><span data-ttu-id="098a8-115">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="098a8-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="098a8-116">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o xs: String)</span><span class="sxs-lookup"><span data-stu-id="098a8-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="098a8-117">Stringa, valore intero compreso tra 2 e 59999, inclusivo o un valore esadecimale compreso tra 0x2 e 0xea5f, inclusi.</span><span class="sxs-lookup"><span data-stu-id="098a8-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="098a8-118">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="098a8-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="098a8-119">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="098a8-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="098a8-120"><strong>EnablePinning</strong></span><span class="sxs-lookup"><span data-stu-id="098a8-120"><strong>EnablePinning</strong></span></span><br/></td>
<td><span data-ttu-id="098a8-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="098a8-121">Boolean</span></span><br/></td>
<td><span data-ttu-id="098a8-122">No</span><span class="sxs-lookup"><span data-stu-id="098a8-122">No</span></span><br/></td>
<td><span data-ttu-id="098a8-123">Limitato a uno dei valori seguenti (0 e 1 non sono validi):</span><span class="sxs-lookup"><span data-stu-id="098a8-123">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="098a8-124">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="098a8-124">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="098a8-125">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="098a8-125">Default.</span></span> <br/> </dd> <span data-ttu-id="098a8-126"><dt><span></span><span></span><strong></strong> false</span><span class="sxs-lookup"><span data-stu-id="098a8-126"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="098a8-127"><strong>MaxCount</strong></span><span class="sxs-lookup"><span data-stu-id="098a8-127"><strong>MaxCount</strong></span></span><br/></td>
<td><span data-ttu-id="098a8-128">xs:nonNegativeInteger</span><span class="sxs-lookup"><span data-stu-id="098a8-128">xs:nonNegativeInteger</span></span><br/></td>
<td><span data-ttu-id="098a8-129">No</span><span class="sxs-lookup"><span data-stu-id="098a8-129">No</span></span><br/></td>
<td><span data-ttu-id="098a8-130">Numero di elementi recenti da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="098a8-130">The number of recent items to display.</span></span><br/> <br/><span data-ttu-id="098a8-131">
<dt><span></span><span></span><strong></strong> (XS: nonNegativeInteger)</span><span class="sxs-lookup"><span data-stu-id="098a8-131">
<dt><span></span><span></span><strong></strong> (xs:nonNegativeInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="098a8-132">Valore intero pari a 0 o superiore.</span><span class="sxs-lookup"><span data-stu-id="098a8-132">An integer value of 0 or greater.</span></span><br/> <span data-ttu-id="098a8-133">Il valore predefinito è <strong>10</strong>.</span><span class="sxs-lookup"><span data-stu-id="098a8-133">Default is <strong>10</strong>.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="098a8-134">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="098a8-134">Child elements</span></span>

<span data-ttu-id="098a8-135">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="098a8-135">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="098a8-136">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="098a8-136">Parent elements</span></span>



| <span data-ttu-id="098a8-137">Elemento</span><span class="sxs-lookup"><span data-stu-id="098a8-137">Element</span></span>                                                                                             |
|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="098a8-138">**ApplicationMenu. RecentItems**</span><span class="sxs-lookup"><span data-stu-id="098a8-138">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="098a8-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="098a8-139">Remarks</span></span>

<span data-ttu-id="098a8-140">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="098a8-140">Required.</span></span>

<span data-ttu-id="098a8-141">Deve essere eseguita esattamente una volta per ogni elemento [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="098a8-141">Must occur exactly once for each [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) element.</span></span>

<span data-ttu-id="098a8-142">Il controllo [elementi recenti](windowsribbon-controls-recentitems.md) consente di visualizzare l'elenco degli elementi usati di recente (MRU) dell'applicazione della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="098a8-142">The [Recent Items](windowsribbon-controls-recentitems.md) control displays the most recently used (MRU) items list of the Ribbon application.</span></span>

## <a name="examples"></a><span data-ttu-id="098a8-143">Esempio</span><span class="sxs-lookup"><span data-stu-id="098a8-143">Examples</span></span>

<span data-ttu-id="098a8-144">Nell'esempio seguente viene illustrato il markup di base per il controllo [degli elementi recenti](windowsribbon-controls-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="098a8-144">The following example demonstrates the basic markup for the [Recent Items](windowsribbon-controls-recentitems.md) control.</span></span>

<span data-ttu-id="098a8-145">Nell'esempio seguente viene illustrata una dichiarazione di comando **RecentItems** .</span><span class="sxs-lookup"><span data-stu-id="098a8-145">The following example shows a **RecentItems** Command declaration.</span></span>


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



<span data-ttu-id="098a8-146">Nell'esempio seguente viene illustrata la dichiarazione di controlli **RecentItems** associati.</span><span class="sxs-lookup"><span data-stu-id="098a8-146">The following example shows the associated **RecentItems** controls declaration.</span></span>


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="element-information"></a><span data-ttu-id="098a8-147">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="098a8-147">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="098a8-148">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="098a8-148">Minimum supported system</span></span><br/> | <span data-ttu-id="098a8-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="098a8-149">Windows 7</span></span> |
| <span data-ttu-id="098a8-150">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="098a8-150">Can be empty</span></span>                        | <span data-ttu-id="098a8-151">Sì</span><span class="sxs-lookup"><span data-stu-id="098a8-151">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="098a8-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="098a8-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="098a8-153">Controllo menu applicazione</span><span class="sxs-lookup"><span data-stu-id="098a8-153">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[<span data-ttu-id="098a8-154">Controllo elementi recenti</span><span class="sxs-lookup"><span data-stu-id="098a8-154">Recent Items control</span></span>](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





