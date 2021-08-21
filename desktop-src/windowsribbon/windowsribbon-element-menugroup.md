---
title: Elemento MenuGroup
description: Rappresenta un contenitore di controlli da visualizzare in una raccolta, in un menu o in una barra degli strumenti.
ms.assetid: 75da63fe-dd9e-46af-8f13-a8d8e7575641
keywords:
- Elemento MenuGroup Windows barra multifunzione
topic_type:
- apiref
api_name:
- MenuGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 854b33d1e11df15b5b383bf004986edc18418f6204ae1298c3171a6653cf5301
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118707095"
---
# <a name="menugroup-element"></a>Elemento MenuGroup

Rappresenta un contenitore di controlli da visualizzare in una raccolta, in un menu o in una barra degli strumenti.

## <a name="usage"></a>Utilizzo

``` syntax
<MenuGroup
  Class = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</MenuGroup>
```

## <a name="attributes"></a>Attributi



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Type</th>
<th>Obbligatoria</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Classe</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Specifica le dimensioni e lo stile di layout per gli elementi nell'interfaccia utente del menu.<br/> Una risorsa immagine può essere fornita in due dimensioni (grande e piccola) e associata all'elemento nel markup usando gli elementi della proprietà <a href="windowsribbon-element-command-largeimages.md"><strong>Command.LargeImages</strong></a> e <a href="windowsribbon-element-command-smallimages.md"><strong>Command.SmallImages.</strong></a> Se viene specificata una sola immagine, il framework la ridimensiona in base alle esigenze.<br/> Limitato a uno dei valori seguenti:<br/> <br/>
<dt><span></span><span></span><strong></strong> (StandardItems)<br/> </dt> <dd> Valore predefinito. <br/> Stile: immagine piccola e testo de-evidenziato.<br/><img src="images/markup/menugroup-standarditems.png" alt="Screen shot of a StandardItems button." /></dd> <dt><span></span><span></span><strong></strong> (MajorItems)<br/> </dt> <dd> Stile: immagine grande e testo in grassetto.<br/>
<blockquote>
[!Note]<br />
Se <strong>MenuGroup</strong> è un elemento figlio di <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu,</strong></a>l'attributo <em>Class</em> viene ignorato e lo stile viene <code>MajorItems</code> applicato dal framework.
</blockquote>
<br/> <img src="images/markup/menugroup-majoritems.png" alt="Screen shot of a MajorItems button." /></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger o xs:string<br/></td>
<td>No<br/></td>
<td>Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command.</strong></a><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)<br/> </dt> <dd> Stringa, valore intero compreso tra 2 e 59999 inclusi o valore esadecimale compreso tra 0x2 e 0xea5f inclusi. <br/> Il valore deve essere univoco all'interno del documento XML della barra multifunzione. <br/> Lunghezza massima: 100 caratteri. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                             | Descrizione                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Button**](windowsribbon-element-button.md)<br/>                           | Può verificarsi una o più volte<br/> <br/> |
| [**CheckBox**](windowsribbon-element-checkbox.md)<br/>                       | Può verificarsi una o più volte<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                       | Può verificarsi una o più volte<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>           | Può verificarsi una o più volte<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/> | Può verificarsi una o più volte<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>         | Può verificarsi una o più volte<br/> <br/> |
| [**Controllo FontControl**](windowsribbon-element-fontcontrol.md)<br/>                 | Può verificarsi al massimo una volta<br/> <br/>      |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                 | Può verificarsi una o più volte<br/> <br/> |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>   | Può verificarsi una o più volte<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>               | Può verificarsi una o più volte<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [**ApplicationMenu**](windowsribbon-element-applicationmenu.md)<br/>                             |
| [**ContextMenu**](windowsribbon-element-contextmenu.md)<br/>                                     |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>                               |
| [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md)<br/>       |
| [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md)<br/>       |
| [**MiniToolbar**](windowsribbon-element-minitoolbar.md)<br/>                                     |
| [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md)<br/>               |
| [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> |



## <a name="remarks"></a>Commenti

Obbligatorio.

Deve verificarsi almeno una volta per ogni elemento [**ApplicationMenu**](windowsribbon-element-applicationmenu.md), [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md), [**MiniToolbar**](windowsribbon-element-minitoolbar.md)o [**SplitButtonGallery.MenuGroups.**](windowsribbon-element-splitbuttongallery-menugroups.md)

Se [**ApplicationMenu è**](windowsribbon-element-applicationmenu.md) l'elemento padre, **MenuGroup** è vincolato agli elementi figlio [**seguenti: Button**](windowsribbon-element-button.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md)o [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).

Se [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md)o [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) è l'elemento padre, **MenuGroup** è vincolato agli elementi figlio [**seguenti: Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), **DropDownButton**, [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)o [**ToggleButton**](windowsribbon-element-togglebutton.md).

Se [**MiniToolbar è**](windowsribbon-element-minitoolbar.md) l'elemento padre, **MenuGroup** è vincolato agli elementi figlio [**seguenti: Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)o [**ToggleButton**](windowsribbon-element-togglebutton.md).

L'attributo Class non è obbligatorio quando [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) è l'elemento padre. Il framework applica il valore MajorItems per l'attributo Class.

Quando [**ApplicationMenu è**](windowsribbon-element-applicationmenu.md) l'elemento padre, l'attributo Class non è obbligatorio.

## <a name="examples"></a>Esempio

L'esempio seguente illustra il markup di base per [**SplitButton**](windowsribbon-element-splitbutton.md) con un **elemento MenuGroup.**

Questa sezione di codice mostra le dichiarazioni [**SplitButton**](windowsribbon-element-splitbutton.md) e **MenuGroup** Command con una risorsa immagine di grandi dimensioni e una piccola. Viene dichiarato anche un oggetto [**Group**](windowsribbon-element-group.md) associato che funge da contenitore padre per **l'elemento SplitButton.**


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



Questa sezione di codice illustra le [**dichiarazioni dei controlli SplitButton**](windowsribbon-element-splitbutton.md) e **MenuGroup** con `StandardItems` e `MajorItems` .


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="element-information"></a>Informazioni sull'elemento

* **Sistema minimo supportato:** Windows 7
* **Può essere vuoto:** No



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Specifica delle risorse immagine della barra multifunzione](windowsribbon-imageformats.md)
</dt> <dt>

[Gruppo di menu](windowsribbon-controls-menugroup.md)
</dt> </dl>

 

 





