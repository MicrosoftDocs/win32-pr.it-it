---
title: Proprietà String.Symbol
description: Rappresenta il nome di una risorsa stringa.
ms.assetid: 7c1d0197-2c9b-4f42-afba-73fd1c366deb
keywords:
- Proprietà String.Symbol Windows ribbon
topic_type:
- apiref
api_name:
- String.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe6c071461fcdeb5f2bbbdbb15fce0f3f6e6031edddf4bd18e034416ba8c49e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706862"
---
# <a name="stringsymbol-property"></a>Proprietà String.Symbol

Rappresenta il nome di una risorsa stringa.

## <a name="usage"></a>Utilizzo

``` syntax
<String.Symbol/>
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

Il simbolo è associato a una definizione di stringa nel file di intestazione della barra multifunzione, ad esempio `#define strSave 59999` .

Questo elemento contiene un valore di tipo *xs:string*. Il valore è vincolato a una stringa composta da una lettera o un carattere di sottolineatura seguito da qualsiasi sequenza di lettere, cifre o caratteri di sottolineatura.

La lunghezza massima è di 100 caratteri.

## <a name="examples"></a>Esempio

L'esempio seguente illustra il markup per [**un elemento Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) con **una dichiarazione String.Symbol.**


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



 

 





