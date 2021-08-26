---
title: Elemento REPEAT
description: L'elemento REPEAT definisce il numero di Windows Media Player ripete uno o più elementi ENTRY o ENTRYREF.
ms.assetid: 1a825f2b-29a7-4180-93df-51b3b5dd14e5
keywords:
- Elemento REPEAT Windows Media Player
topic_type:
- apiref
api_name:
- REPEAT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 330eda0757acb29b48ed10636d8f479b6ebb1395d088020876c717a78f41ae6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002541"
---
# <a name="repeat-element"></a>Elemento REPEAT

**L'elemento REPEAT** definisce il numero di Windows Media Player ripete uno o più **elementi ENTRY** **o ENTRYREF.**

``` syntax
<REPEAT   
   COUNT = "integer"
>
</REPEAT>
```

## <a name="attributes"></a>Attributi

**COUNT**

Intero che rappresenta il numero di volte Windows Media Player ripete gli elementi **ENTRY** e **ENTRYREF** all'interno dell'ambito di questo elemento.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi                |
|-----------------|-------------------------|
| Elementi padre | **Asx**                 |
| Elementi figlio  | **ENTRY,** **ENTRYREF** |



 

## <a name="remarks"></a>Commenti

Questo elemento definisce il numero di volte in cui Windows Media Player ripetute o scorre in ciclo le clip definite dagli elementi **ENTRY** e **ENTRYREF** all'interno dell'ambito di questo elemento. È valido solo **il primo** elemento REPEAT in un metafile. gli **elementi REPEAT** successivi vengono ignorati.

Se non è definito alcun attributo **COUNT,** il contenuto negli elementi **ENTRY** e **ENTRYREF** associati si ripete un numero infinito di volte. Se il valore è zero, Windows Media Player ignora **l'elemento REPEAT** e riproduce il contenuto una sola volta.

## <a name="examples"></a>Esempio


```XML
<ASX VERSION="3.0">
   <ENTRY>
        <REF HREF="mms://example.microsoft.com/clip1.asf" />
<!-- This clip plays once. -->
   </ENTRY>

   <REPEAT COUNT="2">
      <ENTRY>
     <REF HREF="mms://example.microsoft.com/clip2.asf" />
     <REF HREF="mms://example.microsoft.com/clip3.asf" />
 <!-- These clips play twice. -->
      </ENTRY>
   </REPEAT>
</ASX>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------|
| Versione<br/> | Windows Media Player versione 70 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Windows Informazioni di riferimento per gli elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Informazioni di riferimento sui metafile multimediali**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





