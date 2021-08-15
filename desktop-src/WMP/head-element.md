---
title: Elemento head
description: L'elemento head contiene i metadati che si applicano all'intera playlist.
ms.assetid: 9554c84a-34af-4492-964a-4b262cd7c4a4
keywords:
- Elemento head Windows Media Player
topic_type:
- apiref
api_name:
- head Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a865419a005927cd85ea6b03d4fabad2e2ac3ef15a840b3bd01209a4df00c075
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339171"
---
# <a name="head-element"></a>Elemento head

**L'elemento** head contiene i metadati che si applicano all'intera playlist.

``` syntax
<head>
</head>
```

## <a name="attributes"></a>Attributi

Questo elemento non ha attributi.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia | Elementi                                                  |
|-----------|-----------------------------------------------------------|
| Padre    | [Smil](smil-element.md)                                  |
| Figlio     | [title](title-element--wpl.md), [meta](meta-element.md) |



 

## <a name="remarks"></a>Commenti

In genere **l'elemento** head contiene **un elemento titolo** e uno o più **meta** elementi che definiscono le caratteristiche globali della playlist.

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
| Versione<br/> | Windows Media Player serie 9 o successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento meta**](meta-element.md)
</dt> <dt>

[**Elemento title (WPL)**](title-element--wpl.md)
</dt> <dt>

[**Windows Informazioni di riferimento per gli elementi della playlist multimediale**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





