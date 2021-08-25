---
title: Elemento MiniToolbar
description: Rappresenta una barra degli strumenti contestuale.
ms.assetid: bb50890d-554a-4add-a583-d4fd48b823bf
keywords:
- Elemento MiniToolbar Windows ribbon
topic_type:
- apiref
api_name:
- MiniToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e47fee9fbf2b6b0bc95153fd512f6484129dc7f3edebd56e1d97664ecc2bbef0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881741"
---
# <a name="minitoolbar-element"></a>Elemento MiniToolbar

Rappresenta una barra degli strumenti contestuale.

## <a name="usage"></a>Utilizzo

``` syntax
<MiniToolbar
  Name = "xs:string">
  child elements
</MiniToolbar>
```

## <a name="attributes"></a>Attributi



| Attributo           | Type                 | Obbligatoria       | Descrizione                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nome**<br/> | xs:string<br/> | Sì<br/> | <dt> (xs:string)<br/> </dt> <dd> Stringa composta da qualsiasi sequenza di caratteri, inclusi spazi vuoti e caratteri di interruzione di riga.<br/> </dd> </dl> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                         | Descrizione                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [**Menugroup**](windowsribbon-element-menugroup.md)<br/> | Deve verificarsi almeno una volta<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [**ContextPopup.MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi una o più volte per [**ogni ContextPopup.MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md).

A differenza [**dell'elemento ContextMenu,**](windowsribbon-element-contextmenu.md) **miniToolbar** rimane visibile quando si fa clic su un elemento sulla barra degli strumenti.

Se viene visualizzato senza [**ContextMenu,**](windowsribbon-element-contextmenu.md) **miniToolbar** si dissolve quando il puntatore del mouse viene spostato.

> [!Note]  
> A causa di questo comportamento di dissolvente, [**un contextMenu**](windowsribbon-element-contextmenu.md) deve essere visualizzato in prossimità del puntatore del mouse.

 

Poiché i controlli in **MiniToolbar** non sono accessibili tramite tastiera, i comandi che espongono devono essere disponibili altrove nell'interfaccia utente della barra multifunzione.

## <a name="examples"></a>Esempio

L'esempio seguente illustra il markup di base per [**una visualizzazione ContextPopup.**](windowsribbon-element-contextpopup.md)

Questa sezione di codice illustra un set di **dichiarazioni di controllo MiniToolbar.**


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



## <a name="element-information"></a>Informazioni sull'elemento

* **Sistema minimo supportato:** Windows 7
* **Può essere vuoto:** No



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo Popup di contesto](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





