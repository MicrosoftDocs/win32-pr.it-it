---
title: Elemento smil
description: L'elemento smil è sempre l'elemento di livello principale in un file di playlist Windows Media (WPL). Specifica che il file usa la sintassi e la grammatica di SMIL (Synchronized Multimedia Integration Language).
ms.assetid: bb14f1b8-53d0-47ff-9fd3-4620a1467985
keywords:
- Finestre degli elementi SMIL Media Player
topic_type:
- apiref
api_name:
- smil Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78ec8900139cfbd5982228c59010674bbc14765e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331741"
---
# <a name="smil-element"></a>Elemento smil

L'elemento **SMIL** è sempre l'elemento di livello principale in un file di playlist Windows Media (WPL). Specifica che il file usa la sintassi e la grammatica di SMIL (Synchronized Multimedia Integration Language).

``` syntax
<smil>
</smil>
```

## <a name="attributes"></a>Attributi

Questo elemento non ha attributi.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia | Elementi                                           |
|-----------|----------------------------------------------------|
| Padre    | nessuno                                               |
| Figlio     | [Head](head-element.md), [corpo](body-element.md) |



 

## <a name="remarks"></a>Commenti

Ogni playlist di Windows Media deve avere l'elemento **SMIL** alla radice.

## <a name="examples"></a>Esempio


```
<?wpl version = "1.0"?>
<smil>
    <head>
        <entity type="hellip"/>
    </head>

    <body>
        <entity type="hellip"/>
    </body>
</smil>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Body (elemento)**](body-element.md)
</dt> <dt>

[**Elemento Head**](head-element.md)
</dt> <dt>

[**Riferimento agli elementi della playlist Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





