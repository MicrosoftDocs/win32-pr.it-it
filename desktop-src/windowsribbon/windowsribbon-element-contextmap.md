---
title: Elemento ContextMap
description: Rappresenta un mapping di coppia ContextMenu e MiniToolbar.
ms.assetid: 84379578-24c6-4bf7-8dcf-8e21e5665d29
keywords:
- Elemento ContextMap Nella barra multifunzione di Windows
topic_type:
- apiref
api_name:
- ContextMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4754fc75ca09e39cdc7eabbeae2a0a2d2630c31f
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443012"
---
# <a name="contextmap-element"></a><span data-ttu-id="bb3bf-104">Elemento ContextMap</span><span class="sxs-lookup"><span data-stu-id="bb3bf-104">ContextMap element</span></span>

<span data-ttu-id="bb3bf-105">Rappresenta un mapping [**di coppia ContextMenu**](windowsribbon-element-contextmenu.md) [**e MiniToolbar.**](windowsribbon-element-minitoolbar.md)</span><span class="sxs-lookup"><span data-stu-id="bb3bf-105">Represents a [**ContextMenu**](windowsribbon-element-contextmenu.md) and [**MiniToolbar**](windowsribbon-element-minitoolbar.md) pair mapping.</span></span>

## <a name="usage"></a><span data-ttu-id="bb3bf-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="bb3bf-106">Usage</span></span>

``` syntax
<ContextMap
  CommandName = "xs:positiveInteger or xs:string"
  MiniToolbar = "xs:string"
  ContextMenu = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="bb3bf-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="bb3bf-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bb3bf-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="bb3bf-108">Attribute</span></span></th>
<th><span data-ttu-id="bb3bf-109">Type</span><span class="sxs-lookup"><span data-stu-id="bb3bf-109">Type</span></span></th>
<th><span data-ttu-id="bb3bf-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="bb3bf-110">Required</span></span></th>
<th><span data-ttu-id="bb3bf-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb3bf-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bb3bf-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="bb3bf-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="bb3bf-113">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="bb3bf-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="bb3bf-114">No</span><span class="sxs-lookup"><span data-stu-id="bb3bf-114">No</span></span><br/></td>
<td><span data-ttu-id="bb3bf-115">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command.</strong></a></span><span class="sxs-lookup"><span data-stu-id="bb3bf-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="bb3bf-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="bb3bf-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="bb3bf-117">Stringa, valore intero compreso tra 2 e 59999 inclusi o valore esadecimale compreso tra 0x2 e 0xea5f inclusi.</span><span class="sxs-lookup"><span data-stu-id="bb3bf-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="bb3bf-118">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="bb3bf-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="bb3bf-119">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="bb3bf-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb3bf-120"><strong>ContextMenu</strong></span><span class="sxs-lookup"><span data-stu-id="bb3bf-120"><strong>ContextMenu</strong></span></span><br/></td>
<td><span data-ttu-id="bb3bf-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="bb3bf-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="bb3bf-122">No</span><span class="sxs-lookup"><span data-stu-id="bb3bf-122">No</span></span><br/></td>
<td><span data-ttu-id="bb3bf-123">Deve corrispondere a un nome <a href="windowsribbon-element-contextmenu.md"><strong>ContextMenu</strong></a> <em>esistente.</em></span><span class="sxs-lookup"><span data-stu-id="bb3bf-123">Must correspond to an existing <a href="windowsribbon-element-contextmenu.md"><strong>ContextMenu</strong></a> <em>Name</em>.</span></span><br/> <br/><span data-ttu-id="bb3bf-124">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="bb3bf-124">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="bb3bf-125">Stringa composta da qualsiasi sequenza di caratteri, inclusi spazi vuoti e caratteri di interruzione di riga.</span><span class="sxs-lookup"><span data-stu-id="bb3bf-125">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bb3bf-126"><strong>MiniToolbar</strong></span><span class="sxs-lookup"><span data-stu-id="bb3bf-126"><strong>MiniToolbar</strong></span></span><br/></td>
<td><span data-ttu-id="bb3bf-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="bb3bf-127">xs:string</span></span><br/></td>
<td><span data-ttu-id="bb3bf-128">No</span><span class="sxs-lookup"><span data-stu-id="bb3bf-128">No</span></span><br/></td>
<td><span data-ttu-id="bb3bf-129">Deve corrispondere a un nome <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a> <em>esistente.</em></span><span class="sxs-lookup"><span data-stu-id="bb3bf-129">Must correspond to an existing <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a> <em>Name</em>.</span></span><br/> <br/><span data-ttu-id="bb3bf-130">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="bb3bf-130">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="bb3bf-131">Stringa composta da qualsiasi sequenza di caratteri, inclusi spazi vuoti e caratteri di interruzione di riga.</span><span class="sxs-lookup"><span data-stu-id="bb3bf-131">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="bb3bf-132">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="bb3bf-132">Child elements</span></span>

<span data-ttu-id="bb3bf-133">Non ci sono elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="bb3bf-133">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="bb3bf-134">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="bb3bf-134">Parent elements</span></span>



| <span data-ttu-id="bb3bf-135">Elemento</span><span class="sxs-lookup"><span data-stu-id="bb3bf-135">Element</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bb3bf-136">**ContextPopup.ContextMaps**</span><span class="sxs-lookup"><span data-stu-id="bb3bf-136">**ContextPopup.ContextMaps**</span></span>](windowsribbon-element-contextpopup-contextmaps.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="bb3bf-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb3bf-137">Remarks</span></span>

<span data-ttu-id="bb3bf-138">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bb3bf-138">Optional.</span></span>

<span data-ttu-id="bb3bf-139">Può verificarsi una o più volte per [**ogni ContextPopup.ContextMaps**](windowsribbon-element-contextpopup-contextmaps.md).</span><span class="sxs-lookup"><span data-stu-id="bb3bf-139">May occur one or more times for each [**ContextPopup.ContextMaps**](windowsribbon-element-contextpopup-contextmaps.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bb3bf-140">Esempio</span><span class="sxs-lookup"><span data-stu-id="bb3bf-140">Examples</span></span>

<span data-ttu-id="bb3bf-141">L'esempio seguente illustra il markup di base per [**una visualizzazione ContextPopup.**](windowsribbon-element-contextpopup.md)</span><span class="sxs-lookup"><span data-stu-id="bb3bf-141">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="bb3bf-142">Questa sezione di codice illustra un set di **dichiarazioni di controllo ContextMap.**</span><span class="sxs-lookup"><span data-stu-id="bb3bf-142">This section of code shows a set of **ContextMap** control declarations.</span></span>


```XML
    <ContextPopup>
      <!--
        The MiniToolbars and Context Menus are the basic ingredients for 
        the contextual UI popup. 
        Mix-and-match and associate each combination with a ContextMap Command 
        invoked in code.
      -->
      <ContextPopup.MiniToolbars>
        <MiniToolbar Name="MiniToolbar1">
          <MenuGroup Class="MajorItems">
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
            <DropDownButton CommandName="cmdButtons">
              <MenuGroup>
                <Button CommandName="cmdButton1" />
                <Button CommandName="cmdButton2" />
                <Button CommandName="cmdButton3" />
              </MenuGroup>
            </DropDownButton>
          </MenuGroup>
        </MiniToolbar>
        <MiniToolbar Name="MiniToolbar2">
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </MiniToolbar>
      </ContextPopup.MiniToolbars>
      <ContextPopup.ContextMenus>
        <ContextMenu Name="ContextMenu1">
          <MenuGroup>
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
        </ContextMenu>
        <ContextMenu Name="ContextMenu2">
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </ContextMenu>
        <ContextMenu Name="ContextMenu4">
          <MenuGroup>
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </ContextMenu>
      </ContextPopup.ContextMenus>
      <ContextPopup.ContextMaps>
        <ContextMap CommandName="cmdContextMap1"
                    ContextMenu="ContextMenu1"/>
        <ContextMap CommandName="cmdContextMap2"
                    ContextMenu="ContextMenu2"
                    MiniToolbar="MiniToolbar1"/>
        <ContextMap CommandName="cmdContextMap3"
                    MiniToolbar="MiniToolbar2"/>
        <ContextMap CommandName="cmdContextMap4"
                    ContextMenu="ContextMenu4"/>
      </ContextPopup.ContextMaps>
    </ContextPopup>
```



## <a name="element-information"></a><span data-ttu-id="bb3bf-143">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="bb3bf-143">Element information</span></span>


* <span data-ttu-id="bb3bf-144">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="bb3bf-144">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="bb3bf-145">**Può essere vuoto:** Sì</span><span class="sxs-lookup"><span data-stu-id="bb3bf-145">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="bb3bf-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb3bf-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb3bf-147">Controllo Popup del contesto</span><span class="sxs-lookup"><span data-stu-id="bb3bf-147">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





