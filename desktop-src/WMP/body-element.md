---
title: Elemento body
description: L'elemento body contiene gli elementi che definiscono il contenuto di una playlist.
ms.assetid: 96d09635-c360-4a36-a56e-6cecbbd4ff30
keywords:
- Elemento body Windows Media Player
topic_type:
- apiref
api_name:
- body Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c785b7db7b44177469596450ee75a460e2bc6224b191a2811baf95380bea25a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135954"
---
# <a name="body-element"></a>Elemento body

**L'elemento** body contiene gli elementi che definiscono il contenuto di una playlist.

``` syntax
<body>
</body>
```

## <a name="attributes"></a>Attributi

Questo elemento non ha attributi.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia | Elementi                 |
|-----------|--------------------------|
| Padre    | [Smil](smil-element.md) |
| Figlio     | [Seq](seq-element.md)   |



 

## <a name="remarks"></a>Commenti

Il contenuto di una playlist è organizzato all'interno di **un elemento seq** contenuto all'interno dell'elemento **body.** In genere è presente un elemento **seq** che definisce  un set statico di elementi multimediali e contiene elementi multimediali oppure un elemento che definisce un set dinamico di elementi multimediali e contiene un **elemento smartPlaylist.**

## <a name="examples"></a>Esempio


```XML
<body>
    <seq>
        <media></media>
        <media></media>
        <media></media>
    </seq>
</body>

<body>
    <seq>
        <smartPlaylist></smartPlaylist>
    </seq>
</body>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento media**](media-element.md)
</dt> <dt>

[**Elemento seq**](seq-element.md)
</dt> <dt>

[**Elemento smartPlaylist**](smartplaylist-element.md)
</dt> <dt>

[**Elemento smil**](smil-element.md)
</dt> <dt>

[**Windows Informazioni di riferimento per gli elementi della playlist multimediale**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





