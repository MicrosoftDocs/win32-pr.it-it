---
title: Elemento DropDownButton
description: Rappresenta un controllo Pulsante Drop-Down standard.
ms.assetid: 41031be2-43bc-4f75-b37a-1dcecc1635e1
keywords:
- Elemento DropDownButton Windows ribbon
topic_type:
- apiref
api_name:
- DropDownButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08353f4d6c743d92eff08f83e90babb9cc9d075f
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623927"
---
# <a name="dropdownbutton-element"></a>Elemento DropDownButton

Rappresenta un [controllo Pulsante a discesa](windowsribbon-controls-dropdownbutton.md) standard.

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
<col  />
<col  />
<col  />
<col  />
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
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Stringa contenente un elenco delimitato da virgole di numeri interi compresi tra 0 e 31.<br/> Gli spazi vuoti sono validi e ignorati.<br/> Lunghezza massima: 250 caratteri. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger o xs:string<br/></td>
<td>No<br/></td>
<td>Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)<br/> </dt> <dd> Stringa, valore intero compreso tra 2 e 59999, inclusivo o valore esadecimale compreso tra 0x2 e 0xea5f, inclusi. <br/> Il valore deve essere univoco all'interno del documento XML della barra multifunzione. <br/> Lunghezza massima: 100 caratteri. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                             | Descrizione                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Button**](windowsribbon-element-button.md)<br/>                           | Può verificarsi una o più volte<br/> <br/> |
| [**CheckBox**](windowsribbon-element-checkbox.md)<br/>                       | Può verificarsi una o più volte<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                       | Può verificarsi una o più volte<br/> <br/> |
| **DropDownButton**<br/>                                                       | Può verificarsi una o più volte<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/> | Può verificarsi una o più volte<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>         | Può verificarsi una o più volte<br/> <br/> |
| [**Menugroup**](windowsribbon-element-menugroup.md)<br/>                     | Deve verificarsi almeno una volta<br/> <br/>    |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                 | Può verificarsi una o più volte<br/> <br/> |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>   | Può verificarsi una o più volte<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>               | Può verificarsi una o più volte<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                           |
|-----------------------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>             |
| **DropDownButton**<br/>                                                     |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Group**](windowsribbon-element-group.md)<br/>                           |
| [**Menugroup**](windowsribbon-element-menugroup.md)<br/>                   |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>               |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Commenti

Facoltativo o obbligatorio, a seconda dell'elemento padre.

Può verificarsi una o più volte per ogni elemento [**ControlGroup,**](windowsribbon-element-controlgroup.md) **DropDownButton,** [**DropDownGallery,**](windowsribbon-element-dropdowngallery.md) [**Group,**](windowsribbon-element-group.md) [**MenuGroup,**](windowsribbon-element-menugroup.md) [**SplitButton**](windowsribbon-element-splitbutton.md)o [**SplitButtonGallery.**](windowsribbon-element-splitbuttongallery.md)

**DropDownButton** supporta le [modalità dell'applicazione](ribbon-applicationmodes.md) quando è ospitato nella colonna sinistra del menu dell'applicazione.

[**DropDownGallery e**](windowsribbon-element-dropdowngallery.md) [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) non sono elementi figlio validi di **DropDownButton** quando **DropDownButton** è un discendente di [**ApplicationMenu.**](windowsribbon-element-applicationmenu.md)

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per **DropDownButton**.

Questa sezione di codice illustra le dichiarazioni del comando **DropDownButton,** con un [**gruppo**](windowsribbon-element-group.md) associato che funziona come contenitore padre per **l'elemento DropDownButton.**


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



Questa sezione di codice illustra le **dichiarazioni del controllo DropDownButton.**


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

* **Sistema minimo supportato:** Windows 7
* **Può essere vuoto:** No



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo Pulsante a discesa](windowsribbon-controls-dropdownbutton.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

