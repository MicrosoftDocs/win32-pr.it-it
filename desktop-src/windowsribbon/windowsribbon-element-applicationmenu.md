---
title: Elemento ApplicationMenu
description: Rappresenta il menu dell'applicazione. | Elemento ApplicationMenu
ms.assetid: 815e0462-ea45-44b1-81bf-f5797b22e920
keywords:
- Barra multifunzione di Windows per l'elemento ApplicationMenu
topic_type:
- apiref
api_name:
- ApplicationMenu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e535fbcc09a404ad7dd5a4019438f4513f5c77c6
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443052"
---
# <a name="applicationmenu-element"></a><span data-ttu-id="eacd9-105">Elemento ApplicationMenu</span><span class="sxs-lookup"><span data-stu-id="eacd9-105">ApplicationMenu element</span></span>

<span data-ttu-id="eacd9-106">Rappresenta il [menu dell'applicazione](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="eacd9-106">Represents the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="eacd9-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="eacd9-107">Usage</span></span>

``` syntax
<ApplicationMenu
  CommandName = "xs:positiveInteger or xs:string"
>
  child elements
</ApplicationMenu>
```

## <a name="attributes"></a><span data-ttu-id="eacd9-108">Attributi</span><span class="sxs-lookup"><span data-stu-id="eacd9-108">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eacd9-109">Attributo</span><span class="sxs-lookup"><span data-stu-id="eacd9-109">Attribute</span></span></th>
<th><span data-ttu-id="eacd9-110">Type</span><span class="sxs-lookup"><span data-stu-id="eacd9-110">Type</span></span></th>
<th><span data-ttu-id="eacd9-111">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="eacd9-111">Required</span></span></th>
<th><span data-ttu-id="eacd9-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eacd9-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eacd9-113"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="eacd9-113"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="eacd9-114">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="eacd9-114">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="eacd9-115">No</span><span class="sxs-lookup"><span data-stu-id="eacd9-115">No</span></span><br/></td>
<td><span data-ttu-id="eacd9-116">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="eacd9-116">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="eacd9-117">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="eacd9-117">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="eacd9-118">Stringa, valore intero compreso tra 2 e 59999, inclusivo o valore esadecimale compreso tra 0x2 e 0xea5f, inclusi.</span><span class="sxs-lookup"><span data-stu-id="eacd9-118">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="eacd9-119">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="eacd9-119">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="eacd9-120">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="eacd9-120">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="eacd9-121">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="eacd9-121">Child elements</span></span>



| <span data-ttu-id="eacd9-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="eacd9-122">Element</span></span>                                                                                             | <span data-ttu-id="eacd9-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eacd9-123">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="eacd9-124">**ApplicationMenu.RecentItems**</span><span class="sxs-lookup"><span data-stu-id="eacd9-124">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)<br/> | <span data-ttu-id="eacd9-125">Può verificarsi al massimo una volta</span><span class="sxs-lookup"><span data-stu-id="eacd9-125">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="eacd9-126">**Menugroup**</span><span class="sxs-lookup"><span data-stu-id="eacd9-126">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                     | <span data-ttu-id="eacd9-127">Può verificarsi una o più volte</span><span class="sxs-lookup"><span data-stu-id="eacd9-127">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="eacd9-128">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="eacd9-128">Parent elements</span></span>



| <span data-ttu-id="eacd9-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="eacd9-129">Element</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eacd9-130">**Ribbon.ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="eacd9-130">**Ribbon.ApplicationMenu**</span></span>](windowsribbon-element-ribbon-applicationmenu.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="eacd9-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="eacd9-131">Remarks</span></span>

<span data-ttu-id="eacd9-132">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="eacd9-132">Required.</span></span>

<span data-ttu-id="eacd9-133">Deve verificarsi esattamente una volta per [**ogni Ribbon.ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="eacd9-133">Must occur exactly once for each [**Ribbon.ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md).</span></span>

<span data-ttu-id="eacd9-134">Gli elementi figlio **dell'elemento ApplicationMenu** devono essere presenti nell'ordine specificato:</span><span class="sxs-lookup"><span data-stu-id="eacd9-134">The child elements of the **ApplicationMenu** element must occur in the specified order:</span></span>

1.  [<span data-ttu-id="eacd9-135">**ApplicationMenu.RecentItems**</span><span class="sxs-lookup"><span data-stu-id="eacd9-135">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)
2.  [<span data-ttu-id="eacd9-136">**Menugroup**</span><span class="sxs-lookup"><span data-stu-id="eacd9-136">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)

## <a name="examples"></a><span data-ttu-id="eacd9-137">Esempio</span><span class="sxs-lookup"><span data-stu-id="eacd9-137">Examples</span></span>

<span data-ttu-id="eacd9-138">Nell'esempio seguente viene illustrato il markup di base per [il menu dell'applicazione](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="eacd9-138">The following example demonstrates the basic markup for the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

<span data-ttu-id="eacd9-139">Questa sezione di codice illustra le **dichiarazioni del comando ApplicationMenu.**</span><span class="sxs-lookup"><span data-stu-id="eacd9-139">This section of code shows the **ApplicationMenu** Command declarations.</span></span>


```XML
<!-- Command declarations for the Application Menu. -->
<Command Name="cmdFileMenu"
         Symbol="ID_FILE_MENU"
         Id="25000" />
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
<!-- Command declarations for Application Menu items. -->
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
<Command Name="cmdPrint"
         Symbol="ID_FILE_PRINT"
         Comment="Save"
         Id="25004"
         LabelTitle="Print" />
<Command Name="cmdExit"
         Symbol="ID_FILE_EXIT"
         Comment="Exit"
         Id="25005"
         LabelTitle="Exit" />
```



<span data-ttu-id="eacd9-140">Questa sezione di codice illustra le **dichiarazioni del controllo ApplicationMenu.**</span><span class="sxs-lookup"><span data-stu-id="eacd9-140">This section of code shows the **ApplicationMenu** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="eacd9-141">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="eacd9-141">Element information</span></span>

* <span data-ttu-id="eacd9-142">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="eacd9-142">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="eacd9-143">**Può essere vuoto:** No</span><span class="sxs-lookup"><span data-stu-id="eacd9-143">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="eacd9-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eacd9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eacd9-145">Controllo Menu dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="eacd9-145">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> </dl>

 

 





