---
title: Elemento title (WPL)
description: L'elemento title specifica un titolo per la playlist.
ms.assetid: 8a214b96-d507-4dbf-b5f2-8fdfc4409fb0
keywords:
- Elemento title (WPL) Windows Media Player
topic_type:
- apiref
api_name:
- title Element (WPL)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5649553ab51a43bd1fb0aeb78d505d7e922bf80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328869"
---
# <a name="title-element-wpl"></a>Elemento title (WPL)

L'elemento **title** specifica un titolo per la playlist.

``` syntax
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```

## <a name="attributes"></a>Attributi

Questo elemento non ha attributi.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia | Elementi                 |
|-----------|--------------------------|
| Padre    | [Head](head-element.md) |
| Figlio     | nessuno                     |



 

## <a name="remarks"></a>Osservazioni

Quando si sceglie un titolo per una playlist Windows Media (WPL), tenere presente che il contenuto della playlist può essere dinamico. Un approccio efficace consiste nel basare il titolo sulla logica negli elementi **argument** perché definisce il contenuto della playlist. Esempi di questo argomento sono "canzoni rock preferite da 1966" o "canzoni dance che non ho eseguito di recente".

## <a name="examples"></a>Esempio


```
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento argument**](argument-element.md)
</dt> <dt>

[**Elemento Head**](head-element.md)
</dt> <dt>

[**Riferimento agli elementi della playlist Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





