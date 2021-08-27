---
title: ApplicationMenu.RecentItems - proprietà
description: Rappresenta un contenitore per il controllo Elementi recenti nel menu dell'applicazione.
ms.assetid: 26ed38b6-17de-423f-a113-ccbaf3780a91
keywords:
- Proprietà ApplicationMenu.RecentItems Windows ribbon
topic_type:
- apiref
api_name:
- ApplicationMenu.RecentItems
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6cfb5152cd1d9cc4d27abfa3432666f06880d8e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630376"
---
# <a name="applicationmenurecentitems-property"></a>ApplicationMenu.RecentItems - proprietà

Rappresenta un contenitore per il [controllo Elementi](windowsribbon-controls-recentitems.md) recenti nel [menu dell'applicazione](windowsribbon-controls-applicationmenu.md).

## <a name="usage"></a>Utilizzo

``` syntax
<ApplicationMenu.RecentItems
  CommandName = "xs:positiveInteger or xs:string"
>
  child elements
</ApplicationMenu.RecentItems>
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
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger o xs:string<br/></td>
<td>No<br/></td>
<td>Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)<br/> </dt> <dd> Stringa, valore intero compreso tra 2 e 59999, inclusivo o valore esadecimale compreso tra 0x2 e 0xea5f, inclusi. <br/> Il valore deve essere univoco all'interno del documento XML della barra multifunzione. <br/> Lunghezza massima: 100 caratteri. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                             | Descrizione                                    |
|---------------------------------------------------------------------|------------------------------------------------|
| [**Elementi recenti**](windowsribbon-element-recentitems.md)<br/> | Deve verificarsi esattamente una volta<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                     |
|-----------------------------------------------------------------------------|
| [**ApplicationMenu**](windowsribbon-element-applicationmenu.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi al massimo una volta per [**ogni elemento ApplicationMenu.**](windowsribbon-element-applicationmenu.md)

Il [controllo Elementi recenti](windowsribbon-controls-recentitems.md) visualizza l'elenco degli elementi usati più di recente dell'applicazione barra multifunzione.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per il [controllo Elementi](windowsribbon-controls-recentitems.md) recenti.

L'esempio seguente illustra una [**dichiarazione RecentItems**](windowsribbon-element-recentitems.md) Command.


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



L'esempio seguente illustra la **dichiarazione dei controlli ApplicationMenu.RecentItems** e [**RecentItems**](windowsribbon-element-recentitems.md) associati.


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo Menu dell'applicazione](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[Controllo Elementi recenti](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





