---
title: BUTTONGROUP.hoverImage
description: L'attributo hoverImage specifica o recupera il nome dell'immagine che rappresenta lo stato del passaggio del mouse di un pulsante in BUTTONGROUP. Lo stato del passaggio del mouse si verifica quando il pulsante si trova nello stato verso l'alto e l'utente vi passa sopra con il mouse.
ms.assetid: 319b8770-8c4a-441a-ad03-9ff895958cf2
keywords:
- ButtonGROUP.hoverImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ee872c06d405d0f9cf5c09f59a86ba1962d0a5b349460c978e37fb5022f1d60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135904"
---
# <a name="buttongrouphoverimage"></a>BUTTONGROUP.hoverImage

**L'attributo hoverImage** specifica o recupera il nome dell'immagine che rappresenta lo stato del passaggio del mouse di un pulsante in **BUTTONGROUP.** Lo stato del passaggio del mouse si verifica quando il pulsante si trova nello stato verso l'alto e l'utente vi passa sopra con il mouse.

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura.**

## <a name="remarks"></a>Commenti

I formati di immagine supportati sono BMP, JPG, PNG e GIF. Se l'immagine è un file BMP a 8 bit, i relativi valori di tonalità e saturazione possono essere modificati dinamicamente usando gli attributi **hueShift** e **saturazione.**

L'immagine predefinita è quella specificata **nell'attributo image** o il relativo valore predefinito.

Se l'immagine al passaggio del mouse è più grande dell'area definita, l'immagine al passaggio del mouse verrà ritagliata.

Se non è possibile recuperare l'immagine, viene visualizzata un'immagine predefinita (l'immagine rossa-x).

## <a name="examples"></a>Esempio

Vedere *BUTTONELEMENT.* [Attributo mappingColor](buttonelement-mappingcolor.md) per un esempio che illustra l'uso di questo attributo.

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

[**BUTTONGROUP.image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP.saturation**](buttongroup-saturation.md)
</dt> </dl>

 

 





