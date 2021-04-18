---
title: Elemento sourceFilter
description: L'elemento sourceFilter contiene elementi che selezionano gli elementi di una raccolta.
ms.assetid: c961990f-8c57-448d-b4dc-dcfe70300e5a
keywords:
- Finestra elementi sourceFilter Media Player
topic_type:
- apiref
api_name:
- sourceFilter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb43a9577c5fe8857b63067db5be90d314037b84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331740"
---
# <a name="sourcefilter-element"></a>Elemento sourceFilter

L'elemento **sourceFilter** contiene elementi che selezionano gli elementi di una raccolta.

``` syntax
<sourceFilter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</sourceFilter>
```

## <a name="attributes"></a>Attributi

<dl> <dt>

<span id="type"></span><span id="TYPE"></span>**tipo**
</dt> <dd>

Tipo di oggetto filtro. Nessun valore predefinito per questo attributo.

</dd> <dt>

<span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**ID** (obbligatorio) 
</dt> <dd>

GUID che identifica in modo univoco l'oggetto filtro di origine. I metodi dell'oggetto filtro di origine vengono richiamati per interpretare gli elementi del **frammento** contenuti nell'elemento **sourceFilter** .



| Valore                                  | Descrizione                                              |
|----------------------------------------|----------------------------------------------------------|
| {4202947A-A563-4B05-A754-A1B4B5989849} | GUID per il filtro di origine "musica nel catalogo personale".    |
| {B2D9BDDC-8E49-444B-9BA4-193ABF9C7870} | GUID per il filtro di origine "video in My Library".    |
| {CC823400-A8E4-4081-B073-D3B6D952FE69} | GUID per il filtro di origine "Pictures in My Library". |
| {E5415A66-7763-4BDE-B97F-5557CA73C303} | Il GUID per il filtro di origine "TV shows in My Library". |



 

</dd> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**nome** (obbligatorio) 
</dt> <dd>

Nome dell'oggetto filtro.



| Valore                  | Descrizione                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------|
| Musica nella libreria    | Oggetto filtro che seleziona gli elementi specificati dal set di elementi musicali nella libreria dell'utente. |
| Video nella libreria    | Oggetto filtro che seleziona gli elementi specificati dal set di elementi video nella libreria dell'utente. |
| Immagini nella libreria | Oggetto filtro che seleziona gli elementi specificati dal set di elementi della foto nella libreria dell'utente. |
| Programmi TV nella libreria | Oggetto filtro che seleziona gli elementi specificati dal set di elementi TV nella libreria dell'utente.    |



 

</dd> </dl>

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia | Elementi                         |
|-----------|----------------------------------|
| Padre    | [querySet](queryset-element.md) |
| Figlio     | [frammento](fragment-element.md) |



 

## <a name="remarks"></a>Commenti

L'elemento **sourceFilter** seleziona gli elementi dalla libreria senza considerare le dimensioni del set di risultati. L'elemento **Filter** , invece, limita le dimensioni del set di risultati.

## <a name="examples"></a>Esempio


```
<sourceFilter 
    type = "smartFilterObject" 
    id = "{4202947A-A563-4B05-A754-A1B4B5989849}" 
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
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Filter-elemento**](filter-element.md)
</dt> <dt>

[**Elemento Fragment**](fragment-element.md)
</dt> <dt>

[**Elemento querySet**](queryset-element.md)
</dt> <dt>

[**Riferimento agli elementi della playlist Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





