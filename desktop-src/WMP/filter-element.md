---
title: Filter-elemento
description: L'elemento Filter contiene elementi che limitano le dimensioni di una playlist, la durata di una playlist o il numero di elementi multimediali in una playlist.
ms.assetid: 880885f6-493f-466b-b5ad-ab9b569f4cc5
keywords:
- filtrare gli elementi di Windows Media Player
topic_type:
- apiref
api_name:
- filter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 32d2d306faebef813996b59575220efeba99dfb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326726"
---
# <a name="filter-element"></a>Filter-elemento

L'elemento **Filter** contiene elementi che limitano le dimensioni di una playlist, la durata di una playlist o il numero di elementi multimediali in una playlist.

``` syntax
<filter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</filter>
            
```

## <a name="attributes"></a>Attributi

<dl> <dt>

<span id="type"></span><span id="TYPE"></span>**tipo**
</dt> <dd>

Tipo di oggetto filtro. Nessun valore predefinito per questo attributo.

</dd> <dt>

<span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**ID** (obbligatorio) 
</dt> <dd>

GUID che identifica in modo univoco un oggetto filtro. I metodi dell'oggetto filtro vengono richiamati per interpretare gli elementi del **frammento** contenuti nell'elemento **filtro** .



| Valore                                  | Descrizione                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------|
| {BC5E21B0-504C-46F6-82BF-FB975C911AD6} | ID per il filtro "Microsoft auto playlist Filter-limita le playlist automatiche per conteggio, dimensioni o durata". |



 

</dd> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**nome** (obbligatorio) 
</dt> <dd>

Nome dell'oggetto filtro.



| Valore                                                                              | Descrizione                                        |
|------------------------------------------------------------------------------------|----------------------------------------------------|
| Filtro playlist automatico Microsoft: limita le playlist automatiche in base al conteggio, alle dimensioni o alla durata | Limita le playlist automatiche in base al conteggio, alle dimensioni o alla durata. |



 

</dd> </dl>

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia | Elementi                                   |
|-----------|--------------------------------------------|
| Padre    | [smartPlaylist](smartplaylist-element.md) |
| Figlio     | [frammento](fragment-element.md)           |



 

## <a name="remarks"></a>Commenti

L'elemento **Filter** non aggiunge elementi multimediali a una playlist; rimuove o filtra semplicemente il contenuto selezionato dall'elemento **sourceFilter** .

## <a name="examples"></a>Esempio


```XML
<filter 
    type = "smartFilterObject" 
    id = "{BC5E21B0-504C-46F6-82BF-FB975C911AD6}" 
    name = "Microsoft Auto Playlist Filter -- Limits auto playlists by count,size or duration">
        <fragment name = "Limit Number of Items">
            <argument name = "number">25</argument>
        </fragment>
</filter>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento argument**](argument-element.md)
</dt> <dt>

[**Elemento Fragment**](fragment-element.md)
</dt> <dt>

[**Elemento smartPlaylist**](smartplaylist-element.md)
</dt> <dt>

[**Elemento sourceFilter**](sourcefilter-element.md)
</dt> <dt>

[**Riferimento agli elementi della playlist Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





