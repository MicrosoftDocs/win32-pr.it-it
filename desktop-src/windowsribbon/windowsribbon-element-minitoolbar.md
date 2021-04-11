---
title: Elemento MiniToolbar
description: Rappresenta una barra degli strumenti contestuale.
ms.assetid: bb50890d-554a-4add-a583-d4fd48b823bf
keywords:
- Barra multifunzione Windows elemento MiniToolbar
topic_type:
- apiref
api_name:
- MiniToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb5e4a27d10fe5233f8e7059bc9da8ecfd2fa383
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104116957"
---
# <a name="minitoolbar-element"></a><span data-ttu-id="63184-104">Elemento MiniToolbar</span><span class="sxs-lookup"><span data-stu-id="63184-104">MiniToolbar element</span></span>

<span data-ttu-id="63184-105">Rappresenta una barra degli strumenti contestuale.</span><span class="sxs-lookup"><span data-stu-id="63184-105">Represents a contextual toolbar.</span></span>

## <a name="usage"></a><span data-ttu-id="63184-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="63184-106">Usage</span></span>

``` syntax
<MiniToolbar
  Name = "xs:string">
  child elements
</MiniToolbar>
```

## <a name="attributes"></a><span data-ttu-id="63184-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="63184-107">Attributes</span></span>



| <span data-ttu-id="63184-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="63184-108">Attribute</span></span>           | <span data-ttu-id="63184-109">Type</span><span class="sxs-lookup"><span data-stu-id="63184-109">Type</span></span>                 | <span data-ttu-id="63184-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="63184-110">Required</span></span>       | <span data-ttu-id="63184-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63184-111">Description</span></span>                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63184-112">**Nome**</span><span class="sxs-lookup"><span data-stu-id="63184-112">**Name**</span></span><br/> | <span data-ttu-id="63184-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="63184-113">xs:string</span></span><br/> | <span data-ttu-id="63184-114">Sì</span><span class="sxs-lookup"><span data-stu-id="63184-114">Yes</span></span><br/> | <span data-ttu-id="63184-115"><dt> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="63184-115"><dt> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="63184-116">Stringa costituita da qualsiasi sequenza di caratteri, inclusi gli spazi vuoti e i caratteri di interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="63184-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="63184-117">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="63184-117">Child elements</span></span>



| <span data-ttu-id="63184-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="63184-118">Element</span></span>                                                         | <span data-ttu-id="63184-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63184-119">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="63184-120">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="63184-120">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="63184-121">Deve essere presente almeno una volta</span><span class="sxs-lookup"><span data-stu-id="63184-121">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="63184-122">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="63184-122">Parent elements</span></span>



| <span data-ttu-id="63184-123">Elemento</span><span class="sxs-lookup"><span data-stu-id="63184-123">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63184-124">**ContextPopup.MiniToolbars**</span><span class="sxs-lookup"><span data-stu-id="63184-124">**ContextPopup.MiniToolbars**</span></span>](windowsribbon-element-contextpopup-minitoolbars.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="63184-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="63184-125">Remarks</span></span>

<span data-ttu-id="63184-126">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="63184-126">Optional.</span></span>

<span data-ttu-id="63184-127">Può essere presente una o più volte per ogni [**ContextPopup. MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md).</span><span class="sxs-lookup"><span data-stu-id="63184-127">May occur one or more times for each [**ContextPopup.MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md).</span></span>

<span data-ttu-id="63184-128">Diversamente dall'elemento [**ContextMenu**](windowsribbon-element-contextmenu.md) , il **MiniToolbar** rimane visibile quando si fa clic su un elemento sulla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="63184-128">Unlike the [**ContextMenu**](windowsribbon-element-contextmenu.md) element, the **MiniToolbar** remains visible when an item on the toolbar is clicked.</span></span>

<span data-ttu-id="63184-129">Se viene visualizzato senza un oggetto [**ContextMenu**](windowsribbon-element-contextmenu.md), il **MiniToolbar** si dissolve quando il puntatore del mouse viene spostato fuori.</span><span class="sxs-lookup"><span data-stu-id="63184-129">If displayed without a [**ContextMenu**](windowsribbon-element-contextmenu.md), the **MiniToolbar** fades as the mouse pointer is moved away.</span></span>

> [!Note]  
> <span data-ttu-id="63184-130">A causa di questo comportamento di dissolvenza, un oggetto [**ContextMenu**](windowsribbon-element-contextmenu.md) deve essere visualizzato in prossimità del puntatore del mouse.</span><span class="sxs-lookup"><span data-stu-id="63184-130">Due to this fading behavior, a [**ContextMenu**](windowsribbon-element-contextmenu.md) should be displayed in close proximity to the mouse pointer.</span></span>

 

<span data-ttu-id="63184-131">Poiché i controlli in **MiniToolbar** non sono accessibili da tastiera, i comandi da essi esposti dovrebbero essere disponibili altrove nell'interfaccia utente della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="63184-131">Because controls in the **MiniToolbar** are not keyboard accessible, the Commands they expose should be available elsewhere in the Ribbon UI.</span></span>

## <a name="examples"></a><span data-ttu-id="63184-132">Esempio</span><span class="sxs-lookup"><span data-stu-id="63184-132">Examples</span></span>

<span data-ttu-id="63184-133">Nell'esempio seguente viene illustrato il markup di base per una visualizzazione [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="63184-133">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="63184-134">Questa sezione di codice mostra un set di dichiarazioni di controllo **MiniToolbar** .</span><span class="sxs-lookup"><span data-stu-id="63184-134">This section of code shows a set of **MiniToolbar** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="63184-135">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="63184-135">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="63184-136">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63184-136">Minimum supported system</span></span><br/> | <span data-ttu-id="63184-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="63184-137">Windows 7</span></span> |
| <span data-ttu-id="63184-138">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="63184-138">Can be empty</span></span>                        | <span data-ttu-id="63184-139">No</span><span class="sxs-lookup"><span data-stu-id="63184-139">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="63184-140">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="63184-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63184-141">Controllo popup contesto</span><span class="sxs-lookup"><span data-stu-id="63184-141">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





