---
title: BUTTONGROUP.hoverDownImage
description: L'attributo hoverDownImage specifica o recupera il nome dell'immagine che rappresenta lo stato di passaggio del mouse verso il basso di un pulsante in BUTTONGROUP. Lo stato di passaggio del mouse si verifica quando il pulsante si trova nello stato verso il basso e l'utente passa il puntatore del mouse su di esso.
ms.assetid: dc048303-21d1-40ba-99bb-8d1c2f46628b
keywords:
- BUTTONGROUP.hoverDownImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c84d907a9b3fd1fc1a2eaf2dcf30337d016ae0732b147f435f49343d791b65c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119880"
---
# <a name="buttongrouphoverdownimage"></a>BUTTONGROUP.hoverDownImage

**L'attributo hoverDownImage** specifica o recupera il nome dell'immagine che rappresenta lo stato di passaggio del mouse verso il basso di un pulsante in **BUTTONGROUP.** Lo stato di passaggio del mouse si verifica quando il pulsante si trova nello stato verso il basso e l'utente passa il puntatore del mouse su di esso.

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura.**

## <a name="remarks"></a>Commenti

I formati di immagine supportati sono BMP, JPG, PNG e GIF. Se l'immagine è un file BMP a 8 bit, i relativi valori di tonalità e saturazione possono essere modificati dinamicamente usando gli attributi **hueShift** e **saturation.**

L'immagine predefinita è quella specificata **nell'attributo downImage** o il valore predefinito.

Se l'immagine al passaggio del mouse è più grande dell'area definita, l'immagine al passaggio del mouse verrà ritagliata.

Se non è possibile recuperare l'immagine, viene visualizzata un'immagine predefinita (l'immagine rossa-x).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP.downImage**](buttongroup-downimage.md)
</dt> <dt>

[**BUTTONGROUP.hueShift**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTONGROUP.saturation**](buttongroup-saturation.md)
</dt> </dl>

 

 





