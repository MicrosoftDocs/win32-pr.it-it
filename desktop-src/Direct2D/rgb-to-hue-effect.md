---
title: Effetto RGB-to-hue
description: Converte un'immagine RGB negli spazi colori HSL (Hue, Saturation, Lightness) o HSV (Hue, Saturation, Value).
ms.assetid: 1def972d-8172-9217-8ce7-abce4a93f6e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c474705d050c2ef2eff9050a759c60c5d8f1098440e06601ec1e3981e349aaff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160387"
---
# <a name="rgb-to-hue-effect"></a>Effetto RGB-to-hue

Converte un'immagine RGB negli spazi colori HSL (Hue, Saturation, Lightness) o HSV (Hue, Saturation, Value).

HSL e HSV sono due modelli diversi per rappresentare un colore RGB in uno spazio colore cilindrico. Sono utili perché consentono di pensare a un colore usando concetti più intuitivi come la tonalità e l'intensità rispetto alla combinazione di valori rosso, verde e blu.

Questo effetto normalizza i dati di output (tonalità, valore di saturazione per HSV o tonalità, saturazione, leggerezza per HSL) nell'intervallo \[ 0, 1 \] .

Il CLSID per questo effetto è CLSID \_ D2D1RgbToHue.

Per invertire il comportamento di questo effetto, usare [l'effetto Tonalità su RGB.](hue-to-rgb-effect.md)

-   [Codice di esempio](#sample-code)
-   [Proprietà degli effetti](#effect-properties)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="sample-code"></a>Codice di esempio


```C++
ComPtr<ID2D1Effect> rgbToHueEffect;
m_d2dContext->CreateEffect(CLSID_D2D1RgbToHue, &rgbToHueEffect);
 
rgbToHueEffect->SetInput(0, bitmap);
rgbToHueEffect->SetValue(D2D1_RGBTOHUE_PROP_OUTPUT_COLOR_SPACE, D2D1_RGBTOHUE_OUTPUT_COLOR_SPACE_HUE_SATURATION_VALUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(rgbToHueEffect.Get());
m_d2dContext->EndDraw();

```



## <a name="effect-properties"></a>Proprietà degli effetti

Le proprietà per l'effetto di contrasto sono definite [**dall'enumerazione \_ PROP RGBTOHUE \_ D2D1.**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_rgbtohue_prop)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|---------------------------------------------------|
| Client minimo supportato | \[Windows 10 app desktop \| Windows Store\] |
| Server minimo supportato | \[Windows 10 app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects \_ 2.h                                  |
| Libreria                  | d2d1.lib, dxguid.lib                              |


## <a name="related-topics"></a>Argomenti correlati

* [Interfaccia ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
