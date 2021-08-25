---
title: Elemento ABSTRACT
description: L'elemento ABSTRACT contiene testo che descrive l'elemento ASX, BANNER o ENTRY associato.
ms.assetid: 7866fee8-1778-433a-be2f-9df0baa1c13e
keywords:
- Elemento ABSTRACT Windows Media Player
topic_type:
- apiref
api_name:
- ABSTRACT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 153759dbe4bef47693cba13549b58215e4992686eab81cdcb4dadb33aa30279f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903051"
---
# <a name="abstract-element"></a>Elemento ABSTRACT

**L'elemento ABSTRACT** contiene testo che descrive l'elemento **ASX,** **BANNER** o **ENTRY** associato.

``` syntax
<ABSTRACT>
   text string
</ABSTRACT>
      
```

## <a name="attributes"></a>Attributi

Questo elemento non ha attributi.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia | Elementi                       |
|-----------|--------------------------------|
| Padre    | **ASX,** **ENTRY,** **BANNER** |
| Figlio     | nessuno                           |



 

## <a name="remarks"></a>Osservazioni

Se questo elemento viene visualizzato all'interno di un elemento **ASX,** il testo viene visualizzato come descrizione comando quando il puntatore del mouse viene posizionato sul titolo della presentazione.

Se questo elemento viene visualizzato all'interno di un **elemento ENTRY,** il testo viene visualizzato come descrizione comando quando il puntatore del mouse viene posizionato sul titolo del clip.

Se questo elemento viene visualizzato all'interno di **un elemento BANNER,** il testo viene visualizzato come descrizione comando per l'immagine del banner.

Usare un solo **elemento ABSTRACT** per ogni ambito. Quando viene elaborato un file metafile, viene usato solo il primo elemento **ABSTRACT** nell'ambito di un altro elemento. Tutti gli **elementi ABSTRACT** successivi nell'ambito vengono ignorati.

## <a name="examples"></a>Esempio


```XML
<ASX VERSION="3.0">
    <TITLE>The Title of the Show<TITLE>
    <ABSTRACT>
        Brief description of the show. 
    </ABSTRACT>

<ENTRY>    
    <REF HREF="YourMediaFilename.asf" />
    <TITLE>The Title of the Track</TITLE>
    <ABSTRACT>
        Brief description of the track.
    </ABSTRACT>
</ENTRY>
</ASX>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------|
| Versione<br/> | Windows Media Player versione 70 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Windows Informazioni di riferimento su elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Informazioni di riferimento sui metafile multimediali**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





