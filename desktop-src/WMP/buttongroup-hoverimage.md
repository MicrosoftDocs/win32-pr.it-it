---
title: BUTTONGROUP. hoverImage
description: L'attributo hoverImage specifica o Recupera il nome dell'immagine che rappresenta lo stato del passaggio del mouse su un pulsante in BUTTONGROUP. Lo stato del passaggio del mouse si verifica quando il pulsante si trova nello stato attivo e l'utente passa su di esso con il mouse.
ms.assetid: 319b8770-8c4a-441a-ad03-9ff895958cf2
keywords:
- Media Player Windows BUTTONGROUP. hoverImage
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 702a7aa73f5800628fdf14deb0dbfe142cd80dbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324103"
---
# <a name="buttongrouphoverimage"></a>BUTTONGROUP. hoverImage

L'attributo **hoverImage** specifica o Recupera il nome dell'immagine che rappresenta lo stato del passaggio del mouse su un pulsante in **ButtonGroup**. Lo stato del passaggio del mouse si verifica quando il pulsante si trova nello stato attivo e l'utente passa su di esso con il mouse.

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura.

## <a name="remarks"></a>Commenti

I formati di immagine supportati sono BMP, JPG, PNG e GIF. Se l'immagine è un file BMP a 8 bit, i relativi valori di tonalità e saturazione possono essere modificati dinamicamente usando gli attributi **hueShift** e **Saturation** .

L'immagine predefinita è quella specificata nell'attributo **Image** oppure il valore predefinito.

Se l'immagine del passaggio del mouse è maggiore della regione specificata, l'immagine del passaggio del mouse verrà ritagliata.

Se non è possibile recuperare l'immagine, viene visualizzata un'immagine predefinita, ovvero l'immagine rossa (x).

## <a name="examples"></a>Esempio

Vedere *ButtonElement*. attributo [mappingColor](buttonelement-mappingcolor.md) per un esempio che illustra l'uso di questo attributo.

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

[**BUTTONGROUP. image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP. saturazione**](buttongroup-saturation.md)
</dt> </dl>

 

 





