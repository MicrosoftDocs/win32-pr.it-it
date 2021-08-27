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
ms.openlocfilehash: 1de2679d5f78b48ceef569491ef21998fc13faf7126e61f76ad31959bdc2ac6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122781"
---
# <a name="title-element-wpl"></a>Elemento title (WPL)

**L'elemento** title specifica un titolo per la playlist.

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
| Padre    | [Testa](head-element.md) |
| Figlio     | nessuno                     |



 

## <a name="remarks"></a>Osservazioni

Quando si sceglie un titolo per una playlist Windows Media Playlist (WPL), tenere presente che il contenuto della playlist può essere dinamico. Un approccio valido consiste nel basare  il titolo sulla logica negli elementi dell'argomento perché questo è ciò che definisce il contenuto della playlist. Ne sono esempi "My Favorite Rock Songs from 1966" o "Dance Songs That I Haven't Played Recently".

## <a name="examples"></a>Esempio


```
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento argument**](argument-element.md)
</dt> <dt>

[**Elemento head**](head-element.md)
</dt> <dt>

[**Windows Informazioni di riferimento per gli elementi della playlist multimediale**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





