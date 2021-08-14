---
title: Elemento ComboBox
description: Rappresenta un controllo Casella combinata.
ms.assetid: d796e26b-44c2-4e11-b1a5-2ede5bcff676
keywords:
- Elemento ComboBox Windows barra multifunzione
topic_type:
- apiref
api_name:
- ComboBox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 60ee7a03d25508df45469577f4d4159b5db5f5190f188ca594b71f176d037526
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117851191"
---
# <a name="combobox-element"></a>Elemento ComboBox

Rappresenta un [controllo Casella](windowsribbon-controls-combobox.md) combinata.

## <a name="usage"></a>Utilizzo

``` syntax
<ComboBox
  CommandName = "xs:positiveInteger or xs:string"
  IsEditable = "Boolean"
  ResizeType = "ComboBoxResizeType"
  IsAutoCompleteEnabled = "Boolean"/>
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
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger o xs:string<br/></td>
<td>No<br/></td>
<td>Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command.</strong></a><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)<br/> </dt> <dd> Stringa, valore intero compreso tra 2 e 59999 inclusi o valore esadecimale compreso tra 0x2 e 0xea5f inclusi. <br/> Il valore deve essere univoco all'interno del documento XML della barra multifunzione. <br/> Lunghezza massima: 100 caratteri. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsAutoCompleteEnabled</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Limitato a uno dei valori seguenti (0 e 1 non sono validi):<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Valore predefinito. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsEditable</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Limitato a uno dei valori seguenti (0 e 1 non sono validi):<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Valore predefinito. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ResizeType</strong><br/></td>
<td>ComboBoxResizeType<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (NoResize)<br/> </dt> <dd> Valore predefinito. <br/> </dd> <dt><span></span><span></span><strong></strong> (VerticalResize)<br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="windowsribbon-element-dropdownbutton.md"><strong>DropDownButton</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="windowsribbon-element-group.md"><strong>Group</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="windowsribbon-element-menugroup.md"><strong>Menugroup</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Windows 8 e più recente.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi una o più volte per ogni elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md)o [**SplitButtonGallery.**](windowsribbon-element-splitbuttongallery.md)

Poiché **ComboBox è** esclusivamente una raccolta di elementi, non supporta gli elementi Command. È anche l'unico controllo della raccolta che non supporta uno spazio dei comandi (una raccolta di comandi dichiarati nel markup ed elencati nella parte inferiore di una raccolta di elementi o di una raccolta di comandi). Per altre informazioni, vedere [Uso delle raccolte.](ribbon-controls-galleries.md)

Lo screenshot seguente illustra un controllo Casella combinata [della](windowsribbon-controls-combobox.md) barra multifunzione Windows Live Movie Maker.

![Screenshot di un controllo casella combinata nella barra multifunzione di Microsoft Paint.](images/controls/combobox.png)

## <a name="examples"></a>Esempio

Gli esempi seguenti illustrano il markup di base per **l'oggetto ComboBox.**

Questa sezione di codice illustra le dichiarazioni del comando **ComboBox,** con un oggetto [**Group**](windowsribbon-element-group.md) associato che funge da contenitore padre per **l'elemento ComboBox.**


```XML
<!-- ComboBox -->
<Command Name="cmdComboBoxGroup"
         Symbol="cmdComboBoxGroup"
         Comment="ComboBox Group"
         LabelTitle="ComboBox"/>
<Command Name="cmdComboBox"
         Symbol="cmdComboBox"
         Comment="ComboBox"
         LabelTitle="ComboBox"/>
```



Questa sezione di codice illustra le **dichiarazioni del controllo ComboBox.**


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



## <a name="element-information"></a>Informazioni sull'elemento

* **Sistema minimo supportato:** Windows 7
* **Può essere vuoto:** Sì



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo Combo Box](windowsribbon-controls-combobox.md)
</dt> <dt>

[Esempio di raccolta](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





