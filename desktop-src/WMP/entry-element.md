---
title: Elemento ENTRY
description: L'elemento ENTRY specifica un file di Windows Media da visualizzare come clip.
ms.assetid: 7fd16aff-2eed-4f95-92b3-b48a9d785e7c
keywords:
- Elemento ENTRY Media Player Windows
topic_type:
- apiref
api_name:
- ENTRY Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 13da18c72022c916f91bcffe7382f673ba3d4fa4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333245"
---
# <a name="entry-element"></a>Elemento ENTRY

L'elemento **entry** specifica un file di Windows Media da visualizzare come clip.

``` syntax
<ENTRY
   CLIENTSKIP = "YES" | "NO"
   SKIPIFREF = "YES" | "NO"
>
</ENTRY>
```

## <a name="attributes"></a>Attributi

**CLIENTSKIP**

Valore che indica se l'utente può andare avanti oltre il clip.

Di seguito sono indicati alcuni valori possibili.



| Valore | Descrizione                                   |
|-------|-----------------------------------------------|
| YES   | Valore predefinito. L'utente può andare avanti oltre il clip. |
| NO    | L'utente non può andare avanti oltre il clip.       |



 

**SKIPIFREF**

Valore che indica se Windows Media Player deve ignorare questa clip quando l'elemento **entry** viene incluso in un secondo metafile mediante l'utilizzo di un elemento **ENTRYREF** .

Di seguito sono indicati alcuni valori possibili.



| Valore | Descrizione                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| YES   | Windows Media Player ignorerà questa voce, se vi viene fatto riferimento tramite un elemento **ENTRYREF** . |
| NO    | Valore predefinito. Questa voce non verrà ignorata da Windows Media Player.                                   |



 

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi                                                                                                                                                                                     |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementi padre | **ASX**, **evento**, **ripetizione**                                                                                                                                                               |
| Elementi figlio  | **abstract**, **Author**, **banner**, **base**, **Copyright**, **Duration**, **ENDMARKER**, **moreinfo**, **param**, **PREVIEWDURATION**, **ref**, **STARTMARKER**, **StartTime**, **title** |



 

## <a name="remarks"></a>Commenti

Questo elemento è il costrutto fondamentale in un metafile di Windows Media. L'elemento **entry** e gli attributi associati definiscono le metainformazioni per una singola parte logica di contenuto, denominata clip. Gli elementi figlio all'interno dell'ambito di un elemento **entry** definiscono il contenuto multimediale per Windows Media Player per aprire (**ref**), informazioni sul clip che Windows Media Player visualizzerà come testo (**autore**, **Copyright**, **titolo**) e altre impostazioni correlate alla clip. L'elemento figlio **ref** collega il contenuto da trasmettere per l'elemento **entry** padre. Sebbene lo script non venga interrotta, la **voce** non è significativa senza un elemento figlio **ref** .

Se il valore dell'attributo **CLIENTSKIP** è No, l'utente non può andare avanti oltre il contenuto definito dall'elemento **entry** . Questa operazione non funziona se l'elemento **ref** figlio fa riferimento a un altro metafile. È necessario fare riferimento ai metafile annidati usando l'elemento **ENTRYREF** .

L'attributo **SKIPIFREF** riguarda solo gli elementi **entry** inclusi in un secondo metafile tramite l'uso di un elemento **ENTRYREF** . L'elemento **ENTRYREF** fa riferimento a un altro metafile per l'inclusione logica nel file corrente. Se il valore dell'attributo **SKIPIFREF** per un elemento **entry** dal file Metafile a cui si fa riferimento è Yes, Windows Media Player ignora questa voce di cui è stato eseguito il pull e passa all'elemento **entry** successivo, se presente. L'elemento **entry** successivo può essere la voce successiva nel file originale o la voce successiva nel metafile a cui si fa riferimento nell'elemento **ENTRYREF** .

## <a name="examples"></a>Esempio


```XML
<ASX VERSION="3.0">
   <TITLE>Example Windows Media Player Show</TITLE>
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <REF HREF="https://example.microsoft.com/media.asf" />
   </ENTRY>
   
   <ENTRY>
      <TITLE>Another Clip</TITLE>
      <REF HREF="https://example.microsoft.com/more_media.asf" />
   </ENTRY>
</ASX>

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------|
| Versione<br/> | Windows Media Player versione 70 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informazioni di riferimento sui metafile di Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





