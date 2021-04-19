---
title: SLIDER. foregroundImage
description: L'attributo foregroundImage specifica o recupera l'immagine in primo piano del dispositivo di scorrimento.
ms.assetid: f713fba8-e965-4fed-b323-8a513d1f13e6
keywords:
- Media Player Windows SLIDER. foregroundImage
topic_type:
- apiref
api_name:
- SLIDER.foregroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a286d3b73a2647160a0bd23357703f4fcb88d267
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332243"
---
# <a name="sliderforegroundimage"></a>SLIDER. foregroundImage

L'attributo **foregroundImage** specifica o recupera l'immagine in primo piano del dispositivo di scorrimento.

``` syntax
        elementID.foregroundImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura contenente il nome di un file di immagine.

## <a name="remarks"></a>Commenti

Questo attributo è facoltativo. Quando si utilizzano immagini per costruire un controllo dispositivo di scorrimento, la **BackgroundImage** viene utilizzata per l'immagine del dispositivo di scorrimento principale. **ThumbImage** rappresenta il dispositivo di scorrimento effettivo e può essere spostato usando il mouse. Sul dispositivo di scorrimento **thumbImage** è presente una riga invisibile in cui l'immagine di sfondo viene visualizzata su un lato della riga e l'immagine in primo piano viene visualizzata sull'altro lato.

Quando il dispositivo di scorrimento **thumbImage** viene spostato con il mouse, se la **diapositiva** è impostata su true, l'immagine in primo piano scorre come se venisse premuto dal dispositivo di scorrimento per coprire l'immagine di sfondo. Se la **diapositiva** è impostata su false, l'immagine in primo piano non viene spostata, ma viene rivelata sul posto, come se il dispositivo di scorrimento spostasse l'immagine di sfondo dall'immagine in primo piano.

Se l'attributo **affiancato** è impostato su true e l'immagine in primo piano è inferiore all'area di primo piano del controllo dispositivo di scorrimento, l'immagine verrà affiancata orizzontalmente o verticalmente, a seconda dell'attributo **Direction** , per riempire lo spazio disponibile.

I formati supportati sono BMP, JPG, PNG e GIF (escluse le gif animate).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER. backgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**SLIDER. Slide**](slider-slide.md)
</dt> <dt>

[**SLIDER. thumbImage**](slider-thumbimage.md)
</dt> <dt>

[**SLIDER. Value**](slider-value.md)
</dt> </dl>

 

 





