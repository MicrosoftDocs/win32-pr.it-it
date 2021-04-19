---
title: Elemento seq
description: L'elemento seq contiene elementi che definiscono una playlist statica o elementi che definiscono una playlist intelligente.
ms.assetid: 849f7b38-25f2-4708-a83c-e651812a1a72
keywords:
- Elemento seq Media Player Windows
topic_type:
- apiref
api_name:
- seq Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b08b3f4dfa448e48f3a9d2472c6ddb46a4d4dfaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325828"
---
# <a name="seq-element"></a>Elemento seq

L'elemento **Seq** contiene elementi che definiscono una playlist statica o elementi che definiscono una playlist intelligente.

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
| Figlio     | [supporti](media-element.md), [smartPlaylist](smartplaylist-element.md) |



 

## <a name="remarks"></a>Commenti

Quando un elemento **Seq** contiene solo elementi **multimediali** che fanno riferimento a elementi multimediali specifici, la playlist viene considerata statica. Quando un elemento **Seq** contiene un elemento **smartPlaylist** , viene considerato una playlist dinamica "intelligente".

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
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Body (elemento)**](body-element.md)
</dt> <dt>

[**Elemento multimediale**](media-element.md)
</dt> <dt>

[**Elemento smartPlaylist**](smartplaylist-element.md)
</dt> <dt>

[**Riferimento agli elementi della playlist Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





