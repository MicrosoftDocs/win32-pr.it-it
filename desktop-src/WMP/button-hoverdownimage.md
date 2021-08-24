---
title: BUTTON.hoverDownImage
description: L'attributo hoverDownImage specifica o recupera l'immagine visualizzata quando button è in stato down e l'utente passa il puntatore del mouse su di essa.
ms.assetid: 06645307-50f1-400d-aa73-c48d0fba3ee1
keywords:
- Button.hoverDownImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcdb23f9806e36cebd2f5da6a46a8307c268861d73f68361e07f56e9ce09dcc5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902401"
---
# <a name="buttonhoverdownimage"></a>BUTTON.hoverDownImage

**L'attributo hoverDownImage** specifica o recupera l'immagine visualizzata quando **button** è in stato down e l'utente passa il mouse su di essa con il puntatore del mouse.

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura contenente** il nome del file di immagine.

## <a name="remarks"></a>Commenti

I formati di immagine supportati sono BMP, JPG, PNG e GIF.

L'immagine predefinita è quella specificata **nell'attributo downImage** o il valore predefinito.

Se l'immagine al passaggio del mouse è più grande dell'area definita nell'attributo di ambiente, l'immagine al passaggio del mouse verrà ritagliata.

Se non è possibile recuperare l'immagine, viene visualizzata un'immagine predefinita (l'immagine rossa-x).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BUTTON.downImage**](button-downimage.md)
</dt> </dl>

 

 





