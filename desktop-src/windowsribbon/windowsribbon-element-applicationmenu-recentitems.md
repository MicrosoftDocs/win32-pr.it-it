---
title: Proprietà ApplicationMenu. RecentItems
description: Rappresenta un contenitore per il controllo degli elementi recenti nel menu dell'applicazione.
ms.assetid: 26ed38b6-17de-423f-a113-ccbaf3780a91
keywords:
- Barra multifunzione di Windows ApplicationMenu. RecentItems
topic_type:
- apiref
api_name:
- ApplicationMenu.RecentItems
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 473ab6436eabd7fcbbbfb533a8ae4afc07098c81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400659"
---
# <a name="applicationmenurecentitems-property"></a>Proprietà ApplicationMenu. RecentItems

Rappresenta un contenitore per il controllo [degli elementi recenti](windowsribbon-controls-recentitems.md) nel [menu dell'applicazione](windowsribbon-controls-applicationmenu.md).

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
<td>XS: positiveInteger o xs: String<br/></td>
<td>No<br/></td>
<td>Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o xs: String)<br/> </dt> <dd> Stringa, valore intero compreso tra 2 e 59999, inclusivo o un valore esadecimale compreso tra 0x2 e 0xea5f, inclusi. <br/> Il valore deve essere univoco all'interno del documento XML della barra multifunzione. <br/> Lunghezza massima: 100 caratteri. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                             | Descrizione                                    |
|---------------------------------------------------------------------|------------------------------------------------|
| [**RecentItems**](windowsribbon-element-recentitems.md)<br/> | Deve verificarsi esattamente una volta<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                     |
|-----------------------------------------------------------------------------|
| [**ApplicationMenu**](windowsribbon-element-applicationmenu.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi al massimo una volta per ogni elemento [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) .

Il controllo [elementi recenti](windowsribbon-controls-recentitems.md) consente di visualizzare l'elenco degli elementi usati di recente (MRU) dell'applicazione della barra multifunzione.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per il controllo [degli elementi recenti](windowsribbon-controls-recentitems.md) .

Nell'esempio seguente viene illustrata una dichiarazione di comando [**RecentItems**](windowsribbon-element-recentitems.md) .


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



Nell'esempio seguente viene illustrata la Dichiarazione **ApplicationMenu. RecentItems** e [**RecentItems**](windowsribbon-element-recentitems.md) Controls associata.


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo menu applicazione](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[Controllo elementi recenti](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





