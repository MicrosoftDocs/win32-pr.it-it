---
title: Effetto contrasto
description: Aumenta o riduce il contrasto di un'immagine.
ms.assetid: c0cc0f86-f6d4-e951-0cdd-dbad488e0793
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f287b1309aceadc4709bae3b1c2101a06df32d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048472"
---
# <a name="contrast-effect"></a>Effetto contrasto

Aumenta o riduce il contrasto di un'immagine.

Il CLSID per questo effetto è CLSID \_ D2D1Contrast.

La funzione di contrasto modifica ogni valore del canale colori utilizzando due polinomi quadratici a tratti che soddisfano la continuità della pendenza nel punto (0,5, 0,5).

![a tratti polinomi quadratici che soddisfano la continuità della pendenza nel punto (0,5, 0,5)](images/contrast-effect-slope.png)

-   [Immagini di esempio](#example-images)
-   [Codice di esempio](#sample-code)
-   [Proprietà effetto](#effect-properties)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-images"></a>Immagini di esempio

Questo esempio mostra l'output dell'effetto con il contrasto massimo applicato (contrasto = 1,0).

Prima

![immagine prima dell'applicazione dell'effetto](images/contrast-effect-before.png)

After

![immagine dopo l'applicazione dell'effetto](images/contrast-effect-after.png)

## <a name="sample-code"></a>Codice di esempio

```cpp
ComPtr<ID2D1Effect> contrastEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Contrast, &contrastEffect);
 
contrastEffect->SetInput(0, bitmap);
contrastEffect->SetValue(D2D1_CONTRAST_PROP_CONTRAST, 0.5f);
contrastEffect->SetValue(D2D1_CONTRAST_PROP_CLAMP_INPUT, TRUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(contrastEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Proprietà effetto

Le proprietà per l'effetto di contrasto sono definite dall'enumerazione [**d2d1 \_ contrasto \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_contrast_prop) .

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------------|---------------------------------------------------|
| Client minimo supportato | App \[ Windows 10 desktop app \| Windows Store\] |
| Server minimo supportato | App \[ Windows 10 desktop app \| Windows Store\] |
| Intestazione                   | d2d1effects \_ 2. h                                  |
| Libreria                  | d2d1. lib, dxguid. lib                              |

## <a name="related-topics"></a>Argomenti correlati

* [Interfaccia ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
