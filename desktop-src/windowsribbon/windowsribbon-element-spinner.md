---
title: Elemento spinner
description: Rappresenta un controllo Spinner.
ms.assetid: 6a174ec9-0fde-4171-a363-0e330ac31a8b
keywords:
- Elemento casella di selezione Windows barra multifunzione
topic_type:
- apiref
api_name:
- Spinner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 847806e395998f8bc82c302f4403c5bc2b651323ec6c7089803bc66e5f18dc4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439516"
---
# <a name="spinner-element"></a>Elemento spinner

Rappresenta un [controllo Spinner.](windowsribbon-controls-spinner.md)

## <a name="usage"></a>Uso

``` syntax
<Spinner
  CommandName = "xs:positiveInteger or xs:string"/>
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
<td>Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)<br/> </dt> <dd> Stringa, valore intero compreso tra 2 e 59999, inclusivo o valore esadecimale compreso tra 0x2 e 0xea5f, inclusi. <br/> Il valore deve essere univoco all'interno del documento XML della barra multifunzione. <br/> Lunghezza massima: 100 caratteri. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                           |
|-----------------------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>             |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Group**](windowsribbon-element-group.md)<br/>                           |
| [**Menugroup**](windowsribbon-element-menugroup.md)<br/>                   |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi una o più volte per ogni [**elemento ControlGroup**](windowsribbon-element-controlgroup.md) [**o Group.**](windowsribbon-element-group.md)

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per [spinner](windowsribbon-controls-spinner.md).

Questa sezione di codice illustra le **dichiarazioni di Comando spinner,** con un [**elemento Group**](windowsribbon-element-group.md) che funziona come contenitore padre per l'elemento **Spinner.**


```XML
<Command Name="GroupSpinner1" Symbol="IDR_CMD_GROUPSPINNER1" Id="30010">
  <Command.LabelTitle>
    <String Id="210">Resize</String>
  </Command.LabelTitle>
</Command>
<Command Name="Spinner_Size" Symbol="IDR_CMD_SPINNER_RESIZE" Id="30015">
  <Command.LabelTitle>
    <String Id="215">Resize by:</String>
  </Command.LabelTitle>
</Command>
```



Questa sezione di codice illustra le **dichiarazioni del controllo Spinner.**


```XML
<Group CommandName="GroupSpinner1">
  <Spinner CommandName="Spinner_Size" />
</Group>
```



## <a name="element-information"></a>Informazioni sull'elemento

- **Sistema minimo supportato:** Windows 7 
- **Può essere vuoto:** Sì



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo spinner](windowsribbon-controls-spinner.md)
</dt> </dl>

 

 





