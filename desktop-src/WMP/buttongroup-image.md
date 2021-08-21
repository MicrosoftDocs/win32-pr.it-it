---
title: BUTTONGROUP.image
description: L'attributo image specifica o recupera il nome dell'immagine che rappresenta i pulsanti di UN BUTTONGROUP.
ms.assetid: dad50a1e-d147-4e0f-b5d6-8cbfeef32438
keywords:
- BUTTONGROUP.image Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2fcd8d76bd217087b6b948cec3216efc2bbc6c9845e9c18b5a7619d292232b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342634"
---
# <a name="buttongroupimage"></a>BUTTONGROUP.image

**L'attributo** image specifica o recupera il nome dell'immagine che rappresenta i pulsanti di **UN BUTTONGROUP.**

``` syntax
        elementID.image
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura.**

## <a name="remarks"></a>Commenti

I formati di immagine supportati sono BMP, JPG, PNG e GIF. Se l'immagine è un file BMP a 8 bit, i relativi valori di tonalità e saturazione possono essere modificati dinamicamente usando gli attributi **hueShift** e **saturation.**

Se l'immagine del controllo è più grande dell'area definita, l'immagine verrà ritagliata.

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

 

 





