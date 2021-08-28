---
title: Effetto Da tonalità a RGB
description: Converte un'immagine HSL (Hue, Saturation, Lightness) o HSV (Hue, Saturation, Value) nello spazio colore RGB.
ms.assetid: 18e92535-9e89-bf8d-b8c3-a49b645fc417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3abc45ec09cc77935c332a702648472e6be7edeb06bdf9237e4232f467b1e073
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118003132"
---
# <a name="hue-to-rgb-effect"></a>Effetto Da tonalità a RGB

Converte un'immagine HSL (Hue, Saturation, Lightness) o HSV (Hue, Saturation, Value) nello spazio colore RGB.

HSL e HSV sono due modelli diversi per rappresentare un colore RGB in uno spazio colore cilindrico. Sono utili perché consentono di ragionare su un colore usando concetti più intuitivi, ad esempio tonalità e intensità, rispetto alla combinazione di valori rosso, verde e blu.

Questo effetto passa attraverso qualsiasi valore alfa di input.

Il CLSID per questo effetto è CLSID \_ D2D1HueToRgb.

Per invertire il comportamento di questo effetto, usare [l'effetto RGB to Hue](rgb-to-hue-effect.md).

-   [Codice di esempio](#sample-code)
-   [Proprietà dell'effetto](#effect-properties)
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

## <a name="effect-properties"></a>Proprietà degli effetti

Le proprietà per l'effetto di contrasto sono definite dall'enumerazione [**D2D1 \_ HUETORGB \_ PROP.**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_huetorgb_prop)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|---------------------------------------------------|
| Client minimo supportato | \[Windows 10 app desktop \| Windows Store\] |
| Server minimo supportato | \[Windows 10 app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects \_ 2.h                                  |
| Libreria                  | d2d1.lib, dxguid.lib                              |



## <a name="related-topics"></a>Argomenti correlati

* [Interfaccia ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
