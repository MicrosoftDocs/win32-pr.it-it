---
title: ContextPopup. ContextMenus (proprietà)
description: Rappresenta un contenitore per gli elementi ContextMenu.
ms.assetid: 92633689-a892-421e-a5fb-e494f4cd1ea8
keywords:
- ContextPopup. ContextMenus-barra multifunzione di Windows
topic_type:
- apiref
api_name:
- ContextPopup.ContextMenus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ef8ab053b9912f545c2aad931eb8ad9583ff62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302308"
---
# <a name="contextpopupcontextmenus-property"></a><span data-ttu-id="2c56a-104">ContextPopup. ContextMenus (proprietà)</span><span class="sxs-lookup"><span data-stu-id="2c56a-104">ContextPopup.ContextMenus property</span></span>

<span data-ttu-id="2c56a-105">Rappresenta un contenitore per gli elementi [**ContextMenu**](windowsribbon-element-contextmenu.md) .</span><span class="sxs-lookup"><span data-stu-id="2c56a-105">Represents a container for [**ContextMenu**](windowsribbon-element-contextmenu.md) elements.</span></span>

## <a name="usage"></a><span data-ttu-id="2c56a-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="2c56a-106">Usage</span></span>

``` syntax
<ContextPopup.ContextMenus>
  child elements
</ContextPopup.ContextMenus>
```

## <a name="attributes"></a><span data-ttu-id="2c56a-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="2c56a-107">Attributes</span></span>

<span data-ttu-id="2c56a-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="2c56a-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2c56a-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="2c56a-109">Child elements</span></span>



| <span data-ttu-id="2c56a-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="2c56a-110">Element</span></span>                                                             | <span data-ttu-id="2c56a-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c56a-111">Description</span></span>                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="2c56a-112">**ContextMenu**</span><span class="sxs-lookup"><span data-stu-id="2c56a-112">**ContextMenu**</span></span>](windowsribbon-element-contextmenu.md)<br/> | <span data-ttu-id="2c56a-113">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="2c56a-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="2c56a-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="2c56a-114">Parent elements</span></span>



| <span data-ttu-id="2c56a-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="2c56a-115">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="2c56a-116">**ContextPopup**</span><span class="sxs-lookup"><span data-stu-id="2c56a-116">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="2c56a-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="2c56a-117">Remarks</span></span>

<span data-ttu-id="2c56a-118">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2c56a-118">Optional.</span></span>

<span data-ttu-id="2c56a-119">Può essere presente al massimo una volta per ogni [**ContextPopup**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="2c56a-119">May occur at most once for each [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2c56a-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="2c56a-120">Examples</span></span>

<span data-ttu-id="2c56a-121">Nell'esempio seguente viene illustrato il markup di base per una visualizzazione [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="2c56a-121">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="2c56a-122">In questa sezione del codice viene illustrata una dichiarazione di controllo **ContextPopup. ContextMenus** .</span><span class="sxs-lookup"><span data-stu-id="2c56a-122">This section of code shows a **ContextPopup.ContextMenus** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="2c56a-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c56a-123">Requirements</span></span>



| <span data-ttu-id="2c56a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c56a-124">Requirement</span></span> | <span data-ttu-id="2c56a-125">Valore</span><span class="sxs-lookup"><span data-stu-id="2c56a-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="2c56a-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c56a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2c56a-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2c56a-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="2c56a-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c56a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2c56a-129">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2c56a-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2c56a-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c56a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c56a-131">Controllo popup contesto</span><span class="sxs-lookup"><span data-stu-id="2c56a-131">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





