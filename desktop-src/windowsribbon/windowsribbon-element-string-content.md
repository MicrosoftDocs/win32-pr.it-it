---
title: Proprietà String.Content
description: Rappresenta il contenuto di una risorsa stringa.
ms.assetid: 86f34cdc-1311-4f52-979f-201d71bbb9e9
keywords:
- Proprietà String.Content Windows ribbon
topic_type:
- apiref
api_name:
- String.Content
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 526062956c6ab7498caac8712ba932d6e7ac1f2dd6307359183d2529e35fc8a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439506"
---
# <a name="stringcontent-property"></a>Proprietà String.Content

Rappresenta il contenuto di una risorsa stringa.

## <a name="usage"></a>Uso

``` syntax
<String.Content/>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                                                   |
|-----------------------------------------------------------|
| [**Stringa**](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi al massimo una volta per [**ogni elemento**](windowsribbon-element-string.md) String.

Questo elemento contiene un valore di tipo *xs:string*. Il valore è vincolato a una stringa composta da qualsiasi sequenza di caratteri, inclusi spazi vuoti e caratteri di interruzione di riga.

La lunghezza massima è illimitata.

## <a name="examples"></a>Esempio

L'esempio seguente illustra il markup per [**un elemento Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) con una **dichiarazione String.Content.**


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



 

 





