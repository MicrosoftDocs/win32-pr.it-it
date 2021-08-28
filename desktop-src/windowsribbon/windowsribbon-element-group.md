---
title: Group - elemento
description: Rappresenta un controllo Group che funziona come contenitore per un gruppo di elementi.
ms.assetid: b0d3fcda-7165-40f4-9e57-c7ab88b31711
keywords:
- Elemento Group Windows ribbon
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 86d12ddb781ecf7e1effba1cade8eb00e92fe20b
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631369"
---
# <a name="group-element"></a>Group - elemento

Rappresenta un [controllo Group](windowsribbon-controls-group.md) che funziona come contenitore per un gruppo di elementi.

## <a name="usage"></a>Utilizzo

``` syntax
<Group
  SizeDefinition = "xs:string"
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Group>
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
<td><dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Stringa contenente un elenco delimitato da virgole di numeri interi compresi tra 0 e 31.<br/> Gli spazi vuoti sono validi e ignorati.<br/> Lunghezza massima: 250 caratteri. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger o xs:string<br/></td>
<td>No<br/></td>
<td>Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command.</strong></a><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)<br/> </dt> <dd> Stringa, valore intero compreso tra 2 e 59999 inclusi o valore esadecimale compreso tra 0x2 e 0xea5f inclusi. <br/> Il valore deve essere univoco all'interno del documento XML della barra multifunzione. <br/> Lunghezza massima: 100 caratteri. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>SizeDefinition</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Se specificato, il valore di <em>SizeDefinition</em> è vincolato a uno dei modelli <a href="windowsribbon-templates.md">di layout</a> definiti dal framework della barra multifunzione. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Qualsiasi sequenza di zero o più caratteri.<br/> La lunghezza massima è illimitata.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                             | Descrizione                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Button**](windowsribbon-element-button.md)<br/>                           | Può verificarsi una o più volte<br/> <br/> |
| [**CheckBox**](windowsribbon-element-checkbox.md)<br/>                       | Può verificarsi una o più volte<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                       | Può verificarsi una o più volte<br/> <br/> |
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>               | Può verificarsi una o più volte<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>           | Può verificarsi una o più volte<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/> | Può verificarsi una o più volte<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>         | Può verificarsi una o più volte<br/> <br/> |
| [**Controllo FontControl**](windowsribbon-element-fontcontrol.md)<br/>                 | Può verificarsi al massimo una volta<br/> <br/>      |
| [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)<br/>         | Può verificarsi una o più volte<br/> <br/> |
| [**SizeDefinition**](windowsribbon-element-sizedefinition.md)<br/>           | Può verificarsi al massimo una volta<br/> <br/>      |
| [**Spinner**](windowsribbon-element-spinner.md)<br/>                         | Può verificarsi una o più volte<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                 | Può verificarsi una o più volte<br/> <br/> |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>   | Può verificarsi una o più volte<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>               | Può verificarsi una o più volte<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                             |
|-----------------------------------------------------|
| [**TAB**](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi una o più volte per ogni [**elemento Tab.**](windowsribbon-element-tab.md)

[**Tab**](windowsribbon-element-tab.md) supporta le [modalità dell'applicazione](ribbon-applicationmodes.md).

Il markup della barra multifunzione è valido solo quando gli elementi figlio di **Group** corrispondono al modello specificato per *SizeDefinition.*

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato l'utilizzo di un modello personalizzato in un **oggetto Group.**


```
<Group CommandName="cmdCustomGroup1" SizeDefinition="CustomTemplate">
  <Button CommandName="cmdCommand1" />
</Group>
```



## <a name="element-information"></a>Informazioni sull'elemento

* **Sistema minimo supportato:** Windows 7
* **Può essere vuoto:** No



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Personalizzazione di una barra multifunzione tramite definizioni delle dimensioni e criteri di ridimensionamento](windowsribbon-templates.md)
</dt> <dt>

[Controllo Group](windowsribbon-controls-group.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

