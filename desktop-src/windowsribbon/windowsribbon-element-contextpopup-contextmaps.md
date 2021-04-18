---
title: Proprietà ContextPopup. ContextMaps
description: Rappresenta un contenitore per gli elementi ContextMap.
ms.assetid: 06dfd4ba-a1d8-48bb-b185-d265e007a820
keywords:
- Barra multifunzione di Windows ContextPopup. ContextMaps
topic_type:
- apiref
api_name:
- ContextPopup.ContextMaps
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 034381c4af840219ff1d6dd4d7a73aa34f528915
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302307"
---
# <a name="contextpopupcontextmaps-property"></a><span data-ttu-id="54498-104">Proprietà ContextPopup. ContextMaps</span><span class="sxs-lookup"><span data-stu-id="54498-104">ContextPopup.ContextMaps property</span></span>

<span data-ttu-id="54498-105">Rappresenta un contenitore per gli elementi [**ContextMap**](windowsribbon-element-contextmap.md) .</span><span class="sxs-lookup"><span data-stu-id="54498-105">Represents a container for [**ContextMap**](windowsribbon-element-contextmap.md) elements.</span></span>

## <a name="usage"></a><span data-ttu-id="54498-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="54498-106">Usage</span></span>

``` syntax
<ContextPopup.ContextMaps>
  child elements
</ContextPopup.ContextMaps>
```

## <a name="attributes"></a><span data-ttu-id="54498-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="54498-107">Attributes</span></span>

<span data-ttu-id="54498-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="54498-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="54498-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="54498-109">Child elements</span></span>



| <span data-ttu-id="54498-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="54498-110">Element</span></span>                                                           | <span data-ttu-id="54498-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54498-111">Description</span></span>                                        |
|-------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="54498-112">**ContextMap**</span><span class="sxs-lookup"><span data-stu-id="54498-112">**ContextMap**</span></span>](windowsribbon-element-contextmap.md)<br/> | <span data-ttu-id="54498-113">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="54498-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="54498-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="54498-114">Parent elements</span></span>



| <span data-ttu-id="54498-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="54498-115">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="54498-116">**ContextPopup**</span><span class="sxs-lookup"><span data-stu-id="54498-116">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="54498-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="54498-117">Remarks</span></span>

<span data-ttu-id="54498-118">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="54498-118">Optional.</span></span>

<span data-ttu-id="54498-119">Può essere presente al massimo una volta per ogni [**ContextPopup**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="54498-119">May occur at most once for each [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

## <a name="examples"></a><span data-ttu-id="54498-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="54498-120">Examples</span></span>

<span data-ttu-id="54498-121">Nell'esempio seguente viene illustrato il markup di base per una visualizzazione [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="54498-121">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="54498-122">In questa sezione del codice viene illustrata una dichiarazione di controllo **ContextPopup. ContextMaps** .</span><span class="sxs-lookup"><span data-stu-id="54498-122">This section of code shows a **ContextPopup.ContextMaps** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="54498-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54498-123">Requirements</span></span>



| <span data-ttu-id="54498-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="54498-124">Requirement</span></span> | <span data-ttu-id="54498-125">Valore</span><span class="sxs-lookup"><span data-stu-id="54498-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="54498-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54498-126">Minimum supported client</span></span><br/> | <span data-ttu-id="54498-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="54498-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="54498-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54498-128">Minimum supported server</span></span><br/> | <span data-ttu-id="54498-129">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="54498-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="54498-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54498-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54498-131">Controllo popup contesto</span><span class="sxs-lookup"><span data-stu-id="54498-131">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





