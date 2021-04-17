---
title: Proprietà ContextPopup. MiniToolbars
description: Rappresenta un contenitore per gli elementi MiniToolbar.
ms.assetid: 5c17e070-0520-44e6-a066-476107691205
keywords:
- Barra multifunzione di Windows ContextPopup. MiniToolbars
topic_type:
- apiref
api_name:
- ContextPopup.MiniToolbars
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee1e85e6b170b4b7408a17687bd26725e9183161
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478610"
---
# <a name="contextpopupminitoolbars-property"></a><span data-ttu-id="a209d-104">Proprietà ContextPopup. MiniToolbars</span><span class="sxs-lookup"><span data-stu-id="a209d-104">ContextPopup.MiniToolbars property</span></span>

<span data-ttu-id="a209d-105">Rappresenta un contenitore per gli elementi [**MiniToolbar**](windowsribbon-element-minitoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="a209d-105">Represents a container for [**MiniToolbar**](windowsribbon-element-minitoolbar.md) elements.</span></span>

## <a name="usage"></a><span data-ttu-id="a209d-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="a209d-106">Usage</span></span>

``` syntax
<ContextPopup.MiniToolbars>
  child elements
</ContextPopup.MiniToolbars>
```

## <a name="attributes"></a><span data-ttu-id="a209d-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="a209d-107">Attributes</span></span>

<span data-ttu-id="a209d-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="a209d-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a209d-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a209d-109">Child elements</span></span>



| <span data-ttu-id="a209d-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="a209d-110">Element</span></span>                                                             | <span data-ttu-id="a209d-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a209d-111">Description</span></span>                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="a209d-112">**MiniToolbar**</span><span class="sxs-lookup"><span data-stu-id="a209d-112">**MiniToolbar**</span></span>](windowsribbon-element-minitoolbar.md)<br/> | <span data-ttu-id="a209d-113">Può essere presente una o più volte</span><span class="sxs-lookup"><span data-stu-id="a209d-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="a209d-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="a209d-114">Parent elements</span></span>



| <span data-ttu-id="a209d-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="a209d-115">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="a209d-116">**ContextPopup**</span><span class="sxs-lookup"><span data-stu-id="a209d-116">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a209d-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="a209d-117">Remarks</span></span>

<span data-ttu-id="a209d-118">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a209d-118">Optional.</span></span>

<span data-ttu-id="a209d-119">Può essere presente al massimo una volta per ogni [**ContextPopup**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="a209d-119">May occur at most once for each [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

<span data-ttu-id="a209d-120">Poiché i controlli in [**MiniToolbar**](windowsribbon-element-minitoolbar.md) non sono accessibili da tastiera, i comandi da essi esposti dovrebbero essere disponibili altrove nell'interfaccia utente della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="a209d-120">Because controls in the [**MiniToolbar**](windowsribbon-element-minitoolbar.md) are not keyboard accessible, the Commands they expose should be available elsewhere in the Ribbon UI.</span></span>

## <a name="examples"></a><span data-ttu-id="a209d-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="a209d-121">Examples</span></span>

<span data-ttu-id="a209d-122">Nell'esempio seguente viene illustrato il markup di base per una visualizzazione [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="a209d-122">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="a209d-123">Questa sezione di codice mostra la dichiarazione di controllo **ContextPopup. MiniToolbars** .</span><span class="sxs-lookup"><span data-stu-id="a209d-123">This section of code shows the **ContextPopup.MiniToolbars** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="a209d-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a209d-124">Requirements</span></span>



| <span data-ttu-id="a209d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a209d-125">Requirement</span></span> | <span data-ttu-id="a209d-126">Valore</span><span class="sxs-lookup"><span data-stu-id="a209d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="a209d-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a209d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a209d-128">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a209d-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="a209d-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a209d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a209d-130">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a209d-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a209d-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a209d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a209d-132">Controllo popup contesto</span><span class="sxs-lookup"><span data-stu-id="a209d-132">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





