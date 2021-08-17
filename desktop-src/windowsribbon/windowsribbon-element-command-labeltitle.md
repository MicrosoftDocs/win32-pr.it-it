---
title: Command.LabelTitle - proprietà
description: Rappresenta il titolo di un'etichetta.
ms.assetid: 97378ec3-7988-4e39-9cf5-c382b246c5c9
keywords:
- Proprietà Command.LabelTitle Windows barra multifunzione
topic_type:
- apiref
api_name:
- Command.LabelTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44995d3f17b165c38f9fe7490a33e5d140c8d2b375d5d6b625bb00e3228b21e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810791"
---
# <a name="commandlabeltitle-property"></a>Command.LabelTitle - proprietà

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

**Command.LabelTitle** può contenere un valore di tipo *xs:string* vincolato a qualsiasi sequenza di caratteri, inclusi spazi vuoti e caratteri di interruzione di riga.

> [!Note]  
> Usare il riferimento ai caratteri XML del set di caratteri universali (UCS) `&#xA;` per specificare un'interruzione di riga.

 

La lunghezza massima è illimitata.

Se non viene specificato alcun valore per **Command.LabelTitle**, [**l'elemento**](windowsribbon-element-string.md) figlio String è obbligatorio.

> [!Note]  
> Se **Command.LabelTitle contiene** sia un valore che un elemento figlio [**String,**](windowsribbon-element-string.md) **String** ha la precedenza.

 

**Command.LabelTitle** supporta solo l'allineamento a sinistra.

Se un comando viene esposto tramite una voce di menu e il valore di **Command.LabelTitle** o [UI \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md) contiene una lettera preceduta da una e commerciale, come illustrato nell'esempio seguente, questa lettera viene considerata sia come suggerimento tasto di scelta che come tasto di scelta rapida per tale comando dal framework della barra multifunzione.


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



Per visualizzare una e commerciale in un'etichetta, eseguire l'escape della designazione del carattere speciale con una doppia e commerciale ( ) come `&&` illustrato nell'esempio seguente.


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="examples"></a>Esempio

L'esempio seguente illustra il markup per [**un elemento Command**](windowsribbon-element-command.md) con una dichiarazione **Command.LabelTitle.**


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

[Etichetta \_ PKEY \_ dell'interfaccia utente](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 





