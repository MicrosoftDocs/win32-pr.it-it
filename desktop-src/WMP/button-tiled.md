---
title: BUTTON.tiled
description: L'attributo affiancato specifica o recupera un valore che indica se l'immagine BUTTON verrà affiancata.
ms.assetid: 5526477d-a235-4960-adef-5cf0ef9c46be
keywords:
- BUTTON.tiled Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32f4f1dda0b5a79749cfbffaa30f29522ff318a763ad50fcd005479afa9c8997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581375"
---
# <a name="buttontiled"></a>BUTTON.tiled

**L'attributo affiancato** specifica o recupera un valore che indica se l'immagine **BUTTON** verrà affiancata.

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un valore booleano di **lettura/scrittura.**



| Valore | Descrizione                       |
|-------|-----------------------------------|
| true  | L'immagine verrà affiancata.              |
| false | Valore predefinito. L'immagine non verrà affiancata. |



 

## <a name="remarks"></a>Commenti

Se l'immagine è più piccola dell'area effettiva del controllo, la affiancatura dell'immagine verrà ripetuta fino a riempire l'intera area. Se un'immagine non è specificata o non può essere recuperata, **il** riquadro verrà impostato su false.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BUTTON.image**](button-image.md)
</dt> </dl>

 

 





