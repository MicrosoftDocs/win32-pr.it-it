---
title: Elemento filter
description: L'elemento filtro contiene elementi che limitano le dimensioni di una playlist, la durata di una playlist o il numero di elementi multimediali in una playlist.
ms.assetid: 880885f6-493f-466b-b5ad-ab9b569f4cc5
keywords:
- Elemento filter Windows Media Player
topic_type:
- apiref
api_name:
- filter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a059a6a2820d99541076775ac869de0767ffd739743f5b145a155efd0a25abc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118576778"
---
# <a name="filter-element"></a>Elemento filter

**L'elemento filtro** contiene elementi che limitano le dimensioni di una playlist, la durata di una playlist o il numero di elementi multimediali in una playlist.

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

<span id="type"></span><span id="TYPE"></span>**digitare**
</dt> <dd>

Tipo di oggetto filtro. Non sono presenti valori predefiniti per questo attributo.

</dd> <dt>

<span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**ID** (obbligatorio) 
</dt> <dd>

GUID che identifica in modo univoco un oggetto filtro. I metodi dell'oggetto filtro vengono richiamati per interpretare gli elementi **del** frammento contenuti nell'elemento **filtro.**



| Valore                                  | Descrizione                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------|
| {BC5E21B0-504C-46F6-82BF-FB975C911AD6} | ID per il filtro "Filtro playlist automatica Microsoft - Limita le playlist auto in base al conteggio, alle dimensioni o alla durata". |



 

</dd> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**name** (obbligatorio) 
</dt> <dd>

Nome dell'oggetto filtro.



| Valore                                                                              | Descrizione                                        |
|------------------------------------------------------------------------------------|----------------------------------------------------|
| Filtro playlist automatica Microsoft : limita le playlist auto per numero, dimensioni o durata | Limita le playlist automatica in base al conteggio, alle dimensioni o alla durata. |



 

</dd> </dl>

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia | Elementi                                   |
|-----------|--------------------------------------------|
| Padre    | [smartPlaylist](smartplaylist-element.md) |
| Figlio     | [Frammento](fragment-element.md)           |



 

## <a name="remarks"></a>Commenti

**L'elemento filter** non aggiunge elementi multimediali a una playlist. rimuove o filtra semplicemente il contenuto selezionato dall'elemento **sourceFilter.**

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
| Versione<br/> | Windows Media Player serie 9 o successive.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento argument**](argument-element.md)
</dt> <dt>

[**Elemento fragment**](fragment-element.md)
</dt> <dt>

[**Elemento smartPlaylist**](smartplaylist-element.md)
</dt> <dt>

[**Elemento sourceFilter**](sourcefilter-element.md)
</dt> <dt>

[**Windows Informazioni di riferimento per gli elementi della playlist multimediale**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





