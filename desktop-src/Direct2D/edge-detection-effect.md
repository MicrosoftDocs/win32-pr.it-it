---
title: Effetto di rilevamento dei bordi
description: Filtra il contenuto di un'immagine, lasciando le linee ai bordi delle sezioni a contrasto dell'immagine.
ms.assetid: d22868cf-95fe-690e-66ac-268d7e116aee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7067243c19ed65bcdc23f1654999ff10ad3b80bafa641d0d3da940719db7bcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967067"
---
# <a name="edge-detection-effect"></a>Effetto di rilevamento dei bordi

Filtra il contenuto di un'immagine, lasciando le linee ai bordi delle sezioni a contrasto dell'immagine.

Il CLSID per questo effetto è CLSID \_ D2D1EdgeDetection.

-   [Immagine di esempio](#example-image)
-   [Codice di esempio](#sample-code)
-   [Proprietà dell'effetto](#effect-properties)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

![Esempio di output dell'effetto](images/edge-detection-effect.png)

## <a name="sample-code"></a>Codice di esempio

```cpp
ComPtr<ID2D1Effect> edgeDetectionEffect;
m_d2dContext->CreateEffect(CLSID_D2D1EdgeDetection, &edgeDetectionEffect);
 
edgeDetectionEffect->SetInput(0, bitmap);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_STRENGTH, 0.5f);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_BLUR_RADIUS, 0.0f);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_MODE, D2D1_EDGEDETECTION_MODE_SOBEL);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_OVERLAY_EDGES, false);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_ALPHA_MODE, D2D1_ALPHA_MODE_PREMULTIPLIED);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(edgeDetectionEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Proprietà degli effetti

Le proprietà per l'effetto di rilevamento dei bordi sono definite dall'enumerazione [**D2D1 \_ EDGEDETECTION \_ PROP.**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_edgedetection_prop)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|---------------------------------------------------|
| Client minimo supportato | \[Windows 10 app desktop \| Windows Store\] |
| Server minimo supportato | \[Windows 10 app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects \_ 2.h                                  |
| Libreria                  | d2d1.lib, dxguid.lib                              |

## <a name="related-topics"></a>Argomenti correlati

* [Interfaccia ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
