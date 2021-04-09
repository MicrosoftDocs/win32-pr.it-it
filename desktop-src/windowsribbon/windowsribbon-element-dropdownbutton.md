---
title: Elemento DropDownButton
description: Rappresenta un controllo pulsante di Drop-Down standard.
ms.assetid: 41031be2-43bc-4f75-b37a-1dcecc1635e1
keywords:
- Barra multifunzione Windows elemento DropDownButton
topic_type:
- apiref
api_name:
- DropDownButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 98af363aeb70a61def04eaee0ad13ff60e6e7640
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729223"
---
# <a name="dropdownbutton-element"></a>Elemento DropDownButton

Rappresenta un controllo [pulsante a discesa](windowsribbon-controls-dropdownbutton.md) standard.

## <a name="usage"></a>Utilizzo

``` syntax
<DropDownButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</DropDownButton>
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



| Elemento                                                                             | Descrizione                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Button**](windowsribbon-element-button.md)<br/>                           | Può essere presente una o più volte<br/> <br/> |
| [**Casella**](windowsribbon-element-checkbox.md)<br/>                       | Può essere presente una o più volte<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                       | Può essere presente una o più volte<br/> <br/> |
| **DropDownButton**<br/>                                                       | Può essere presente una o più volte<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/> | Può essere presente una o più volte<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>         | Può essere presente una o più volte<br/> <br/> |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>                     | Deve essere presente almeno una volta<br/> <br/>    |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                 | Può essere presente una o più volte<br/> <br/> |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>   | Può essere presente una o più volte<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>               | Può essere presente una o più volte<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                           |
|-----------------------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>             |
| **DropDownButton**<br/>                                                     |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Group**](windowsribbon-element-group.md)<br/>                           |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>                   |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>               |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Commenti

Facoltativo o obbligatorio, a seconda dell'elemento padre.

Può essere presente una o più volte per ogni elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), **DropDownButton**, [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md)o [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .

**DropDownButton** supporta le [modalità di applicazione](ribbon-applicationmodes.md) quando è ospitato nella colonna sinistra del menu dell'applicazione.

[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) e [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) non sono elementi figlio validi di **DropDownButton** quando **DropDownButton** è un discendente di [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per **DropDownButton**.

In questa sezione del codice vengono illustrate le dichiarazioni di comando **DropDownButton** , con un [**gruppo**](windowsribbon-element-group.md) associato che funge da contenitore padre per l'elemento **DropDownButton** .


```XML
<!-- DropDownButton -->
<Command Name="cmdDropDownButtonGroup"
         Symbol="cmdDropDownButtonGroup"
         Comment="DropDownButton Group"
         LabelTitle="DropDownButton"/>
<Command Name="cmdDropDownButton"
         Symbol="cmdDropDownButton"
         Comment="DropDownButton"
         LabelTitle="DropDownButton"/>
<Command Name="cmdDDBButton1"
         Symbol="cmdDDBButton1"
         Comment="DDBButton1"
         LabelTitle="DDB Button"/>
<Command Name="cmdDDBColorPicker"
         Symbol="cmdDDBColorPicker"
         Comment="DDBColorPicker"
         LabelTitle="DDB ColorPicker"/>
```



In questa sezione del codice vengono illustrate le dichiarazioni di controllo **DropDownButton** .


```XML
<Group CommandName="cmdDropDownButtonGroup">
  <DropDownButton CommandName="cmdDropDownButton">
    <MenuGroup>
      <Button CommandName="cmdDDBButton1"/>
      <DropDownColorPicker CommandName="cmdDDBColorPicker"/>
    </MenuGroup>
  </DropDownButton>
</Group>
```



## <a name="element-information"></a>Informazioni sull'elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema minimo supportato<br/> | Windows 7 |
| Può essere vuoto                        | No        |



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Controllo pulsante a discesa](windowsribbon-controls-dropdownbutton.md)
</dt> <dt>

[**Modalità selettore**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

