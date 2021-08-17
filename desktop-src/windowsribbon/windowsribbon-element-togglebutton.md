---
title: Elemento ToggleButton
description: Rappresenta un controllo Toggle Button.
ms.assetid: f26a90e6-9e9a-4fde-8753-50b8b1d09f80
keywords:
- Elemento ToggleButton Windows ribbon
topic_type:
- apiref
api_name:
- ToggleButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e17c4f9ea6aa557db6c1f9b98aca60b6da351936a70b783a0618217c03ba7b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119441591"
---
# <a name="togglebutton-element"></a>Elemento ToggleButton

Rappresenta un [controllo Toggle Button.](windowsribbon-controls-togglebutton.md)

## <a name="usage"></a>Utilizzo

``` syntax
<ToggleButton
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
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
<td><strong>ApplicationDefaults.IsChecked</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Questo attributo è valido solo quando <strong>l'elemento ToggleButton</strong> è un elemento figlio di <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults.</strong></a> <br/> Limitato a uno dei valori seguenti:<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Valore predefinito. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd></dd> </dl></td>
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

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [**Group**](windowsribbon-element-group.md)<br/>                                                                   |
| [**Menugroup**](windowsribbon-element-menugroup.md)<br/>                                                           |
| [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [**SplitButton.ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md)<br/>                                 |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a>Commenti

Facoltativo o obbligatorio, a seconda dell'elemento padre.

Può verificarsi al massimo una volta per [**ogni elemento SplitButton.ButtonItem.**](windowsribbon-element-splitbutton-buttonitem.md)

Può verificarsi una o più volte per ogni elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md)o [**SplitButtonGallery.**](windowsribbon-element-splitbuttongallery.md)

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per **l'elemento ToggleButton.**

Questa sezione di codice illustra una dichiarazione **di elemento ToggleButton** all'interno dell'elemento [**QuickAccessToolbar.ApplicationDefaults.**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="element-information"></a>Informazioni sull'elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema minimo supportato<br/> | Windows 7 |
| Può essere vuoto                        | Sì       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo Toggle Button](windowsribbon-controls-togglebutton.md)
</dt> </dl>

 

 





