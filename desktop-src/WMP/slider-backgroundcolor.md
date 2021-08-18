---
title: SLIDER.backgroundColor
description: L'attributo backgroundColor specifica o recupera il colore di sfondo del controllo dispositivo di scorrimento.
ms.assetid: 8f2c48ec-29f5-4fbe-aa62-c7cfb8a8678c
keywords:
- SLIDER.backgroundColor Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fc2de30392c58cfad151e2d3c209f0407880a47522a536bf08dbe42d7f56dc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995231"
---
# <a name="sliderbackgroundcolor"></a>SLIDER.backgroundColor

**L'attributo backgroundColor** specifica o recupera il colore di sfondo del controllo dispositivo di scorrimento.

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una  stringa di lettura/scrittura contenente qualsiasi valore di colore Internet Explorer Microsoft. e non prevede alcun valore predefinito.

## <a name="remarks"></a>Commenti

È possibile costruire un controllo dispositivo di scorrimento di base specificando **backgroundColor** o **backgroundImage** e **foregroundColor** **o foregroundImage**.

Quando si usano i colori, le dimensioni del controllo dispositivo di scorrimento definiscono l'area riempita dal colore di sfondo. Il colore di primo piano copre il colore di sfondo all'aumentare della posizione del dispositivo di scorrimento.

Per creare un riempimento sfumato dell'area occupata dal colore di sfondo o primo piano, specificare gli **attributi backgroundEndColor** **o foregroundEndColor.**

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

[**SLIDER.backgroundEndColor**](slider-backgroundendcolor.md)
</dt> <dt>

[**SLIDER.backgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**SLIDER.foregroundColor**](slider-foregroundcolor.md)
</dt> <dt>

[**SLIDER.foregroundEndColor**](slider-foregroundendcolor.md)
</dt> <dt>

[**SLIDER.foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





