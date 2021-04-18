---
title: BUTTON. hoverDownImage
description: L'attributo hoverDownImage specifica o recupera l'immagine visualizzata quando il pulsante è nello stato di inattività e l'utente passa il puntatore del mouse su di esso.
ms.assetid: 06645307-50f1-400d-aa73-c48d0fba3ee1
keywords:
- BUTTON. hoverDownImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bc8221875656c38a35eb6539dce25f58133984f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325453"
---
# <a name="buttonhoverdownimage"></a>BUTTON. hoverDownImage

L'attributo **hoverDownImage** specifica o recupera l'immagine visualizzata quando il **pulsante** è nello stato di inattività e l'utente passa il puntatore del mouse su di esso.

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura contenente il nome del file di immagine.

## <a name="remarks"></a>Commenti

I formati di immagine supportati sono BMP, JPG, PNG e GIF.

L'immagine predefinita è quella specificata nell'attributo **downImage** o il relativo valore predefinito.

Se l'immagine al passaggio del mouse è più grande dell'area definita nell'attributo di ambiente, l'immagine al passaggio del mouse verrà ritagliata.

Se non è possibile recuperare l'immagine, viene visualizzata un'immagine predefinita, ovvero l'immagine rossa (x).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BUTTON. downImage**](button-downimage.md)
</dt> </dl>

 

 





