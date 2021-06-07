---
title: Elemento MiniToolbar
description: Rappresenta una barra degli strumenti contestuale.
ms.assetid: bb50890d-554a-4add-a583-d4fd48b823bf
keywords:
- Barra multifunzione di Windows per l'elemento MiniToolbar
topic_type:
- apiref
api_name:
- MiniToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ceea8ba1a220674f177e740411bf98a13d7bfc2e
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443262"
---
# <a name="minitoolbar-element"></a><span data-ttu-id="33d1a-104">Elemento MiniToolbar</span><span class="sxs-lookup"><span data-stu-id="33d1a-104">MiniToolbar element</span></span>

<span data-ttu-id="33d1a-105">Rappresenta una barra degli strumenti contestuale.</span><span class="sxs-lookup"><span data-stu-id="33d1a-105">Represents a contextual toolbar.</span></span>

## <a name="usage"></a><span data-ttu-id="33d1a-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="33d1a-106">Usage</span></span>

``` syntax
<MiniToolbar
  Name = "xs:string">
  child elements
</MiniToolbar>
```

## <a name="attributes"></a><span data-ttu-id="33d1a-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="33d1a-107">Attributes</span></span>



| <span data-ttu-id="33d1a-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="33d1a-108">Attribute</span></span>           | <span data-ttu-id="33d1a-109">Type</span><span class="sxs-lookup"><span data-stu-id="33d1a-109">Type</span></span>                 | <span data-ttu-id="33d1a-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="33d1a-110">Required</span></span>       | <span data-ttu-id="33d1a-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33d1a-111">Description</span></span>                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33d1a-112">**Nome**</span><span class="sxs-lookup"><span data-stu-id="33d1a-112">**Name**</span></span><br/> | <span data-ttu-id="33d1a-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="33d1a-113">xs:string</span></span><br/> | <span data-ttu-id="33d1a-114">Sì</span><span class="sxs-lookup"><span data-stu-id="33d1a-114">Yes</span></span><br/> | <span data-ttu-id="33d1a-115"><dt> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="33d1a-115"><dt> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="33d1a-116">Stringa composta da qualsiasi sequenza di caratteri, inclusi spazi vuoti e caratteri di interruzione di riga.</span><span class="sxs-lookup"><span data-stu-id="33d1a-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="33d1a-117">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="33d1a-117">Child elements</span></span>



| <span data-ttu-id="33d1a-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="33d1a-118">Element</span></span>                                                         | <span data-ttu-id="33d1a-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33d1a-119">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="33d1a-120">**Menugroup**</span><span class="sxs-lookup"><span data-stu-id="33d1a-120">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="33d1a-121">Deve verificarsi almeno una volta</span><span class="sxs-lookup"><span data-stu-id="33d1a-121">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="33d1a-122">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="33d1a-122">Parent elements</span></span>



| <span data-ttu-id="33d1a-123">Elemento</span><span class="sxs-lookup"><span data-stu-id="33d1a-123">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33d1a-124">**ContextPopup.MiniToolbars**</span><span class="sxs-lookup"><span data-stu-id="33d1a-124">**ContextPopup.MiniToolbars**</span></span>](windowsribbon-element-contextpopup-minitoolbars.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="33d1a-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="33d1a-125">Remarks</span></span>

<span data-ttu-id="33d1a-126">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="33d1a-126">Optional.</span></span>

<span data-ttu-id="33d1a-127">Può verificarsi una o più volte per [**ogni ContextPopup.MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md).</span><span class="sxs-lookup"><span data-stu-id="33d1a-127">May occur one or more times for each [**ContextPopup.MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md).</span></span>

<span data-ttu-id="33d1a-128">A differenza [**dell'elemento ContextMenu,**](windowsribbon-element-contextmenu.md) **miniToolbar** rimane visibile quando si fa clic su un elemento sulla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="33d1a-128">Unlike the [**ContextMenu**](windowsribbon-element-contextmenu.md) element, the **MiniToolbar** remains visible when an item on the toolbar is clicked.</span></span>

<span data-ttu-id="33d1a-129">Se viene visualizzato senza [**ContextMenu,**](windowsribbon-element-contextmenu.md) **miniToolbar** si dissolve quando il puntatore del mouse viene spostato.</span><span class="sxs-lookup"><span data-stu-id="33d1a-129">If displayed without a [**ContextMenu**](windowsribbon-element-contextmenu.md), the **MiniToolbar** fades as the mouse pointer is moved away.</span></span>

> [!Note]  
> <span data-ttu-id="33d1a-130">A causa di questo comportamento di dissolvente, [**un contextMenu**](windowsribbon-element-contextmenu.md) deve essere visualizzato in prossimità del puntatore del mouse.</span><span class="sxs-lookup"><span data-stu-id="33d1a-130">Due to this fading behavior, a [**ContextMenu**](windowsribbon-element-contextmenu.md) should be displayed in close proximity to the mouse pointer.</span></span>

 

<span data-ttu-id="33d1a-131">Poiché i controlli in **MiniToolbar** non sono accessibili tramite tastiera, i comandi che espongono devono essere disponibili altrove nell'interfaccia utente della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="33d1a-131">Because controls in the **MiniToolbar** are not keyboard accessible, the Commands they expose should be available elsewhere in the Ribbon UI.</span></span>

## <a name="examples"></a><span data-ttu-id="33d1a-132">Esempio</span><span class="sxs-lookup"><span data-stu-id="33d1a-132">Examples</span></span>

<span data-ttu-id="33d1a-133">L'esempio seguente illustra il markup di base per [**una visualizzazione ContextPopup.**](windowsribbon-element-contextpopup.md)</span><span class="sxs-lookup"><span data-stu-id="33d1a-133">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="33d1a-134">Questa sezione di codice illustra un set di **dichiarazioni di controllo MiniToolbar.**</span><span class="sxs-lookup"><span data-stu-id="33d1a-134">This section of code shows a set of **MiniToolbar** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="33d1a-135">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="33d1a-135">Element information</span></span>

* <span data-ttu-id="33d1a-136">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="33d1a-136">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="33d1a-137">**Può essere vuoto:** No</span><span class="sxs-lookup"><span data-stu-id="33d1a-137">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="33d1a-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33d1a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33d1a-139">Controllo Popup di contesto</span><span class="sxs-lookup"><span data-stu-id="33d1a-139">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





