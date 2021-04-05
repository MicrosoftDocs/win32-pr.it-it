---
title: Elemento ContextMenu
description: Rappresenta un controllo del menu di scelta rapida.
ms.assetid: 08cc0514-0795-4e6b-b80c-33d920783032
keywords:
- Barra multifunzione Windows elemento ContextMenu
topic_type:
- apiref
api_name:
- ContextMenu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c824e87c063fb863e79f10cb9755b74df36023f7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718379"
---
# <a name="contextmenu-element"></a><span data-ttu-id="48158-104">Elemento ContextMenu</span><span class="sxs-lookup"><span data-stu-id="48158-104">ContextMenu element</span></span>

<span data-ttu-id="48158-105">Rappresenta un controllo del menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="48158-105">Represents a context menu control.</span></span>

## <a name="usage"></a><span data-ttu-id="48158-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="48158-106">Usage</span></span>

``` syntax
<ContextMenu
  Name = "xs:string">
  child elements
</ContextMenu>
```

## <a name="attributes"></a><span data-ttu-id="48158-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="48158-107">Attributes</span></span>



| <span data-ttu-id="48158-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="48158-108">Attribute</span></span>           | <span data-ttu-id="48158-109">Type</span><span class="sxs-lookup"><span data-stu-id="48158-109">Type</span></span>                 | <span data-ttu-id="48158-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="48158-110">Required</span></span>       | <span data-ttu-id="48158-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48158-111">Description</span></span>                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48158-112">**Nome**</span><span class="sxs-lookup"><span data-stu-id="48158-112">**Name**</span></span><br/> | <span data-ttu-id="48158-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="48158-113">xs:string</span></span><br/> | <span data-ttu-id="48158-114">Sì</span><span class="sxs-lookup"><span data-stu-id="48158-114">Yes</span></span><br/> | <span data-ttu-id="48158-115"><dt> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="48158-115"><dt> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="48158-116">Stringa costituita da qualsiasi sequenza di caratteri, inclusi gli spazi vuoti e i caratteri di interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="48158-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="48158-117">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="48158-117">Child elements</span></span>



| <span data-ttu-id="48158-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="48158-118">Element</span></span>                                                         | <span data-ttu-id="48158-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48158-119">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="48158-120">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="48158-120">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="48158-121">Deve essere presente almeno una volta</span><span class="sxs-lookup"><span data-stu-id="48158-121">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="48158-122">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="48158-122">Parent elements</span></span>



| <span data-ttu-id="48158-123">Elemento</span><span class="sxs-lookup"><span data-stu-id="48158-123">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48158-124">**ContextPopup. ContextMenus**</span><span class="sxs-lookup"><span data-stu-id="48158-124">**ContextPopup.ContextMenus**</span></span>](windowsribbon-element-contextpopup-contextmenus.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="48158-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="48158-125">Remarks</span></span>

<span data-ttu-id="48158-126">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="48158-126">Optional.</span></span>

<span data-ttu-id="48158-127">Può verificarsi una o più volte per ogni [**ContextPopup. ContextMenus**](windowsribbon-element-contextpopup-contextmenus.md).</span><span class="sxs-lookup"><span data-stu-id="48158-127">May occur one or more times for each [**ContextPopup.ContextMenus**](windowsribbon-element-contextpopup-contextmenus.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="48158-128">Un oggetto **ContextMenu** non può [ospitare controlli](windowsribbon-controls-spinner.md) [casella combinata o casella](windowsribbon-controls-combobox.md) di selezione.</span><span class="sxs-lookup"><span data-stu-id="48158-128">A **ContextMenu** cannot host [Combo Box](windowsribbon-controls-combobox.md) or [Spinner](windowsribbon-controls-spinner.md) controls.</span></span>

 

## <a name="examples"></a><span data-ttu-id="48158-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="48158-129">Examples</span></span>

<span data-ttu-id="48158-130">Nell'esempio seguente viene illustrato il markup di base per una visualizzazione [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="48158-130">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="48158-131">Questa sezione di codice mostra un set di dichiarazioni di controllo **ContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="48158-131">This section of code shows a set of **ContextMenu** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="48158-132">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="48158-132">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="48158-133">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48158-133">Minimum supported system</span></span><br/> | <span data-ttu-id="48158-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="48158-134">Windows 7</span></span> |
| <span data-ttu-id="48158-135">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="48158-135">Can be empty</span></span>                        | <span data-ttu-id="48158-136">No</span><span class="sxs-lookup"><span data-stu-id="48158-136">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="48158-137">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="48158-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48158-138">Controllo popup contesto</span><span class="sxs-lookup"><span data-stu-id="48158-138">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





