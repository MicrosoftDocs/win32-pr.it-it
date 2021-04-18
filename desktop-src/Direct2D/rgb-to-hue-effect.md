---
title: Effetto RGB-to-Hue
description: Converte un'immagine RGB negli spazi dei colori HSL (Hue, Saturation, Lightity) o HSV (Hue, Saturation, value).
ms.assetid: 1def972d-8172-9217-8ce7-abce4a93f6e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ccb4d3f67d116426d7a3497c04c4e8fb115b74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400540"
---
# <a name="rgb-to-hue-effect"></a>Effetto RGB-to-Hue

Converte un'immagine RGB negli spazi dei colori HSL (Hue, Saturation, Lightity) o HSV (Hue, Saturation, value).

HSL e HSV sono due modelli diversi per la rappresentazione di un colore RGB in uno spazio di colore cilindrico. Sono utili perché consentono di ragionare su un colore usando concetti più intuitivi, ad esempio Hue e Intensity, e combinando i valori rosso, verde e blu.

Questo effetto Normalizza i dati di output (tonalità, valore di saturazione per HSV o tonalità, saturazione, luminosità per HSL) nell'intervallo compreso tra \[ 0 e 1 \] .

Il CLSID per questo effetto è CLSID \_ D2D1RgbToHue.

Per invertire il comportamento di questo effetto, usare l' [effetto tonalità su RGB](hue-to-rgb-effect.md).

-   [Codice di esempio](#sample-code)
-   [Proprietà effetto](#effect-properties)
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



## <a name="effect-properties"></a>Proprietà effetto

Le proprietà per l'effetto contrasto sono definite dall'enumerazione [**d2d1 \_ RGBTOHUE \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_rgbtohue_prop) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|---------------------------------------------------|
| Client minimo supportato | App \[ Windows 10 desktop app \| Windows Store\] |
| Server minimo supportato | App \[ Windows 10 desktop app \| Windows Store\] |
| Intestazione                   | d2d1effects \_ 2. h                                  |
| Libreria                  | d2d1. lib, dxguid. lib                              |


## <a name="related-topics"></a>Argomenti correlati

* [Interfaccia ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
