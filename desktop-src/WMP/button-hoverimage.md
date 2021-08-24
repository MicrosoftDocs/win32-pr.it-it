---
title: BUTTON.hoverImage
description: L'attributo hoverImage specifica o recupera l'immagine visualizzata quando BUTTON è nello stato attivo e l'utente vi passa sopra con il puntatore del mouse.
ms.assetid: 6704e63d-1def-4e8e-808f-131c3cc1c0de
keywords:
- Button.hoverImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8488fb599a958a96ef7b5aaa5afbf4c219110f0da5be7016a8190efe2004475d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003721"
---
# <a name="buttonhoverimage"></a>BUTTON.hoverImage

**L'attributo hoverImage** specifica o recupera l'immagine visualizzata quando **BUTTON** è nello stato attivo e l'utente vi passa sopra con il puntatore del mouse.

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura contenente** il nome del file di immagine.

## <a name="remarks"></a>Commenti

I formati di immagine supportati sono BMP, JPG, PNG e GIF.

L'immagine predefinita è quella specificata **nell'attributo image** o il relativo valore predefinito.

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

[**BUTTON.image**](button-image.md)
</dt> </dl>

 

 





