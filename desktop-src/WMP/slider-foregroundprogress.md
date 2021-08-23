---
title: SLIDER.foregroundProgress
description: L'attributo foregroundProgress specifica o recupera la posizione corrente dell'indicatore di stato in primo piano come percentuale dell'area del dispositivo di scorrimento.
ms.assetid: 1218ca5a-445c-441b-aa62-74a184a25c2d
keywords:
- Slider.foregroundProgress Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e48819a2b3245fc8a72d29e9a30135cc37702417ca498c88b8be01578b74988
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646341"
---
# <a name="sliderforegroundprogress"></a>SLIDER.foregroundProgress

**L'attributo foregroundProgress** specifica o recupera la posizione corrente dell'indicatore di stato in primo piano come percentuale dell'area del dispositivo di scorrimento.

``` syntax
        elementID.foregroundProgress
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un numero di **lettura/scrittura** (**float**) compreso tra 0 e 100.

## <a name="remarks"></a>Commenti

Questo attributo viene usato principalmente per tenere traccia dello stato di avanzamento del download di un file multimediale e allo stesso tempo per tenere traccia della posizione di riproduzione corrente del file usando **l'attributo** value. La posizione del cursore del dispositivo di scorrimento è vincolata all'area dello stato di avanzamento in primo piano. Ciò consente la ricerca interattiva solo all'interno della parte disponibile di un file in download.

Per usare questa funzionalità, **l'attributo useForegroundProgress** deve essere impostato su true.

## <a name="examples"></a>Esempio


```C++
<SLIDER
  id="seek"
  backgroundColor="blue"
  foregroundColor="red"
  thumbImage="seekthumb.bmp"
  min="0"
  max="wmpprop:player.currentMedia.duration"
  value="wmpprop:player.controls.currentPosition"
  useForegroundProgress="true"
  foregroundProgress="wmpprop:player.network.downloadProgress"
  ondragend="player.controls.currentposition=value"
/>

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER.min**](slider-min.md)
</dt> <dt>

[**SLIDER.max**](slider-max.md)
</dt> <dt>

[**SLIDER.useForegroundProgress**](slider-useforegroundprogress.md)
</dt> <dt>

[**SLIDER.value**](slider-value.md)
</dt> </dl>

 

 





