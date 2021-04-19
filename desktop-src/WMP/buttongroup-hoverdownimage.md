---
title: BUTTONGROUP. hoverDownImage
description: L'attributo hoverDownImage specifica o Recupera il nome dell'immagine che rappresenta lo stato di spostamento verso il basso di un pulsante in BUTTONGROUP. Lo stato di spostamento verso il basso si verifica quando il pulsante è nello stato di inattività e l'utente passa il mouse su di esso con il mouse.
ms.assetid: dc048303-21d1-40ba-99bb-8d1c2f46628b
keywords:
- Media Player Windows BUTTONGROUP. hoverDownImage
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a40788fafffd6eb4626bc834a941f7330c988fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324104"
---
# <a name="buttongrouphoverdownimage"></a>BUTTONGROUP. hoverDownImage

L'attributo **hoverDownImage** specifica o Recupera il nome dell'immagine che rappresenta lo stato di spostamento verso il basso di un pulsante in **ButtonGroup**. Lo stato di spostamento verso il basso si verifica quando il pulsante è nello stato di inattività e l'utente passa il mouse su di esso con il mouse.

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura.

## <a name="remarks"></a>Commenti

I formati di immagine supportati sono BMP, JPG, PNG e GIF. Se l'immagine è un file BMP a 8 bit, i relativi valori di tonalità e saturazione possono essere modificati dinamicamente usando gli attributi **hueShift** e **Saturation** .

L'immagine predefinita è quella specificata nell'attributo **downImage** o il relativo valore predefinito.

Se l'immagine al passaggio del mouse è più grande dell'area definita, l'immagine al passaggio del mouse verrà ritagliata.

Se non è possibile recuperare l'immagine, viene visualizzata un'immagine predefinita, ovvero l'immagine rossa (x).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP. downImage**](buttongroup-downimage.md)
</dt> <dt>

[**BUTTONGROUP. hueShift**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTONGROUP. saturazione**](buttongroup-saturation.md)
</dt> </dl>

 

 





