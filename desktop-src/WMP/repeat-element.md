---
title: Elemento REPEAT
description: L'elemento REPEAT definisce il numero di volte in cui Windows Media Player ripete uno o più elementi ENTRY o ENTRYREF.
ms.assetid: 1a825f2b-29a7-4180-93df-51b3b5dd14e5
keywords:
- Ripeti finestre elementi Media Player
topic_type:
- apiref
api_name:
- REPEAT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aff7d5eaa9594882b029f0b02f4888d93fff01d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331584"
---
# <a name="repeat-element"></a>Elemento REPEAT

L'elemento **Repeat** definisce il numero di volte in cui Windows Media Player ripete uno o più elementi **entry** o **ENTRYREF** .

``` syntax
<REPEAT   
   COUNT = "integer"
>
</REPEAT>
```

## <a name="attributes"></a>Attributi

**COUNT**

Integer che rappresenta il numero di volte in cui Windows Media Player ripete gli elementi **entry** e **ENTRYREF** all'interno dell'ambito di questo elemento.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elementi                |
|-----------------|-------------------------|
| Elementi padre | **ASX**                 |
| Elementi figlio  | **voce**, **ENTRYREF** |



 

## <a name="remarks"></a>Commenti

Questo elemento definisce il numero di volte in cui Windows Media Player ripete o scorre i clip definiti dalla **voce** e **ENTRYREF** gli elementi all'interno dell'ambito di questo elemento. Solo il primo elemento **Repeat** in un metafile è valido. gli elementi **ripetuti** successivi vengono ignorati.

Se non è definito alcun attributo **count** , il contenuto negli elementi **entry** e **ENTRYREF** associati si ripete un numero infinito di volte. Il valore zero fa in modo che Windows Media Player ignori l'elemento **Repeat** e riproduca il contenuto una volta.

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

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informazioni di riferimento sui metafile di Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





