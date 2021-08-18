---
title: BUTTONGROUP.disabledImage
description: L'attributo disabledImage specifica o recupera il nome dell'immagine che rappresenta lo stato disabilitato dei pulsanti in BUTTONGROUP.
ms.assetid: 34d4e6a9-de73-4dfa-9c23-4f17b55298f6
keywords:
- BUTTONGROUP.disabledImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eeef37bbc25185a64e767f00f9ce17934e8b445327606b552ad69d282e42e4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764351"
---
# <a name="buttongroupdisabledimage"></a>BUTTONGROUP.disabledImage

**L'attributo disabledImage** specifica o recupera il nome dell'immagine che rappresenta lo stato disabilitato dei pulsanti in **BUTTONGROUP.**

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura.**

## <a name="remarks"></a>Commenti

I formati di immagine supportati sono BMP, JPG, PNG e GIF. Se l'immagine è un file BMP a 8 bit, i relativi valori di tonalità e **saturazione** possono essere modificati dinamicamente usando gli attributi **hueShift** e saturation.

Quando **l'attributo disabled** di **un elemento BUTTONELEMENT** è impostato su true, viene visualizzata l'area corrispondente di **disabledImage** per **BUTTONGROUP.** Se l'immagine disabilitata è più grande dell'area definita, l'immagine disabilitata verrà ritagliata.

Se non è possibile recuperare l'immagine, viene visualizzata un'immagine predefinita (l'immagine rossa-x).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP.hueShift**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTONGROUP.saturation**](buttongroup-saturation.md)
</dt> </dl>

 

 





