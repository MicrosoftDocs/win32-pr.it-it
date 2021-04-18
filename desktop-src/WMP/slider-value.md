---
title: SLIDER. Value
description: L'attributo value specifica o recupera la posizione corrente del dispositivo di scorrimento. | SLIDER. Value
ms.assetid: 2cd2f8b2-d3f1-4897-98b0-af551d6693e6
keywords:
- Media Player SLIDER. Value Windows
topic_type:
- apiref
api_name:
- SLIDER.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87aeff5c97808efb812f530236227b07f463855
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327703"
---
# <a name="slidervalue"></a>SLIDER. Value

L'attributo **value** specifica o recupera la posizione corrente del dispositivo di scorrimento.

``` syntax
        elementID.value
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **numero** di lettura/scrittura (**float**) con un valore predefinito di **min**.

## <a name="remarks"></a>Commenti

Il **valore** deve essere sempre maggiore o uguale a **min** e minore o uguale a **Max**. Se si specifica un valore non compreso in questo intervallo, il **valore** e la posizione del dispositivo di scorrimento non vengono modificati.

Vedere **CUSTOMSLIDER**. attributo [dimensione positionImage](customslider-positionimage.md) per un esempio che illustra come vengono utilizzati gli attributi dell'elemento **Slider** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER. min**](slider-min.md)
</dt> </dl>

 

 





