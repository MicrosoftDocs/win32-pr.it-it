---
title: Elemento seq
description: L'elemento seq contiene elementi che definiscono una playlist statica o elementi che definiscono una playlist intelligente.
ms.assetid: 849f7b38-25f2-4708-a83c-e651812a1a72
keywords:
- Elemento seq Windows Media Player
topic_type:
- apiref
api_name:
- seq Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d300931ac93353189e80de1a9f3a34d2e89d365026b149dc623f37c80e280fee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118833302"
---
# <a name="seq-element"></a>Elemento seq

**L'elemento seq** contiene elementi che definiscono una playlist statica o elementi che definiscono una playlist intelligente.

``` syntax
<seq>
</seq>
```

## <a name="attributes"></a>Attributi

Questo elemento non ha attributi.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia | Elementi                                                               |
|-----------|------------------------------------------------------------------------|
| Padre    | [body](body-element.md)                                               |
| Figlio     | [media,](media-element.md) [smartPlaylist](smartplaylist-element.md) |



 

## <a name="remarks"></a>Commenti

Quando un **elemento seq** contiene solo **elementi multimediali** che fanno riferimento a elementi multimediali specifici, la playlist viene considerata statica. Quando un **elemento seq** contiene un **elemento smartPlaylist,** viene considerato una playlist dinamica "intelligente".

## <a name="examples"></a>Esempio


```
<seq>
    <media></media>
    <media></media>
</seq>

<seq>
    <smartPlaylist></smartPlaylist>
</seq>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento body**](body-element.md)
</dt> <dt>

[**Elemento media**](media-element.md)
</dt> <dt>

[**Elemento smartPlaylist**](smartplaylist-element.md)
</dt> <dt>

[**Windows Informazioni di riferimento per gli elementi della playlist multimediale**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





