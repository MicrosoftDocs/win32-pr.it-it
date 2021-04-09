---
title: Proprietà String.Id
description: Rappresenta l'ID univoco di una risorsa di stringa.
ms.assetid: 393da279-bdf6-4796-a546-1931cbe49113
keywords:
- Barra multifunzione di Windows proprietà String.Id
topic_type:
- apiref
api_name:
- String.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3ab87327ed4f11a901fb8a201e72137ab62c7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121066"
---
# <a name="stringid-property"></a>Proprietà String.Id

Rappresenta l'ID univoco di una risorsa di stringa.

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

Può verificarsi al massimo una volta per ogni elemento [**stringa**](windowsribbon-element-string.md) .

Il valore di **String.ID** deve essere univoco.

L'ID è associato a una definizione di stringa nel file di intestazione della barra multifunzione, ad esempio `#define strSave 59999` .

Questo elemento contiene un valore dall'Unione dei tipi *xs: positiveInteger* e *xs: String*. Il valore è vincolato a un valore intero compreso tra 2 e 59999, inclusivi o 0x2 e 0xea5f in formato esadecimale, inclusivo.

La lunghezza massima è di 10 caratteri con zeri iniziali facoltativi.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup per un elemento [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) con una Dichiarazione **String.ID** .


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
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



 

 





