---
title: Elemento querySet
description: L'elemento querySet contiene elementi che definiscono quali elementi multimediali verranno selezionati dalla libreria.
ms.assetid: 18b5a509-a56b-4fd1-812f-60b8efd5136b
keywords:
- Finestra elementi querySet Media Player
topic_type:
- apiref
api_name:
- querySet Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4971c2a7f601132640d7654a95dd288f1740a467
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331217"
---
# <a name="queryset-element"></a>Elemento querySet

L'elemento **querySet** contiene elementi che definiscono quali elementi multimediali verranno selezionati dalla libreria.

``` syntax
<querySet>
</querySet>
```

## <a name="attributes"></a>Attributi

Questo elemento non ha attributi.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia | Elementi                                   |
|-----------|--------------------------------------------|
| Padre    | [smartPlaylist](smartplaylist-element.md) |
| Figlio     | [sourceFilter](sourcefilter-element.md)   |



 

## <a name="remarks"></a>Commenti

L'elemento **querySet** specifica quali elementi multimediali devono essere selezionati dalla libreria, senza considerare le dimensioni del set di risultati. L'elemento **Filter** , invece, limita le dimensioni del set di risultati.

## <a name="examples"></a>Esempio


```
<querySet>
    <sourceFilter 
        type = "smartFilterObject" 
        id = "{4202947A-A563-4B05-A754-A1B4B5989849}"
        name = "Windows Media Local Music Library Filter">
            <fragment name = "Genre">
                <argument name = "Condition">Equals</argument>
                <argument name = "Value">Rock</argument>
            </fragment>
            <fragment name = "Artist">
                <argument name = "Condition">Does Not Equal</argument>
                <argument name = "Value">Brenda Diaz</argument>
            </fragment>
    </sourceFilter>
</querySet>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento argument**](argument-element.md)
</dt> <dt>

[**Filter-elemento**](filter-element.md)
</dt> <dt>

[**Elemento Fragment**](fragment-element.md)
</dt> <dt>

[**Elemento smartPlaylist**](smartplaylist-element.md)
</dt> <dt>

[**Elemento sourceFilter**](sourcefilter-element.md)
</dt> <dt>

[**Riferimento agli elementi della playlist Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





