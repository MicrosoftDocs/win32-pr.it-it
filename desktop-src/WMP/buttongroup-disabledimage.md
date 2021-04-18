---
title: BUTTONGROUP. disabledImage
description: L'attributo disabledImage specifica o Recupera il nome dell'immagine che rappresenta lo stato disabilitato dei pulsanti in BUTTONGROUP.
ms.assetid: 34d4e6a9-de73-4dfa-9c23-4f17b55298f6
keywords:
- Media Player Windows BUTTONGROUP. disabledImage
topic_type:
- apiref
api_name:
- BUTTONGROUP.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9659c4d726313c0fb202a840e12891f00ad3fcf0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324997"
---
# <a name="buttongroupdisabledimage"></a>BUTTONGROUP. disabledImage

L'attributo **disabledImage** specifica o Recupera il nome dell'immagine che rappresenta lo stato disabilitato dei pulsanti in **ButtonGroup**.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura.

## <a name="remarks"></a>Commenti

I formati di immagine supportati sono BMP, JPG, PNG e GIF. Se l'immagine è un file BMP a 8 bit, i relativi valori di tonalità e saturazione possono essere modificati dinamicamente usando gli attributi **hueShift** e **Saturation** .

Quando l'attributo **disabled** di un elemento **ButtonElement** è impostato su true, viene visualizzata l'area corrispondente di **disabledImage** per **ButtonGroup** . Se l'immagine disabilitata è più grande dell'area definita, l'immagine disabilitata verrà ritagliata.

Se non è possibile recuperare l'immagine, viene visualizzata un'immagine predefinita, ovvero l'immagine rossa (x).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP. hueShift**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTONGROUP. saturazione**](buttongroup-saturation.md)
</dt> </dl>

 

 





