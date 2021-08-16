---
title: Elemento smartPlaylist
description: L'elemento smartPlaylist contiene la parte definita dinamicamente di una playlist.
ms.assetid: 05912849-7475-4eb9-a7bd-00f20b80b1cf
keywords:
- Elemento smartPlaylist Windows Media Player
topic_type:
- apiref
api_name:
- smartPlaylist Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a21d685759e9e8b27c881ceaec6595535b3c4b799eb28ecd94dd96a3a571ec99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763471"
---
# <a name="smartplaylist-element"></a>Elemento smartPlaylist

**L'elemento smartPlaylist** contiene la parte definita dinamicamente di una playlist.

``` syntax
<smartPlaylist
    version = "number"
>
</smartPlaylist>
```

## <a name="attributes"></a>Attributi



| Termine                                                                                                                                   | Descrizione                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="version__required______________"></span><span id="VERSION__REQUIRED______________"></span>**version** (obbligatorio) <br/> | Numero decimale che rappresenta il numero di versione dello schema smart playlist. Impostare su 1.0.0.0.<br/> |



 

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia | Elementi                                                       |
|-----------|----------------------------------------------------------------|
| Padre    | [Seq](seq-element.md)                                         |
| Figlio     | [querySet](queryset-element.md), [filtro](filter-element.md) |



 

## <a name="remarks"></a>Commenti

Un **elemento smartPlaylist** contiene in genere un **elemento querySet** e può anche contenere un **elemento filter.**

## <a name="examples"></a>Esempio


```
<smartPlaylist version = "1.0.0.0">
    <querySet>
        <sourceFilter 
            type = "smartFilterObject"
            id = "12345678-1234-3333-abCD-123ABCdefGHI"
            name = "Music in my library">
                <fragment name = "Genre">
                    <argument name = "condition">Is</argument>
                    <argument name = "value">Rock</argument>
                </fragment>
                <fragment name = "Album Artist">
                    <argument name = "condition">Is Not</argument>
                    <argument name = "value">Brenda Diaz</argument>
                </fragment>
        </sourceFilter>
    </querySet>
    <filter>
    </filter>
</smartPlaylist>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento argument**](argument-element.md)
</dt> <dt>

[**Elemento filter**](filter-element.md)
</dt> <dt>

[**Elemento fragment**](fragment-element.md)
</dt> <dt>

[**Elemento querySet**](queryset-element.md)
</dt> <dt>

[**Elemento seq**](seq-element.md)
</dt> <dt>

[**Windows Informazioni di riferimento per gli elementi della playlist multimediale**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





