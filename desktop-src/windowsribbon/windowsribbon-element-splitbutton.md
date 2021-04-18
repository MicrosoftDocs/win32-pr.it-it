---
title: Elemento SplitButton
description: Rappresenta un controllo pulsante di suddivisione standard.
ms.assetid: dece1100-ed04-49a3-a16d-3c5d5e7a2225
keywords:
- Barra multifunzione Windows elemento SplitButton
topic_type:
- apiref
api_name:
- SplitButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3235d58d6499d7d57c54e33e1049f40c50dd189a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300050"
---
# <a name="splitbutton-element"></a>Elemento SplitButton

Rappresenta un controllo [pulsante di suddivisione](windowsribbon-controls-splitbutton.md) standard.

## <a name="usage"></a>Utilizzo

``` syntax
<SplitButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</SplitButton>
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
<td><strong>ApplicationModes</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Valido solo se <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> è l'elemento padre.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: String)<br/> </dt> <dd> Stringa che contiene un elenco delimitato da virgole di numeri interi compresi tra 0 e 31.<br/> Gli spazi vuoti sono validi e vengono ignorati.<br/> Lunghezza massima: 250 caratteri. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>XS: positiveInteger o xs: String<br/></td>
<td>No<br/></td>
<td>Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o xs: String)<br/> </dt> <dd> Stringa, valore intero compreso tra 2 e 59999, inclusivo o un valore esadecimale compreso tra 0x2 e 0xea5f, inclusi. <br/> Il valore deve essere univoco all'interno del documento XML della barra multifunzione. <br/> Lunghezza massima: 100 caratteri. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                   | Descrizione                                        |
|-------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Button**](windowsribbon-element-button.md)<br/>                                 | Può essere presente una o più volte<br/> <br/> |
| [**Casella**](windowsribbon-element-checkbox.md)<br/>                             | Può essere presente una o più volte<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>                 | Può essere presente una o più volte<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/>       | Può essere presente una o più volte<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>               | Può essere presente una o più volte<br/> <br/> |
| **SplitButton**<br/>                                                                | Può essere presente una o più volte<br/> <br/> |
| [**SplitButton. ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md)<br/> | Può verificarsi al massimo una volta<br/> <br/>      |
| [**SplitButton. MenuGroups**](windowsribbon-element-splitbutton-menugroups.md)<br/> | Può verificarsi al massimo una volta<br/> <br/>      |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>         | Può essere presente una o più volte<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                     | Può essere presente una o più volte<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                           |
|-----------------------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>             |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Group**](windowsribbon-element-group.md)<br/>                           |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>                   |
| **SplitButton**<br/>                                                        |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può essere presente una o più volte per ogni elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), **SplitButton** o [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .

**SplitButton** supporta le [modalità di applicazione](ribbon-applicationmodes.md) quando è ospitato nella colonna sinistra del menu dell'applicazione.

[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) e [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) non sono elementi figlio validi di [**DropDownButton**](windowsribbon-element-dropdownbutton.md) quando **DropDownButton** è un discendente di [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).

[**SplitButton. MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) deve essere presente una sola volta se le seguenti non sono presenti come elementi figlio di **SplitButton**:

-   [**Pulsante**](windowsribbon-element-button.md)
-   [**Casella**](windowsribbon-element-checkbox.md)
-   [**DropDownButton**](windowsribbon-element-dropdownbutton.md)
-   [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)
-   [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)
-   **SplitButton**
-   [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)
-   [**ToggleButton**](windowsribbon-element-togglebutton.md)

Questi controlli vengono considerati come elementi figlio di un singolo elemento predefinito [**SplitButton. MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) .

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per il [pulsante di suddivisione](windowsribbon-controls-splitbutton.md).

In questa sezione del codice vengono illustrate le dichiarazioni di comando **SplitButton** , con un [**gruppo**](windowsribbon-element-group.md) associato che funge da contenitore padre per l'elemento **SplitButton** .


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



In questa sezione del codice vengono illustrate le dichiarazioni di controllo **SplitButton** .


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



|                                     |           |
|-------------------------------------|-----------|
| Sistema minimo supportato<br/> | Windows 7 |
| Può essere vuoto                        | No        |



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Controllo pulsante combinato](windowsribbon-controls-splitbutton.md)
</dt> <dt>

[**Modalità selettore**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

