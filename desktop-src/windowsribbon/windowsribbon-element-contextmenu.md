---
title: Elemento ContextMenu
description: Rappresenta un controllo menu di scelta rapida.
ms.assetid: 08cc0514-0795-4e6b-b80c-33d920783032
keywords:
- Barra multifunzione di Windows per l'elemento ContextMenu
topic_type:
- apiref
api_name:
- ContextMenu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 916a031ed642a76fb22ecc58dbbe1ce29cbcd105
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443470"
---
# <a name="contextmenu-element"></a><span data-ttu-id="20867-104">Elemento ContextMenu</span><span class="sxs-lookup"><span data-stu-id="20867-104">ContextMenu element</span></span>

<span data-ttu-id="20867-105">Rappresenta un controllo menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="20867-105">Represents a context menu control.</span></span>

## <a name="usage"></a><span data-ttu-id="20867-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="20867-106">Usage</span></span>

``` syntax
<ContextMenu
  Name = "xs:string">
  child elements
</ContextMenu>
```

## <a name="attributes"></a><span data-ttu-id="20867-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="20867-107">Attributes</span></span>



| <span data-ttu-id="20867-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="20867-108">Attribute</span></span>           | <span data-ttu-id="20867-109">Type</span><span class="sxs-lookup"><span data-stu-id="20867-109">Type</span></span>                 | <span data-ttu-id="20867-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="20867-110">Required</span></span>       | <span data-ttu-id="20867-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20867-111">Description</span></span>                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20867-112">**Nome**</span><span class="sxs-lookup"><span data-stu-id="20867-112">**Name**</span></span><br/> | <span data-ttu-id="20867-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="20867-113">xs:string</span></span><br/> | <span data-ttu-id="20867-114">Sì</span><span class="sxs-lookup"><span data-stu-id="20867-114">Yes</span></span><br/> | <span data-ttu-id="20867-115"><dt> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="20867-115"><dt> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="20867-116">Stringa composta da qualsiasi sequenza di caratteri, inclusi spazi vuoti e caratteri di interruzione di riga.</span><span class="sxs-lookup"><span data-stu-id="20867-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="20867-117">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="20867-117">Child elements</span></span>



| <span data-ttu-id="20867-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="20867-118">Element</span></span>                                                         | <span data-ttu-id="20867-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20867-119">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="20867-120">**Menugroup**</span><span class="sxs-lookup"><span data-stu-id="20867-120">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="20867-121">Deve verificarsi almeno una volta</span><span class="sxs-lookup"><span data-stu-id="20867-121">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="20867-122">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="20867-122">Parent elements</span></span>



| <span data-ttu-id="20867-123">Elemento</span><span class="sxs-lookup"><span data-stu-id="20867-123">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20867-124">**ContextPopup.ContextMenus**</span><span class="sxs-lookup"><span data-stu-id="20867-124">**ContextPopup.ContextMenus**</span></span>](windowsribbon-element-contextpopup-contextmenus.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="20867-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="20867-125">Remarks</span></span>

<span data-ttu-id="20867-126">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="20867-126">Optional.</span></span>

<span data-ttu-id="20867-127">Può verificarsi una o più volte per [**ogni ContextPopup.ContextMenus**](windowsribbon-element-contextpopup-contextmenus.md).</span><span class="sxs-lookup"><span data-stu-id="20867-127">May occur one or more times for each [**ContextPopup.ContextMenus**](windowsribbon-element-contextpopup-contextmenus.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="20867-128">ContextMenu **non** può ospitare [controlli Casella combinata](windowsribbon-controls-combobox.md) o Casella di [selezione.](windowsribbon-controls-spinner.md)</span><span class="sxs-lookup"><span data-stu-id="20867-128">A **ContextMenu** cannot host [Combo Box](windowsribbon-controls-combobox.md) or [Spinner](windowsribbon-controls-spinner.md) controls.</span></span>

 

## <a name="examples"></a><span data-ttu-id="20867-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="20867-129">Examples</span></span>

<span data-ttu-id="20867-130">L'esempio seguente illustra il markup di base per [**una visualizzazione ContextPopup.**](windowsribbon-element-contextpopup.md)</span><span class="sxs-lookup"><span data-stu-id="20867-130">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="20867-131">Questa sezione di codice illustra un set di **dichiarazioni di controllo ContextMenu.**</span><span class="sxs-lookup"><span data-stu-id="20867-131">This section of code shows a set of **ContextMenu** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="20867-132">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="20867-132">Element information</span></span>

* <span data-ttu-id="20867-133">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="20867-133">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="20867-134">**Può essere vuoto:** No</span><span class="sxs-lookup"><span data-stu-id="20867-134">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="20867-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20867-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20867-136">Controllo Popup di contesto</span><span class="sxs-lookup"><span data-stu-id="20867-136">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





