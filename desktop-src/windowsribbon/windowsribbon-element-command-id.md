---
title: Command.Id proprietà
description: Rappresenta un ID univoco per un oggetto Command.
ms.assetid: 937ca9d6-6910-4133-9cfa-d7e3f895f876
keywords:
- Command.Id proprietà Windows barra multifunzione
topic_type:
- apiref
api_name:
- Command.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50c542cbf4103c6063a177990d454a45e5f937745720c7c0a7bc5c60c4c1047e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931616"
---
# <a name="commandid-property"></a>Command.Id proprietà

Rappresenta un ID univoco per un oggetto Command.

## <a name="usage"></a>Utilizzo

``` syntax
<Command.Id/>
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

L'ID è associato a una definizione command nel file di intestazione della barra multifunzione, ad esempio `#define cmdSave 25003 /* Save */` .

Questo elemento contiene un valore dell'unione dei tipi *xs:positiveInteger* e *xs:string* vincolati a un valore intero compreso tra 2 e 59999, inclusivo o 0x2 e 0xea5f in formato esadecimale, inclusivo.

La lunghezza massima è di 10 caratteri, inclusi gli zeri iniziali facoltativi.

## <a name="examples"></a>Esempio

L'esempio seguente illustra il markup per un [**elemento Command**](windowsribbon-element-command.md) con una **Command.Id** dichiarazione.


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
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



 

 





