---
title: String.Id proprietà
description: Rappresenta l'ID univoco di una risorsa stringa.
ms.assetid: 393da279-bdf6-4796-a546-1931cbe49113
keywords:
- String.Id proprietà Windows ribbon
topic_type:
- apiref
api_name:
- String.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15f9c1af4ba32982ce52ba470f6b3d1996abe11c81bdd520a4e50203adb56093
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119441651"
---
# <a name="stringid-property"></a>String.Id proprietà

Rappresenta l'ID univoco di una risorsa stringa.

## <a name="usage"></a>Utilizzo

``` syntax
<String.Id/>
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

Il valore per **String.Id** deve essere univoco.

L'ID è associato a una definizione di stringa nel file di intestazione della barra multifunzione, ad esempio `#define strSave 59999` .

Questo elemento contiene un valore dall'unione dei tipi *xs:positiveInteger* *e xs:string*. Il valore è vincolato a un valore intero compreso tra 2 e 59999, inclusivo o 0x2 e 0xea5f in formato esadecimale, inclusivo.

La lunghezza massima è di 10 caratteri con zeri iniziali facoltativi.

## <a name="examples"></a>Esempio

L'esempio seguente illustra il markup per [**un elemento Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) con una **String.Id** dichiarazione.


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



 

 





