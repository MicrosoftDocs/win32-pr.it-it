---
title: Elemento RecentItems
description: Rappresenta il controllo degli elementi recenti nel menu dell'applicazione.
ms.assetid: a3df0bb0-e0f8-413a-879d-8e39164535d0
keywords:
- Barra multifunzione Windows elemento RecentItems
topic_type:
- apiref
api_name:
- RecentItems
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17269342521a5da5db8d7a852a985c29ed7e2e98
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "104046251"
---
# <a name="recentitems-element"></a>Elemento RecentItems

Rappresenta il controllo [degli elementi recenti](windowsribbon-controls-recentitems.md) nel [menu dell'applicazione](windowsribbon-controls-applicationmenu.md).

## <a name="usage"></a>Utilizzo

``` syntax
<RecentItems
  CommandName = "xs:positiveInteger or xs:string"
  MaxCount = "xs:nonNegativeInteger"
  EnablePinning = "Boolean"/>
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
<tr class="even">
<td><strong>EnablePinning</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Limitato a uno dei valori seguenti (0 e 1 non sono validi):<br/> <br/>
<dt><span></span><span></span><strong></strong> true<br/> </dt> <dd> Valore predefinito. <br/> </dd> <dt><span></span><span></span><strong></strong> false<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaxCount</strong><br/></td>
<td>xs:nonNegativeInteger<br/></td>
<td>No<br/></td>
<td>Numero di elementi recenti da visualizzare.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: nonNegativeInteger)<br/> </dt> <dd> Valore intero pari a 0 o superiore.<br/> Il valore predefinito è <strong>10</strong>.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                                             |
|-----------------------------------------------------------------------------------------------------|
| [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md)<br/> |



## <a name="remarks"></a>Commenti

Obbligatorio.

Deve essere eseguita esattamente una volta per ogni elemento [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) .

Il controllo [elementi recenti](windowsribbon-controls-recentitems.md) consente di visualizzare l'elenco degli elementi usati di recente (MRU) dell'applicazione della barra multifunzione.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per il controllo [degli elementi recenti](windowsribbon-controls-recentitems.md) .

Nell'esempio seguente viene illustrata una dichiarazione di comando **RecentItems** .


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



Nell'esempio seguente viene illustrata la dichiarazione di controlli **RecentItems** associati.


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="element-information"></a>Informazioni sull'elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema minimo supportato<br/> | Windows 7 |
| Può essere vuoto                        | Sì       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo menu applicazione](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[Controllo elementi recenti](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





