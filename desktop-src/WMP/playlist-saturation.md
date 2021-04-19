---
title: PLAYLIST. saturazione
description: L'attributo Saturation specifica o Recupera il valore di saturazione delle immagini a discesa.
ms.assetid: 4c5dd3d9-828a-45c9-896a-9a702d354544
keywords:
- Media Player Windows PLAYLIST. Saturation
topic_type:
- apiref
api_name:
- PLAYLIST.saturation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82eb53afeafb0754f0e754f68fd5ff785eaade8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326714"
---
# <a name="playlistsaturation"></a>PLAYLIST. saturazione

L'attributo **Saturation** specifica o Recupera il valore di saturazione delle immagini a discesa.

``` syntax
        elementID.saturation
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **numero** di lettura/scrittura (**float**) con un valore compreso tra 0,0 e 2,0 e il cui valore predefinito è 1,0.

## <a name="remarks"></a>Commenti

Questo attributo modifica il valore di saturazione delle immagini specificate dagli attributi **dropDownBackgroundImage** e **dropDownImage** se sono state specificate e fanno riferimento a immagini BMP a 8 bit.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PLAYLIST (elemento)**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. dropDownBackgroundImage**](playlist-dropdownbackgroundimage.md)
</dt> <dt>

[**PLAYLIST. dropDownImage**](playlist-dropdownimage.md)
</dt> <dt>

[**PLAYLIST. hueShift**](playlist-hueshift.md)
</dt> </dl>

 

 





