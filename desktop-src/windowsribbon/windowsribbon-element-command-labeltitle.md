---
title: Proprietà Command. LabelTitle
description: Rappresenta il titolo di un'etichetta.
ms.assetid: 97378ec3-7988-4e39-9cf5-c382b246c5c9
keywords:
- Barra multifunzione di Windows Command. LabelTitle
topic_type:
- apiref
api_name:
- Command.LabelTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed6d6c72ddd60cca63834fdcf21cf8f8b726ad22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518688"
---
# <a name="commandlabeltitle-property"></a>Proprietà Command. LabelTitle

Rappresenta il titolo di un'etichetta.

## <a name="usage"></a>Utilizzo

``` syntax
<Command.LabelTitle>
  child elements
</Command.LabelTitle>
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

**Command. LabelTitle** può contenere un valore di tipo *xs: String* vincolato a qualsiasi sequenza di caratteri, inclusi gli spazi vuoti e i caratteri di interruzioni di riga.

> [!Note]  
> Usare il riferimento al carattere XML UCS (Universal Character Set) `&#xA;` per specificare un'interruzioni di riga.

 

La lunghezza massima è unbounded.

Se non viene specificato alcun valore per **Command. LabelTitle**, l'elemento figlio [**stringa**](windowsribbon-element-string.md) è obbligatorio.

> [!Note]  
> Se **Command. LabelTitle** contiene sia un elemento Value che un elemento figlio [**String**](windowsribbon-element-string.md) , la **stringa** avrà la precedenza.

 

**Command. LabelTitle** supporta solo l'allineamento a sinistra.

Se un comando viene esposto tramite una voce di menu e il valore di **Command. LabelTitle** o dell' [ \_ \_ etichetta pkey dell'interfaccia utente](windowsribbon-reference-properties-uipkey-label.md) contiene una lettera preceduta da una e commerciale, come illustrato nell'esempio seguente, questa lettera viene considerata come un tasto di scelta rapida e un tasto di scelta rapida per tale comando dal framework della barra multifunzione.


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



Per visualizzare una e commerciale in un'etichetta, eseguire l'escape della designazione del carattere speciale con una doppia e commerciale ( `&&` ), come illustrato nell'esempio seguente.


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup per un elemento [**Command**](windowsribbon-element-command.md) con una Dichiarazione **Command. LabelTitle** .


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



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[\_Etichetta pkey dell'interfaccia utente \_](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 





