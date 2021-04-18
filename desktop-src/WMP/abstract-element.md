---
title: ABSTRACT (elemento)
description: L'elemento astratto contiene testo che descrive l'elemento ASX, BANNER o ENTRY associato.
ms.assetid: 7866fee8-1778-433a-be2f-9df0baa1c13e
keywords:
- Media Player di Windows elemento astratto
topic_type:
- apiref
api_name:
- ABSTRACT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e90b6f52b697242be23303ab3597dac549a6177
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330903"
---
# <a name="abstract-element"></a>ABSTRACT (elemento)

L'elemento **astratto** contiene testo che descrive l'elemento **ASX**, **banner** o **entry** associato.

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
| Padre    | **ASX**, **voce**, **banner** |
| Figlio     | nessuno                           |



 

## <a name="remarks"></a>Osservazioni

Se questo elemento viene visualizzato all'interno di un elemento **ASX** , il testo viene visualizzato come descrizione comando quando il mouse viene posizionato sul titolo della visualizzazione.

Se questo elemento viene visualizzato all'interno di un elemento **entry** , il testo viene visualizzato come descrizione comando quando il mouse viene posizionato sul titolo della clip.

Se questo elemento viene visualizzato all'interno di un elemento **banner** , il testo viene visualizzato come descrizione comando per l'icona del banner.

Usare un solo elemento **astratto** per ambito. Quando viene elaborato un file Metafile, viene utilizzato solo il primo elemento **astratto** nell'ambito di un altro elemento. Tutti gli elementi **astratti** successivi in tale ambito vengono ignorati.

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

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informazioni di riferimento sui metafile di Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





