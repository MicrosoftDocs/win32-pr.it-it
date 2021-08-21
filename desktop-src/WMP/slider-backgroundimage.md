---
title: SLIDER.backgroundImage
description: L'attributo backgroundImage specifica o recupera l'immagine di sfondo del dispositivo di scorrimento.
ms.assetid: 73757635-4d1c-4ed0-8721-0608cd85859c
keywords:
- SLIDER.backgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2c4f6d31e3f870541310b23544a15c7b9af0043014a9013310cea7dd4ee072
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118832998"
---
# <a name="sliderbackgroundimage"></a>SLIDER.backgroundImage

**L'attributo backgroundImage** specifica o recupera l'immagine di sfondo del dispositivo di scorrimento.

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura** contenente il nome di un file di immagine.

## <a name="remarks"></a>Commenti

Questo attributo è facoltativo. Quando si usano immagini per costruire un dispositivo di scorrimento, **backgroundImage** viene usato per l'immagine del dispositivo di scorrimento principale. ThumbImage **rappresenta** il dispositivo di scorrimento effettivo e può essere spostato usando il mouse. Nel dispositivo **di scorrimento thumbImage** è presente una linea invisibile in cui l'immagine di sfondo viene visualizzata su un lato della linea e l'immagine in primo piano viene visualizzata sull'altro lato.

Quando il **dispositivo di scorrimento thumbImage** viene spostato con il mouse, se **la** diapositiva è impostata su true, l'immagine in primo piano scorre come se fosse trascinata dal dispositivo di scorrimento per coprire l'immagine di sfondo. Se **la diapositiva** è impostata su false, l'immagine in primo piano non viene spostata, ma viene rivelata sul posto, come se il dispositivo di scorrimento sposta l'immagine di sfondo fuori dall'immagine in primo piano.

Se **l'attributo affiancato** è impostato su true e l'immagine di sfondo è più piccola del controllo dispositivo di scorrimento, l'immagine verrà affiancata orizzontalmente o verticalmente a seconda **dell'attributo direction.** Se l'attributo **borderSize** è impostato su un valore maggiore di zero, il numero specificato sarà il numero di pixel  da sinistra, destra o superiore e inferiore dell'immagine (anche in questo caso, a seconda dell'attributo direction) che verranno riservati ai bordi del controllo dispositivo di scorrimento. In questo caso, viene usata solo la parte centrale dell'immagine per affiancare il resto del controllo.

I formati supportati sono BMP, JPG, PNG e GIF (senza includere gif animate).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER.foregroundImage**](slider-foregroundimage.md)
</dt> <dt>

[**SLIDER.slide**](slider-slide.md)
</dt> <dt>

[**SLIDER.thumbImage**](slider-thumbimage.md)
</dt> </dl>

 

 





