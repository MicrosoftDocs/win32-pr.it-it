---
title: Elemento AUTHOR
description: L'elemento AUTHOR contiene il nome dell'autore di un metafile di Windows Media o di un clip multimediale.
ms.assetid: d80aad3d-4471-4310-8d43-2733ed83103c
keywords:
- Elemento AUTHOR Windows Media Player
topic_type:
- apiref
api_name:
- AUTHOR Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d20498ebd7c8a56edc2e32bc2e76422c9b22242
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325267"
---
# <a name="author-element"></a>Elemento AUTHOR

L'elemento **Author** contiene il nome dell'autore di un metafile di Windows Media o di un clip multimediale.

``` syntax
<AUTHOR>   
   text string
</AUTHOR>
```

## <a name="attributes"></a>Attributi

Questo elemento non ha attributi.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elemento            |
|-----------------|--------------------|
| Elementi padre | **ASX**, **voce** |
| Elementi figlio  | nessuno               |



 

## <a name="remarks"></a>Osservazioni

Questo elemento contiene una stringa di testo che rappresenta il nome dell'autore di un metafile Windows Media o di un clip multimediale. È possibile utilizzare l'elemento **Author** all'interno dell'elemento **ASX** e negli elementi **entry** .

Se questo elemento viene visualizzato nell'elemento **ASX** , il testo viene visualizzato come **Mostra** informazioni.

Se questo elemento viene visualizzato in un elemento **entry** , il testo viene visualizzato come autore della clip.

Ogni elemento **ASX** e **entry** padre deve contenere al massimo un elemento **autore** figlio. Più elementi **Author** dopo il primo verranno ignorati e non verranno visualizzati.

## <a name="examples"></a>Esempio


```XML
<ASX VERSION="3.0">
   <AUTHOR>Neal S.</AUTHOR>   <!-- Show author -->
   <ENTRY>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
      <AUTHOR>Robert P.</AUTHOR>  <!-- Clip author -->
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

 

 





