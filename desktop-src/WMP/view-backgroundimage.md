---
title: VIEW.backgroundImage
description: L'attributo backgroundImage specifica o recupera l'immagine di sfondo di VIEW o SUBVIEW.
ms.assetid: 60ffb257-2f43-4ae3-869d-3eb981ef4ae7
keywords:
- VIEW.backgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1de8bcbd0eb47f03aaff46b4292a8afe226ca8a221ec570537351af8e509801
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761741"
---
# <a name="viewbackgroundimage"></a>VIEW.backgroundImage

**L'attributo backgroundImage** specifica o recupera l'immagine di sfondo di **VIEW** **o SUBVIEW.**

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura.**

## <a name="remarks"></a>Commenti

I formati supportati sono BMP, JPG, GIF e PNG. Se l'immagine è un file BMP a 8 bit, i relativi valori di tonalità e saturazione possono essere modificati dinamicamente usando gli attributi **backgroundImageHueShift** e **backgroundImageSaturation.**

In un Windows di download multimediale, se si specifica l'attributo **backgroundImage** per un elemento **VIEW,** è necessario specificare anche l'attributo **backgroundColor** per tale elemento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento VIEW**](view-element.md)
</dt> <dt>

[**VIEW.backgroundImageHueShift**](view-backgroundimagehueshift.md)
</dt> <dt>

[**VIEW.backgroundImageSaturation**](view-backgroundimagesaturation.md)
</dt> </dl>

 

 





