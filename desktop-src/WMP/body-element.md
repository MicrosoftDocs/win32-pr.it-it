---
title: Body (elemento)
description: L'elemento Body contiene gli elementi che definiscono il contenuto di una playlist.
ms.assetid: 96d09635-c360-4a36-a56e-6cecbbd4ff30
keywords:
- Finestra elementi corpo Media Player
topic_type:
- apiref
api_name:
- body Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb30885efe9e018bf8792b38facdc086c5473b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331015"
---
# <a name="body-element"></a>Body (elemento)

L'elemento **Body** contiene gli elementi che definiscono il contenuto di una playlist.

``` syntax
<body>
</body>
```

## <a name="attributes"></a>Attributi

Questo elemento non ha attributi.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia | Elementi                 |
|-----------|--------------------------|
| Padre    | [SMIL](smil-element.md) |
| Figlio     | [Seq](seq-element.md)   |



 

## <a name="remarks"></a>Commenti

Il contenuto di una playlist è organizzato all'interno di un elemento **Seq** contenuto all'interno dell'elemento **Body** . In genere è presente un elemento **Seq** che definisce un set statico di elementi multimediali e contiene elementi **multimediali** oppure ne esiste uno che definisce un set dinamico di elementi multimediali e contiene un elemento **smartPlaylist** .

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
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento multimediale**](media-element.md)
</dt> <dt>

[**Elemento seq**](seq-element.md)
</dt> <dt>

[**Elemento smartPlaylist**](smartplaylist-element.md)
</dt> <dt>

[**Elemento smil**](smil-element.md)
</dt> <dt>

[**Riferimento agli elementi della playlist Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





