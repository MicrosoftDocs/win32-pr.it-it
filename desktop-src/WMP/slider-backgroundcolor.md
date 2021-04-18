---
title: SLIDER. backgroundColor
description: L'attributo backgroundColor specifica o Recupera il colore di sfondo del controllo dispositivo di scorrimento.
ms.assetid: 8f2c48ec-29f5-4fbe-aa62-c7cfb8a8678c
keywords:
- Windows SLIDER. backgroundColor Media Player
topic_type:
- apiref
api_name:
- SLIDER.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06cc595af13b28541fcc570e130da4e804fdeafe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325128"
---
# <a name="sliderbackgroundcolor"></a>SLIDER. backgroundColor

L'attributo **BackgroundColor** specifica o Recupera il colore di sfondo del controllo dispositivo di scorrimento.

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura contenente qualsiasi valore di colore di Microsoft Internet Explorer. e non prevede alcun valore predefinito.

## <a name="remarks"></a>Commenti

Un controllo dispositivo di scorrimento di base può essere creato specificando **BackgroundColor** o **BackgroundImage**, **ForegroundColor** o **foregroundImage**.

Quando si usano i colori, le dimensioni del controllo dispositivo di scorrimento definiscono l'area riempita dal colore di sfondo. Il colore di primo piano copre il colore di sfondo quando aumenta la posizione del dispositivo di scorrimento.

Per creare un riempimento sfumato dell'area occupata dal colore di sfondo o di primo piano, specificare gli attributi **backgroundEndColor** o **foregroundEndColor** .

Vedere *CUSTOMSLIDER*. attributo [dimensione positionImage](customslider-positionimage.md) per un esempio che illustra come vengono utilizzati gli attributi dell'elemento **Slider** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento ai colori**](color-reference.md)
</dt> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER. backgroundEndColor**](slider-backgroundendcolor.md)
</dt> <dt>

[**SLIDER. backgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**SLIDER. foregroundColor**](slider-foregroundcolor.md)
</dt> <dt>

[**SLIDER. foregroundEndColor**](slider-foregroundendcolor.md)
</dt> <dt>

[**SLIDER. foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





