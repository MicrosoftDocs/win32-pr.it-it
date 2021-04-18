---
title: Elemento meta
description: L'elemento meta specifica i metadati che si applicano all'intera playlist.
ms.assetid: 7248e1d9-ebd1-48cb-9019-89a35eac27ae
keywords:
- meta-elemento Media Player Windows
topic_type:
- apiref
api_name:
- meta Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f3c41c25a0df0895c645c34f97495712b113ffc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327149"
---
# <a name="meta-element"></a>Elemento meta

L'elemento **meta** specifica i metadati che si applicano all'intera playlist.

``` syntax
<meta
    name = "string"
    content = "string"
/>
```

## <a name="attributes"></a>Attributi



| Termine                                                                       | Descrizione                                                                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="name"></span><span id="NAME"></span>**nome**<br/>          | Nome di un elemento di metadati.<br/>                                                                                       |
| <span id="content"></span><span id="CONTENT"></span>**contenuto**<br/> | Valore di un elemento di metadati. Ad esempio, se l'attributo del nome è "genre", l'attributo di contenuto potrebbe essere "Rock".<br/> |



 

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia | Elementi                 |
|-----------|--------------------------|
| Padre    | [Head](head-element.md) |
| Figlio     | nessuno                     |



 

## <a name="remarks"></a>Osservazioni

L'autore di una playlist di Windows Media può impostare l'attributo Name di un metaelemento su qualsiasi stringa. Nell'elenco seguente vengono illustrati alcuni attributi di nome tipici presenti nelle playlist di Windows Media create da Windows Media Player e altri componenti Microsoft.

-   Autore
-   Category
-   Genre
-   UserName
-   UserRating
-   Generator

## <a name="examples"></a>Esempio


```
<head>
    <meta name = "Author" content = "Frank Lee"/>
    <meta name = "Category" content = "Classic"/>
    <meta name = "Genre" content = "Rock"/>
</head>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento Head**](head-element.md)
</dt> <dt>

[**Riferimento agli elementi della playlist Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





