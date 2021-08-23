---
title: SLIDER.foregroundImage
description: L'attributo foregroundImage specifica o recupera l'immagine in primo piano del dispositivo di scorrimento.
ms.assetid: f713fba8-e965-4fed-b323-8a513d1f13e6
keywords:
- Slider.foregroundImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7fad50a6e33ca4de5890dfca340e36aa2fdc0af0c0b938793eac4edc1dfb71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119735711"
---
# <a name="sliderforegroundimage"></a>SLIDER.foregroundImage

**L'attributo foregroundImage** specifica o recupera l'immagine in primo piano del dispositivo di scorrimento.

``` syntax
        elementID.foregroundImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura** contenente il nome di un file di immagine.

## <a name="remarks"></a>Commenti

Questo attributo è facoltativo. Quando si usano le immagini per costruire un controllo dispositivo di scorrimento, **backgroundImage viene** usato per l'immagine del dispositivo di scorrimento principale. ThumbImage **rappresenta** il dispositivo di scorrimento effettivo e può essere spostato usando il mouse. Sul dispositivo **di scorrimento thumbImage** è presente una linea invisibile in cui l'immagine di sfondo viene visualizzata su un lato della linea e l'immagine in primo piano viene visualizzata sull'altro lato.

Quando il dispositivo **di scorrimento thumbImage** viene spostato con il mouse, se la diapositiva è impostata su true, l'immagine in primo piano scorre come se fosse trascinata dal dispositivo di scorrimento per coprire l'immagine di sfondo.  Se **la diapositiva** è impostata su false, l'immagine in primo piano non si sposta, ma viene rivelata sul posto, come se il dispositivo di scorrimento sposta l'immagine di sfondo fuori dall'immagine in primo piano.

Se  l'attributo affiancato è impostato su true e l'immagine in primo piano è più piccola dell'area  di primo piano del controllo dispositivo di scorrimento, l'immagine verrà affiancata orizzontalmente o verticalmente, a seconda dell'attributo di direzione, per riempire lo spazio disponibile.

I formati supportati sono BMP, JPG, PNG e GIF (senza GIF animate).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER.backgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**SLIDER.slide**](slider-slide.md)
</dt> <dt>

[**SLIDER.thumbImage**](slider-thumbimage.md)
</dt> <dt>

[**SLIDER.value**](slider-value.md)
</dt> </dl>

 

 





