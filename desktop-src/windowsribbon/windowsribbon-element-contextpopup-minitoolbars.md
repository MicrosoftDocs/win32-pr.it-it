---
title: ContextPopup.MiniToolbars - proprietà
description: Rappresenta un contenitore per gli elementi MiniToolbar.
ms.assetid: 5c17e070-0520-44e6-a066-476107691205
keywords:
- Proprietà ContextPopup.MiniToolbars Windows ribbon
topic_type:
- apiref
api_name:
- ContextPopup.MiniToolbars
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18f4a083d894f798d83bd153fe74b9fb0560e2fbdb8132ec7874db0a2e533824
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772131"
---
# <a name="contextpopupminitoolbars-property"></a>ContextPopup.MiniToolbars - proprietà

Rappresenta un contenitore per [**gli elementi MiniToolbar.**](windowsribbon-element-minitoolbar.md)

## <a name="usage"></a>Utilizzo

``` syntax
<ContextPopup.MiniToolbars>
  child elements
</ContextPopup.MiniToolbars>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                             | Descrizione                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [**MiniToolbar**](windowsribbon-element-minitoolbar.md)<br/> | Può verificarsi una o più volte<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                               |
|-----------------------------------------------------------------------|
| [**ContextPopup**](windowsribbon-element-contextpopup.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi al massimo una volta per [**ogni ContextPopup**](windowsribbon-element-contextpopup.md).

Poiché i controlli in [**MiniToolbar**](windowsribbon-element-minitoolbar.md) non sono accessibili tramite tastiera, i comandi che espongono devono essere disponibili altrove nell'interfaccia utente della barra multifunzione.

## <a name="examples"></a>Esempio

L'esempio seguente illustra il markup di base per [**una visualizzazione ContextPopup.**](windowsribbon-element-contextpopup.md)

Questa sezione di codice illustra la dichiarazione del controllo **ContextPopup.MiniToolbars.**


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



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo Popup di contesto](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





