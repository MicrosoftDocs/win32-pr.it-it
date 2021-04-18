---
title: Proprietà Command. Symbol
description: Rappresenta il nome di un comando a cui è possibile fare riferimento esternamente.
ms.assetid: affa5f3f-f641-4bec-9165-6102509cf355
keywords:
- Barra multifunzione di Windows Command. Symbol
topic_type:
- apiref
api_name:
- Command.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88dccb71a90feca7348ca9731ca5966b012c9c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302311"
---
# <a name="commandsymbol-property"></a>Proprietà Command. Symbol

Rappresenta il nome di un [**comando**](windowsribbon-element-command.md) a cui è possibile fare riferimento esternamente.

## <a name="usage"></a>Utilizzo

``` syntax
<Command.Symbol/>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                                                     |
|-------------------------------------------------------------|
| [**Comando**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi al massimo una volta per ogni [**comando**](windowsribbon-element-command.md).

Il simbolo è associato a una definizione di comando nel file di intestazione della barra multifunzione, ad esempio `#define cmdSave 25003 /* Save */` .

Questo elemento contiene un valore di tipo *xs: String*.

Il valore è vincolato a una stringa costituita da una lettera o un carattere di sottolineatura seguito da una sequenza di lettere, cifre e caratteri di sottolineatura.

La lunghezza massima è di 100 caratteri.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup per un elemento [**Command**](windowsribbon-element-command.md) con una Dichiarazione **Command. Symbol** .


```XML
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



 

 





