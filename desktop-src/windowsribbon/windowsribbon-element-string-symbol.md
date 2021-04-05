---
title: Proprietà String. Symbol
description: Rappresenta il nome di una risorsa di stringa.
ms.assetid: 7c1d0197-2c9b-4f42-afba-73fd1c366deb
keywords:
- Proprietà String. Symbol (barra multifunzione di Windows)
topic_type:
- apiref
api_name:
- String.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7bf7d30ddd8677b1c5ff0a5e55d4b9c119795ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873401"
---
# <a name="stringsymbol-property"></a>Proprietà String. Symbol

Rappresenta il nome di una risorsa di stringa.

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

Può verificarsi al massimo una volta per ogni elemento [**stringa**](windowsribbon-element-string.md) .

Il simbolo è associato a una definizione di stringa nel file di intestazione della barra multifunzione, ad esempio `#define strSave 59999` .

Questo elemento contiene un valore di tipo *xs: String*. Il valore è vincolato a una stringa costituita da una lettera o un carattere di sottolineatura seguito da una sequenza di lettere, cifre o caratteri di sottolineatura.

La lunghezza massima è di 100 caratteri.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup per un elemento [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) con una Dichiarazione **String. Symbol** .


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



 

 





