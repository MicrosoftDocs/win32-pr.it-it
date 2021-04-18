---
title: BUTTONGROUP. hueShift
description: L'attributo hueShift specifica o recupera la quantità in base alla quale viene spostata la tonalità delle immagini BUTTONGROUP.
ms.assetid: 156256ef-ec24-40c4-ad23-064e38c79e69
keywords:
- Media Player Windows BUTTONGROUP. hueShift
topic_type:
- apiref
api_name:
- BUTTONGROUP.hueShift
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bf77faea27ecc5adee6525c4ee8d8ff1541aac4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324101"
---
# <a name="buttongrouphueshift"></a>BUTTONGROUP. hueShift

L'attributo **hueShift** specifica o recupera la quantità in base alla quale viene spostata la tonalità delle immagini **ButtonGroup** .

``` syntax
        elementID.hueShift
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **numero** di lettura/scrittura (**float**) con un valore compreso tra 0,0 e 360,0 e il cui valore predefinito è 0,0.

## <a name="remarks"></a>Commenti

Questo attributo modifica il valore di tonalità delle immagini specificate dagli attributi **disabledImage**, **downImage**, **hoverDownImage**, **hoverImage** e **Image** se sono stati specificati e fanno riferimento a immagini BMP a 8 bit.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP. disabledImage**](buttongroup-disabledimage.md)
</dt> <dt>

[**BUTTONGROUP. downImage**](buttongroup-downimage.md)
</dt> <dt>

[**BUTTONGROUP. hoverDownImage**](buttongroup-hoverdownimage.md)
</dt> <dt>

[**BUTTONGROUP. hoverImage**](buttongroup-hoverimage.md)
</dt> <dt>

[**BUTTONGROUP. image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP. saturazione**](buttongroup-saturation.md)
</dt> </dl>

 

 





