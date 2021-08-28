---
title: Elemento AUTHOR
description: L'elemento AUTHOR contiene il nome dell'autore di un Windows o di un clip multimediale.
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
ms.openlocfilehash: 058753d73049debe01e442f49bf12476642111549ad890e931100026badaeb3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098891"
---
# <a name="author-element"></a>Elemento AUTHOR

**L'elemento AUTHOR** contiene il nome dell'autore di un Windows o di un clip multimediale.

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
| Elementi padre | **ASX**, **ENTRY** |
| Elementi figlio  | nessuno               |



 

## <a name="remarks"></a>Osservazioni

Questo elemento contiene una stringa di testo che rappresenta il nome dell'autore di un Windows o di un clip multimediale. È possibile usare **l'elemento AUTHOR** all'interno **dell'elemento ASX** e all'interno **degli elementi ENTRY.**

Se questo elemento viene visualizzato **nell'elemento ASX,** il testo viene visualizzato come **Mostra** informazioni.

Se questo elemento viene visualizzato in un **elemento ENTRY,** il testo viene visualizzato come autore del clip.

Ogni elemento **ASX e** **ENTRY** padre deve contenere al massimo un elemento **AUTHOR** figlio. Più **elementi AUTHOR** dopo il primo verranno ignorati e non verranno visualizzati.

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

[**Windows Informazioni di riferimento per gli elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Informazioni di riferimento sui metafile multimediali**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





