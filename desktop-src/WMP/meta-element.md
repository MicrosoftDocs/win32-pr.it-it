---
title: Elemento meta
description: L'elemento meta specifica i metadati che si applicano all'intera playlist.
ms.assetid: 7248e1d9-ebd1-48cb-9019-89a35eac27ae
keywords:
- Elemento meta Windows Media Player
topic_type:
- apiref
api_name:
- meta Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b2e4120b3eceea6d2a664edec9b48a46d33ad19b788bb820458a8802dccd2d9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119415741"
---
# <a name="meta-element"></a>Elemento meta

**L'elemento meta** specifica i metadati che si applicano all'intera playlist.

``` syntax
<meta
    name = "string"
    content = "string"
/>
```

## <a name="attributes"></a>Attributi



| Termine                                                                       | Descrizione                                                                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="name"></span><span id="NAME"></span>**Nome**<br/>          | Nome di un elemento di metadati.<br/>                                                                                       |
| <span id="content"></span><span id="CONTENT"></span>**Contenuto**<br/> | Valore di un elemento di metadati. Ad esempio, se l'attributo name è "Genre", l'attributo content potrebbe essere "Rock".<br/> |



 

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia | Elementi                 |
|-----------|--------------------------|
| Padre    | [Testa](head-element.md) |
| Figlio     | nessuno                     |



 

## <a name="remarks"></a>Osservazioni

L'autore di una Windows Playlist multimediale può impostare l'attributo name di un meta-elemento su qualsiasi stringa. L'elenco seguente mostra alcuni attributi di nome tipici disponibili in Windows Playlist multimediali create da Windows Media Player e altri componenti Microsoft.

-   Autore
-   Category
-   Genre
-   Nome utente
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
| Versione<br/> | Windows Media Player serie 9 o successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento head**](head-element.md)
</dt> <dt>

[**Windows Informazioni di riferimento per gli elementi della playlist multimediale**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





