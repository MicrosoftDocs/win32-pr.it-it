---
title: SLIDER. borderSize
description: L'attributo borderSize specifica o recupera lo spessore del bordo in pixel.
ms.assetid: ca766b45-1be3-4207-8cd0-ad50c33d52be
keywords:
- Media Player Windows SLIDER. borderSize
topic_type:
- apiref
api_name:
- SLIDER.borderSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c3ebc95e3ecf04ae78fa78c4b46f38fdd910004
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329991"
---
# <a name="sliderbordersize"></a>SLIDER. borderSize

L'attributo **borderSize** specifica o recupera lo spessore del bordo in pixel.

``` syntax
        elementID.borderSize
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **numero** di lettura/scrittura (**Long**) che rappresenta lo spessore del bordo in pixel. Il valore predefinito è zero.

## <a name="remarks"></a>Commenti

Questo attributo definisce un offset dall'inizio e dalla fine del controllo dispositivo di scorrimento, che è da sinistra a destra se l'attributo **Direction** è impostato su "Horizontal" e dall'alto verso il basso se è impostato su "Vertical". Queste posizioni di offset definiscono le posizioni minime e massime del cursore del dispositivo di scorrimento, oltre le quali non verrà applicato il colore di primo piano o l'immagine.

Se un'immagine di sfondo viene utilizzata con l'attributo **affiancato** impostato su true, l'offset viene applicato all'immagine, determinando la quantità dell'immagine, da sinistra a destra o dalla parte superiore e inferiore, da utilizzare per i bordi iniziale e finale del controllo dispositivo di scorrimento, con la parte centrale dell'immagine che viene affiancata nel resto. In questo modo, è possibile usare una piccola immagine di sfondo per coprire la lunghezza totale di un controllo dispositivo di scorrimento più grande.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER. foregroundColor**](slider-foregroundcolor.md)
</dt> <dt>

[**SLIDER. foregroundImage**](slider-foregroundimage.md)
</dt> <dt>

[**SLIDER. thumbImage**](slider-thumbimage.md)
</dt> <dt>

[**SLIDER. affiancato**](slider-tiled.md)
</dt> </dl>

 

 





