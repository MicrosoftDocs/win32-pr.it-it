---
title: Command.TooltipDescription - proprietà
description: Rappresenta una descrizione comando.
ms.assetid: 2d3ea497-2d96-4420-8fcf-39ac2c472bf1
keywords:
- Proprietà Command.TooltipDescription Windows barra multifunzione
topic_type:
- apiref
api_name:
- Command.TooltipDescription
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5dd356ae3bcfa5949e8469240330a3a09a11f01b5a919ed02f4eb55683fbc15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933211"
---
# <a name="commandtooltipdescription-property"></a>Command.TooltipDescription - proprietà

Rappresenta una descrizione comando.

## <a name="usage"></a>Utilizzo

``` syntax
<Command.TooltipDescription>
  child elements
</Command.TooltipDescription>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                   | Descrizione                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [**Stringa**](windowsribbon-element-string.md)<br/> | Può verificarsi al massimo una volta<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



| Elemento                                                     |
|-------------------------------------------------------------|
| [**Comando**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi al massimo una volta per ogni [**comando**](windowsribbon-element-command.md).

**Command.TooltipDescription può** contenere un valore di tipo *xs:string* vincolato a qualsiasi sequenza di caratteri, inclusi gli spazi vuoti e i caratteri di interruzione di riga .

> [!Note]  
> Usare il riferimento ai caratteri XML del set di caratteri universali (UCS) `&#xA;` per specificare un'interruzione di riga.

 

La lunghezza massima è illimitata.

Se non viene specificato alcun valore per **Command.TooltipDescription**, [**l'elemento**](windowsribbon-element-string.md) figlio String è obbligatorio.

> [!Note]  
> Se **Command.TooltipDescription contiene** sia un valore che un elemento figlio [**String,**](windowsribbon-element-string.md) **String** ha la precedenza.

 

**Command.TooltipDescription supporta** solo l'allineamento a sinistra.

## <a name="examples"></a>Esempio

L'esempio seguente illustra il markup per un [**elemento Command**](windowsribbon-element-command.md) con una **dichiarazione Command.TooltipDescription.**


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



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 





