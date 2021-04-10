---
title: Effetto tonalità-RGB
description: Converte un'immagine HSL (Hue, Saturation, luminosità) o HSV (Hue, Saturation, value) nello spazio colori RGB.
ms.assetid: 18e92535-9e89-bf8d-b8c3-a49b645fc417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82064d01281ab0edf2327f00cf6e852a0bebae53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964150"
---
# <a name="hue-to-rgb-effect"></a>Effetto tonalità-RGB

Converte un'immagine HSL (Hue, Saturation, luminosità) o HSV (Hue, Saturation, value) nello spazio colori RGB.

HSL e HSV sono due modelli diversi per la rappresentazione di un colore RGB in uno spazio di colore cilindrico. Sono utili perché consentono di ragionare su un colore usando concetti più intuitivi, ad esempio Hue e Intensity, e combinando i valori rosso, verde e blu.

Questo effetto passa tutti i valori alfa di input.

Il CLSID per questo effetto è CLSID \_ D2D1HueToRgb.

Per invertire il comportamento di questo effetto, usare l' [effetto RGB a tonalità](rgb-to-hue-effect.md).

-   [Codice di esempio](#sample-code)
-   [Proprietà effetto](#effect-properties)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="sample-code"></a>Codice di esempio

```cpp
ComPtr<ID2D1Effect> hueToRgbEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueToRgb, &hueToRgbEffect);
 
hueToRgbEffect->SetInput(0, bitmap);
hueToRgbEffect->SetValue(D2D1_HUETORGB_INPUT_COLOR_SPACE, D2D1_HUETORGB_INPUT_COLOR_SPACE_HUE_SATURATION_LIGHTNESS);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Proprietà effetto

Le proprietà per l'effetto contrasto sono definite dall'enumerazione [**d2d1 \_ HUETORGB \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_huetorgb_prop) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|---------------------------------------------------|
| Client minimo supportato | App \[ Windows 10 desktop app \| Windows Store\] |
| Server minimo supportato | App \[ Windows 10 desktop app \| Windows Store\] |
| Intestazione                   | d2d1effects \_ 2. h                                  |
| Libreria                  | d2d1. lib, dxguid. lib                              |



## <a name="related-topics"></a>Argomenti correlati

* [Interfaccia ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
