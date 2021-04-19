---
title: Visualizza. backgroundImage
description: L'attributo backgroundImage specifica o recupera l'immagine di sfondo della vista o della vista.
ms.assetid: 60ffb257-2f43-4ae3-869d-3eb981ef4ae7
keywords:
- VIEW. backgroundImage Media Player Windows
topic_type:
- apiref
api_name:
- VIEW.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e96f4a93882e02589d7f15b74ba5cb225f506d69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325973"
---
# <a name="viewbackgroundimage"></a>Visualizza. backgroundImage

L'attributo **BackgroundImage** specifica o recupera l'immagine di sfondo della **vista** o **della vista.**

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura.

## <a name="remarks"></a>Commenti

I formati supportati sono BMP, JPG, GIF e PNG. Se l'immagine è un file BMP a 8 bit, i relativi valori di tonalità e saturazione possono essere modificati dinamicamente usando gli attributi **backgroundImageHueShift** e **backgroundImageSaturation** .

In un pacchetto di download di Windows Media, se si specifica l'attributo **BackgroundImage** per un elemento di **visualizzazione** , è necessario specificare anche l'attributo **BackgroundColor** per quell'elemento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento VIEW**](view-element.md)
</dt> <dt>

[**Visualizza backgroundImageHueShift**](view-backgroundimagehueshift.md)
</dt> <dt>

[**Visualizza backgroundImageSaturation**](view-backgroundimagesaturation.md)
</dt> </dl>

 

 





