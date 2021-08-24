---
title: Elemento sourceFilter
description: L'elemento sourceFilter contiene elementi che selezionano elementi da una libreria.
ms.assetid: c961990f-8c57-448d-b4dc-dcfe70300e5a
keywords:
- Elemento sourceFilter Windows Media Player
topic_type:
- apiref
api_name:
- sourceFilter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14294f227e5ebe29e422d60a95734f7b93207880ea82ef9fb70ed3f7cf6dac4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763271"
---
# <a name="sourcefilter-element"></a>Elemento sourceFilter

**L'elemento sourceFilter** contiene elementi che selezionano elementi da una libreria.

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

<span id="type"></span><span id="TYPE"></span>**digitare**
</dt> <dd>

Tipo di oggetto filtro. Non sono presenti valori predefiniti per questo attributo.

</dd> <dt>

<span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**ID** (obbligatorio) 
</dt> <dd>

GUID che identifica in modo univoco l'oggetto filtro di origine. I metodi dell'oggetto filtro di origine vengono richiamati per interpretare gli elementi **del** frammento contenuti nell'elemento **sourceFilter.**



| Valore                                  | Descrizione                                              |
|----------------------------------------|----------------------------------------------------------|
| {4202947A-A563-4B05-A754-A1B4B5989849} | GUID per il filtro di origine "Musica nella libreria".    |
| {B2D9BDDC-8E49-444B-9BA4-193ABF9C7870} | GUID per il filtro di origine "Video nella libreria".    |
| {CC823400-A8E4-4081-B073-D3B6D952FE69} | GUID per il filtro di origine "Immagini nella libreria". |
| {E5415A66-7763-4BDE-B97F-5557CA73C303} | GUID per il filtro di origine "PROGRAMMI TV nella libreria". |



 

</dd> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**name** (obbligatorio) 
</dt> <dd>

Nome dell'oggetto filtro.



| Valore                  | Descrizione                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------|
| Musica nella libreria    | Oggetto filtro che seleziona gli elementi specificati dal set di elementi musicali nella libreria dell'utente. |
| Video nella libreria    | Oggetto filtro che seleziona gli elementi specificati dal set di elementi video nella libreria dell'utente. |
| Immagini nella libreria | Oggetto filtro che seleziona gli elementi specificati dal set di elementi foto nella libreria dell'utente. |
| Programmi TV nella libreria | Oggetto filtro che seleziona gli elementi specificati dal set di elementi TV nella libreria dell'utente.    |



 

</dd> </dl>

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia | Elementi                         |
|-----------|----------------------------------|
| Padre    | [querySet](queryset-element.md) |
| Figlio     | [Frammento](fragment-element.md) |



 

## <a name="remarks"></a>Commenti

**L'elemento sourceFilter** seleziona gli elementi dalla libreria indipendentemente dalle dimensioni del set di risultati. **L'elemento** filtro, d'altra parte, limita le dimensioni del set di risultati.

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
| Versione<br/> | Windows Media Player serie 9 o successive.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento filter**](filter-element.md)
</dt> <dt>

[**Elemento fragment**](fragment-element.md)
</dt> <dt>

[**Elemento querySet**](queryset-element.md)
</dt> <dt>

[**Windows Informazioni di riferimento per gli elementi della playlist multimediale**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





