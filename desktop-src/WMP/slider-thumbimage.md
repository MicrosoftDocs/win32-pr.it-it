---
title: SLIDER. thumbImage
description: L'attributo thumbImage specifica o recupera l'immagine che verrà usata per rappresentare la posizione corrente del dispositivo di scorrimento.
ms.assetid: 3aa69188-3443-483c-81a9-bf22832509d8
keywords:
- Media Player Windows SLIDER. thumbImage
topic_type:
- apiref
api_name:
- SLIDER.thumbImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b798dfbae24fe2cef3669d2fb372966e47254026
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331578"
---
# <a name="sliderthumbimage"></a>SLIDER. thumbImage

L'attributo **thumbImage** specifica o recupera l'immagine che verrà usata per rappresentare la posizione corrente del dispositivo di scorrimento.

``` syntax
        elementID.thumbImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura contenente il nome di un file di immagine.

## <a name="remarks"></a>Commenti

**ThumbImage** specifica l'immagine che verrà usata per rappresentare la posizione corrente, oltre a indicare che l'utente può eseguire un'azione con il controllo. Se non viene specificata alcuna immagine Thumb, il dispositivo di scorrimento non è interattivo.

L'immagine Thumb è centrata nella dimensione stretta del controllo dispositivo di scorrimento. Se l'immagine Thumb è più stretta del controllo, l'immagine viene visualizzata al centro dello sfondo. Se l'immagine Thumb è più grande del controllo, le estremità dell'immagine vengono tagliate.

La posizione del dispositivo di scorrimento è specificata dal centro dell'immagine Thumb. Se **borderSize** è zero, solo metà dell'immagine Thumb sarà visibile nelle posizioni iniziale e finale del dispositivo di scorrimento. Per evitare questo problema, impostare **borderSize** su un valore maggiore o uguale a metà della larghezza dell'immagine del cursore (o metà dell'altezza se **Direction** è impostato su "Vertical").

I formati supportati sono BMP, JPG, PNG e GIF (escluse le gif animate).

Vedere **CUSTOMSLIDER**. attributo [dimensione positionImage](customslider-positionimage.md) per un esempio che illustra come vengono utilizzati gli attributi dell'elemento **Slider** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER. borderSize**](slider-bordersize.md)
</dt> <dt>

[**SLIDER. Direction**](slider-direction.md)
</dt> </dl>

 

 





