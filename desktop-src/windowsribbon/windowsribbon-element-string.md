---
title: Elemento String
description: Rappresenta una risorsa di stringa.
ms.assetid: 83e5bdbb-ef86-4942-af40-2e327360ee67
keywords:
- Barra multifunzione Windows elemento stringa
topic_type:
- apiref
api_name:
- String
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 577d318292081dddf4e2839967642c6115a474d6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045800"
---
# <a name="string-element"></a>Elemento String

Rappresenta una risorsa di stringa.

## <a name="usage"></a>Utilizzo

``` syntax
<String
  Content = "xs:string"
  Id = "xs:positiveInteger or xs:string"
  Symbol = "xs:string">
  child elements
</String>
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
<td><strong>Contenuto</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (XS: String)<br/> </dt> <dd> Stringa costituita da qualsiasi sequenza di caratteri, inclusi gli spazi vuoti e i caratteri di interruzioni di riga.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Id</strong><br/></td>
<td>XS: positiveInteger o xs: String<br/></td>
<td>No<br/></td>
<td>ID di risorsa univoco. <br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o xs: String)<br/> </dt> <dd> Valore intero compreso tra 2 e 59999, inclusivo o 0x2 e 0xea5f in formato esadecimale, inclusivo. <br/> La lunghezza massima è di 10 caratteri, inclusi gli zeri iniziali facoltativi. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Simbolo</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Simbolo di risorsa per la stringa.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: String)<br/> </dt> <dd> Lettera o carattere di sottolineatura seguito da qualsiasi sequenza di lettere, cifre o caratteri di sottolineatura.<br/> La lunghezza massima è di 100 caratteri.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                   | Descrizione                                   |
|---------------------------------------------------------------------------|-----------------------------------------------|
| [**String. Content**](windowsribbon-element-string-content.md)<br/> | Può verificarsi al massimo una volta<br/> <br/> |
| [**String.Id**](windowsribbon-element-string-id.md)<br/>           | Può verificarsi al massimo una volta<br/> <br/> |
| [**String. Symbol**](windowsribbon-element-string-symbol.md)<br/>   | Può verificarsi al massimo una volta<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                                           |
|---------------------------------------------------------------------------------------------------|
| [**Command. suggerimento**](windowsribbon-element-command-keytip.md)<br/>                         |
| [**Comando. LabelDescription**](windowsribbon-element-command-labeldescription.md)<br/>     |
| [**Comando. LabelTitle**](windowsribbon-element-command-labeltitle.md)<br/>                 |
| [**Comando. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)<br/> |
| [**Comando. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)<br/>             |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi al massimo una volta per ogni [**comando. LabelTitle**](windowsribbon-element-command-labeltitle.md), [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md), [**Command. suggerimento**](windowsribbon-element-command-keytip.md), [**Command. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)o [**Command. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) .

La definizione di stringa viene aggiunta al file di intestazione della barra multifunzione, ad esempio `#define strSave 59999` .

La stringa viene aggiunta a una tabella di stringhe nel file di risorse della barra multifunzione in cui un nome e un ID vengono generati dal framework della barra multifunzione se non ne viene dichiarata nessuna.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup per un elemento [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) con una dichiarazione di **stringa** .


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="element-information"></a>Informazioni sull'elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema minimo supportato<br/> | Windows 7 |
| Può essere vuoto                        | No        |



 

 





