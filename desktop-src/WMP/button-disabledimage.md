---
title: BUTTON.disabledImage
description: L'attributo disabledImage specifica o recupera l'immagine visualizzata quando BUTTON è disabilitato.
ms.assetid: b5654323-589a-45da-9534-6fa67c3a4c4b
keywords:
- Button.disabledImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c3768afd8b1356a1c0ca67a43f951e19143258dfc4f27a3a5e9d861fe9e930
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864481"
---
# <a name="buttondisabledimage"></a>BUTTON.disabledImage

**L'attributo disabledImage** specifica o recupera l'immagine visualizzata quando **BUTTON** è disabilitato.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura contenente** il nome del file di immagine.

## <a name="remarks"></a>Commenti

I formati di immagine supportati sono BMP, JPG, PNG e GIF.

Questa immagine verrà visualizzata ogni volta che **l'attributo** disabilitato del controllo è impostato su true. Se l'immagine disabilitata è più grande dell'area definita, l'immagine disabilitata verrà ritagliata.

Se non è possibile recuperare l'immagine, viene visualizzata un'immagine predefinita (l'immagine rossa-x).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> </dl>

 

 





