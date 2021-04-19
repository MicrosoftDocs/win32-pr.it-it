---
title: SLIDER. foregroundColor
description: L'attributo foregroundColor specifica o Recupera il colore di primo piano del controllo dispositivo di scorrimento.
ms.assetid: 8c8de4a9-0021-41ed-aeb8-75653855b6f1
keywords:
- Media Player Windows SLIDER. foregroundColor
topic_type:
- apiref
api_name:
- SLIDER.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d334dff4d9b7d90582e44018bf8f56c04fa784a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332246"
---
# <a name="sliderforegroundcolor"></a>SLIDER. foregroundColor

L'attributo **ForegroundColor** specifica o Recupera il colore di primo piano del controllo dispositivo di scorrimento.

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura contenente qualsiasi valore di colore di Microsoft Internet Explorer. Il valore predefinito è "white".

## <a name="remarks"></a>Commenti

È possibile creare un controllo dispositivo di scorrimento di base specificando una delle due coppie di attributi: **BackgroundColor** e **ForegroundColor** oppure **BackgroundImage** e **foregroundImage**.

Quando si crea un controllo dispositivo di scorrimento usando gli attributi di colore, le dimensioni del controllo dispositivo di scorrimento definiscono l'area riempita dal colore di sfondo. Il colore di primo piano copre il colore di sfondo quando aumenta la posizione del dispositivo di scorrimento.

Per creare un riempimento sfumato nell'area occupata dal colore di sfondo o di primo piano, specificare gli attributi **backgroundEndColor** o **foregroundEndColor** .

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

[**SLIDER. backgroundColor**](slider-backgroundcolor.md)
</dt> <dt>

[**SLIDER. backgroundEndColor**](slider-backgroundendcolor.md)
</dt> <dt>

[**SLIDER. foregroundEndColor**](slider-foregroundendcolor.md)
</dt> <dt>

[**SLIDER. foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





