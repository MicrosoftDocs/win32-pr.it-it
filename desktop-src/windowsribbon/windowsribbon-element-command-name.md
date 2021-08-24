---
title: Command.Name proprietà
description: Rappresenta il nome di un oggetto Command.
ms.assetid: 36fb0b93-143f-4706-8c32-e6c818cce16f
keywords:
- Command.Name proprietà Windows barra multifunzione
topic_type:
- apiref
api_name:
- Command.Name
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48162c5edda2dd8787518ce7042a8ae8eeb349ff332488cd834d10b377d96a0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587751"
---
# <a name="commandname-property"></a>Command.Name proprietà

Rappresenta il nome di un oggetto Command.

## <a name="usage"></a>Utilizzo

``` syntax
<Command.Name/>
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

**Command.Name** viene fatto riferimento nel markup per associare un oggetto Command a un controllo tramite *l'attributo CommandName* del controllo.

Questo elemento contiene un valore di tipo *xs:string*.

Il valore è vincolato a una stringa costituita da una lettera o un carattere di sottolineatura seguito da qualsiasi sequenza di lettere, cifre e caratteri di sottolineatura.

La lunghezza massima è di 100 caratteri.

## <a name="examples"></a>Esempio

L'esempio seguente illustra il markup per un [**elemento Command**](windowsribbon-element-command.md) con una **Command.Name** dichiarazione.


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



 

 





