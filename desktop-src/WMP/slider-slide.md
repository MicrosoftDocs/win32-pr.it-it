---
title: SLIDER. Slide
description: L'attributo Slide specifica o recupera un valore che indica se l'immagine in primo piano scorre sull'immagine di sfondo o viene rivelata gradualmente in una posizione statica sull'immagine di sfondo.
ms.assetid: dc68c2a0-d3fe-4984-9607-12703a27edbd
keywords:
- Media Player SLIDER. Slide Windows
topic_type:
- apiref
api_name:
- SLIDER.slide
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9f79b5016b323380c5a4d06c8af7ab5fb0b8a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330720"
---
# <a name="sliderslide"></a>SLIDER. Slide

L'attributo **Slide** specifica o recupera un valore che indica se l'immagine in primo piano scorre sull'immagine di sfondo o viene rivelata gradualmente in una posizione statica sull'immagine di sfondo.

``` syntax
        elementID.slide
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione                                                          |
|-------|----------------------------------------------------------------------|
| true  | Valore predefinito. L'immagine di primo piano scorre sull'immagine di sfondo.      |
| false | L'immagine in primo piano viene rivelata sul posto sull'immagine di sfondo. |



 

## <a name="remarks"></a>Commenti

Quando il dispositivo di scorrimento **thumbImage** viene spostato con il mouse, se la **diapositiva** è impostata su true, l'immagine in primo piano scorre come se venisse premuto dal dispositivo di scorrimento per coprire l'immagine di sfondo. Se la **diapositiva** è impostata su false, l'immagine in primo piano non viene spostata, ma viene rivelata sul posto, come se il dispositivo di scorrimento spostasse l'immagine di sfondo dall'immagine in primo piano.

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

[**SLIDER. foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





