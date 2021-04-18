---
title: SLIDER. backgroundImage
description: L'attributo backgroundImage specifica o recupera l'immagine di sfondo del dispositivo di scorrimento.
ms.assetid: 73757635-4d1c-4ed0-8721-0608cd85859c
keywords:
- Media Player Windows SLIDER. backgroundImage
topic_type:
- apiref
api_name:
- SLIDER.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1188756c16b13bef69dfd0bcd9a5b66560856f99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325123"
---
# <a name="sliderbackgroundimage"></a>SLIDER. backgroundImage

L'attributo **BackgroundImage** specifica o recupera l'immagine di sfondo del dispositivo di scorrimento.

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura contenente il nome di un file di immagine.

## <a name="remarks"></a>Commenti

Questo attributo è facoltativo. Quando si usano immagini per costruire un dispositivo di scorrimento, il valore **BackgroundImage** viene usato per l'immagine del dispositivo di scorrimento principale. **ThumbImage** rappresenta il dispositivo di scorrimento effettivo e può essere spostato usando il mouse. Sul dispositivo di scorrimento **thumbImage** è presente una riga invisibile in cui l'immagine di sfondo viene visualizzata su un lato della riga e l'immagine in primo piano viene visualizzata sull'altro lato.

Quando il dispositivo di scorrimento **thumbImage** viene spostato con il mouse, se la **diapositiva** è impostata su true, l'immagine in primo piano scorre come se venisse premuto dal dispositivo di scorrimento per coprire l'immagine di sfondo. Se la **diapositiva** è impostata su false, l'immagine in primo piano non viene spostata, ma viene rivelata sul posto, come se il dispositivo di scorrimento spostasse l'immagine di sfondo dall'immagine in primo piano.

Se l'attributo **affiancato** è impostato su true e l'immagine di sfondo è minore del controllo dispositivo di scorrimento, l'immagine verrà affiancata orizzontalmente o verticalmente a seconda dell'attributo **Direction** . Se l'attributo **borderSize** è impostato su un valore maggiore di zero, il numero specificato sarà il numero di pixel a partire da sinistra e a destra o superiore e inferiore dell'immagine (anche in questo caso, a seconda dell'attributo **Direction** ) che verrà riservato ai bordi del controllo dispositivo di scorrimento. In questo caso, solo la parte centrale dell'immagine viene usata per affiancare il resto del controllo.

I formati supportati sono BMP, JPG, PNG e GIF (escluse le gif animate).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER. foregroundImage**](slider-foregroundimage.md)
</dt> <dt>

[**SLIDER. Slide**](slider-slide.md)
</dt> <dt>

[**SLIDER. thumbImage**](slider-thumbimage.md)
</dt> </dl>

 

 





