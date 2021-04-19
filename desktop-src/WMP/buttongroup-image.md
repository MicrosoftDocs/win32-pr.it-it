---
title: BUTTONGROUP. image
description: L'attributo Image specifica o Recupera il nome dell'immagine che rappresenta i pulsanti di un BUTTONGROUP.
ms.assetid: dad50a1e-d147-4e0f-b5d6-8cbfeef32438
keywords:
- Media Player Windows BUTTONGROUP. image
topic_type:
- apiref
api_name:
- BUTTONGROUP.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fa395edc149671ad05a38a5ff7c77053b6e3d82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332140"
---
# <a name="buttongroupimage"></a>BUTTONGROUP. image

L'attributo **Image** specifica o Recupera il nome dell'immagine che rappresenta i pulsanti di un **ButtonGroup**.

``` syntax
        elementID.image
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura.

## <a name="remarks"></a>Commenti

I formati di immagine supportati sono BMP, JPG, PNG e GIF. Se l'immagine è un file BMP a 8 bit, i relativi valori di tonalità e saturazione possono essere modificati dinamicamente usando gli attributi **hueShift** e **Saturation** .

Se l'immagine del controllo è più grande dell'area definita, l'immagine verrà ritagliata.

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

 

 





