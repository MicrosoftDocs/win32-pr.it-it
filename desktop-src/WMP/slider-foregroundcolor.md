---
title: SLIDER.foregroundColor
description: L'attributo foregroundColor specifica o recupera il colore di primo piano del controllo dispositivo di scorrimento.
ms.assetid: 8c8de4a9-0021-41ed-aeb8-75653855b6f1
keywords:
- SLIDER.foregroundColor Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a111dca131351dedaf2080d16bffa4db1344e9993cabcfe8ca44f149fd97eb3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569090"
---
# <a name="sliderforegroundcolor"></a>SLIDER.foregroundColor

**L'attributo foregroundColor** specifica o recupera il colore di primo piano del controllo dispositivo di scorrimento.

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una  stringa di lettura/scrittura contenente qualsiasi valore di colore Internet Explorer Microsoft. Il valore predefinito è "white".

## <a name="remarks"></a>Commenti

È possibile costruire un controllo dispositivo di scorrimento di base specificando una delle due coppie di attributi: **backgroundColor** e **foregroundColor** o **backgroundImage** e **foregroundImage**.

Quando si costruisce un controllo dispositivo di scorrimento usando gli attributi di colore, le dimensioni del controllo dispositivo di scorrimento definiscono l'area riempita dal colore di sfondo. Il colore di primo piano copre il colore di sfondo all'aumentare della posizione del dispositivo di scorrimento.

Per creare un riempimento sfumato nell'area occupata dal colore di sfondo o primo piano, specificare gli attributi **backgroundEndColor** **o foregroundEndColor.**

Vedere *CUSTOMSLIDER*. [Attributo positionImage](customslider-positionimage.md) per un esempio che illustra come vengono usati gli attributi **dell'elemento SLIDER.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento sul colore**](color-reference.md)
</dt> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER.backgroundColor**](slider-backgroundcolor.md)
</dt> <dt>

[**SLIDER.backgroundEndColor**](slider-backgroundendcolor.md)
</dt> <dt>

[**SLIDER.foregroundEndColor**](slider-foregroundendcolor.md)
</dt> <dt>

[**SLIDER.foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





