---
title: SLIDER.slide
description: L'attributo slide specifica o recupera un valore che indica se l'immagine in primo piano scorre sull'immagine di sfondo o viene gradualmente rivelata in una posizione statica sull'immagine di sfondo.
ms.assetid: dc68c2a0-d3fe-4984-9607-12703a27edbd
keywords:
- Slider.slide Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.slide
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5d1a9480a171372ff5c90990d07bd583bd880570472b25af8d1ada945b31a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117933509"
---
# <a name="sliderslide"></a>SLIDER.slide

**L'attributo slide** specifica o recupera un valore che indica se l'immagine in primo piano scorre sull'immagine di sfondo o viene gradualmente rivelata in una posizione statica sull'immagine di sfondo.

``` syntax
        elementID.slide
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un valore booleano di **lettura/scrittura.**



| Valore | Descrizione                                                          |
|-------|----------------------------------------------------------------------|
| true  | Valore predefinito. L'immagine in primo piano scorre sull'immagine di sfondo.      |
| false | L'immagine in primo piano viene rivelata sul posto rispetto all'immagine di sfondo. |



 

## <a name="remarks"></a>Commenti

Quando il dispositivo **di scorrimento thumbImage** viene spostato con il mouse, se la diapositiva è impostata su true, l'immagine in primo piano scorre come se fosse trascinata dal dispositivo di scorrimento per coprire l'immagine di sfondo.  Se **la diapositiva** è impostata su false, l'immagine in primo piano non si sposta, ma viene rivelata sul posto, come se il dispositivo di scorrimento sposta l'immagine di sfondo fuori dall'immagine in primo piano.

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

[**SLIDER.foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





