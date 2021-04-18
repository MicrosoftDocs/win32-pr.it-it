---
title: BUTTON. disabledImage
description: L'attributo disabledImage specifica o recupera l'immagine visualizzata quando il pulsante è disabilitato.
ms.assetid: b5654323-589a-45da-9534-6fa67c3a4c4b
keywords:
- BUTTON. disabledImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eac407f6e7fbdd155f4bcabe98cecc0546f7d97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324585"
---
# <a name="buttondisabledimage"></a>BUTTON. disabledImage

L'attributo **disabledImage** specifica o recupera l'immagine visualizzata quando il **pulsante** è disabilitato.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura contenente il nome del file di immagine.

## <a name="remarks"></a>Commenti

I formati di immagine supportati sono BMP, JPG, PNG e GIF.

Questa immagine verrà visualizzata ogni volta che l'attributo **disabled** del controllo è impostato su true. Se l'immagine disabilitata è più grande dell'area definita, l'immagine disabilitata verrà ritagliata.

Se non è possibile recuperare l'immagine, viene visualizzata un'immagine predefinita, ovvero l'immagine rossa (x).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> </dl>

 

 





