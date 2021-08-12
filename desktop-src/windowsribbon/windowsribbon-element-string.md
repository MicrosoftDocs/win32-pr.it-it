---
title: Elemento String
description: Rappresenta una risorsa stringa.
ms.assetid: 83e5bdbb-ef86-4942-af40-2e327360ee67
keywords:
- Elemento String Windows ribbon
topic_type:
- apiref
api_name:
- String
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80558bed1e2152454df46d8a8dc6ab4fc40056f0257a08c91026504ec64f1722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439409"
---
# <a name="string-element"></a>Elemento String

Rappresenta una risorsa stringa.

## <a name="usage"></a>Uso

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
<td><dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Stringa composta da qualsiasi sequenza di caratteri, inclusi spazi vuoti e caratteri di interruzione di riga.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Id</strong><br/></td>
<td>xs:positiveInteger o xs:string<br/></td>
<td>No<br/></td>
<td>ID risorsa univoco. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)<br/> </dt> <dd> Valore intero compreso tra 2 e 59999, inclusivo o 0x2 e 0xea5f in formato esadecimale, inclusivo. <br/> La lunghezza massima è di 10 caratteri, inclusi gli zeri iniziali facoltativi. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Simbolo</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Simbolo di risorsa per la stringa.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Lettera o carattere di sottolineatura seguito da qualsiasi sequenza di lettere, cifre o caratteri di sottolineatura.<br/> La lunghezza massima è di 100 caratteri.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                   | Descrizione                                   |
|---------------------------------------------------------------------------|-----------------------------------------------|
| [**String.Content**](windowsribbon-element-string-content.md)<br/> | Può verificarsi al massimo una volta<br/> <br/> |
| [**String.Id**](windowsribbon-element-string-id.md)<br/>           | Può verificarsi al massimo una volta<br/> <br/> |
| [**String.Symbol**](windowsribbon-element-string-symbol.md)<br/>   | Può verificarsi al massimo una volta<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                                           |
|---------------------------------------------------------------------------------------------------|
| [**Command.Keytip**](windowsribbon-element-command-keytip.md)<br/>                         |
| [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md)<br/>     |
| [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md)<br/>                 |
| [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)<br/> |
| [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)<br/>             |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi al massimo una volta per ogni elemento [**Command.LabelTitle,**](windowsribbon-element-command-labeltitle.md) [**Command.LabelDescription,**](windowsribbon-element-command-labeldescription.md) [**Command.Keytip,**](windowsribbon-element-command-keytip.md) [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)o [**Command.TooltipDescription.**](windowsribbon-element-command-tooltipdescription.md)

La definizione di stringa viene aggiunta al file di intestazione della barra multifunzione, ad esempio `#define strSave 59999` .

La stringa viene aggiunta a una tabella di stringhe nel file di risorse della barra multifunzione in cui un nome e un ID vengono generati dal framework della barra multifunzione se non ne viene dichiarato nessuno.

## <a name="examples"></a>Esempio

L'esempio seguente illustra il markup per [**un elemento Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) con una **dichiarazione String.**


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

- **Sistema minimo supportato:** Windows 7 
- **Può essere vuoto:** No



 

 





