---
title: SLIDER.value
description: L'attributo value specifica o recupera la posizione corrente del dispositivo di scorrimento. | SLIDER.value
ms.assetid: 2cd2f8b2-d3f1-4897-98b0-af551d6693e6
keywords:
- Slider.value Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30f9ae7c0dc45f3a14cad2aa5b7332b037302b6658043233bbd98b1d99a12e10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118629"
---
# <a name="slidervalue"></a>SLIDER.value

**L'attributo** value specifica o recupera la posizione corrente del dispositivo di scorrimento.

``` syntax
        elementID.value
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un numero di **lettura/scrittura** (**float**) con valore predefinito **min**.

## <a name="remarks"></a>Commenti

Il **valore** deve essere sempre maggiore o uguale a **min** e minore o uguale a **max.** Se si specifica un valore non compreso in questo intervallo, **il valore** e la posizione del dispositivo di scorrimento non vengono modificati.

Vedere **l'oggetto ELIDER**. [Attributo positionImage](customslider-positionimage.md) per un esempio che illustra come vengono usati gli attributi dell'elemento **SLIDER.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER.min**](slider-min.md)
</dt> </dl>

 

 





