---
title: Elemento Head
description: L'elemento Head contiene i metadati che si applicano all'intera playlist.
ms.assetid: 9554c84a-34af-4492-964a-4b262cd7c4a4
keywords:
- Media Player di Windows elemento Head
topic_type:
- apiref
api_name:
- head Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8708a8a683f7457e6568df3a897c71253ad76c02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328883"
---
# <a name="head-element"></a>Elemento Head

L'elemento **Head** contiene i metadati che si applicano all'intera playlist.

``` syntax
<head>
</head>
```

## <a name="attributes"></a>Attributi

Questo elemento non ha attributi.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia | Elementi                                                  |
|-----------|-----------------------------------------------------------|
| Padre    | [SMIL](smil-element.md)                                  |
| Figlio     | [titolo](title-element--wpl.md), [meta](meta-element.md) |



 

## <a name="remarks"></a>Commenti

In genere l'elemento **Head** contiene un elemento **title** e uno o più elementi **meta** che definiscono le caratteristiche globali della playlist.

## <a name="examples"></a>Esempio


```
<head>
    <title>Party Playlist</title>
    <meta name = "Author" CONTENT = "Frank Lee"/>
    <meta name = "Category" CONTENT = "Party Music"/>
    <meta name = "Genre" CONTENT = "Pop"/>
    <meta name = "UserName1" CONTENT = "Frank001"/>
    <meta name = "UserRating1" CONTENT = "82"/>
</head>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento meta**](meta-element.md)
</dt> <dt>

[**Elemento title (WPL)**](title-element--wpl.md)
</dt> <dt>

[**Riferimento agli elementi della playlist Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





