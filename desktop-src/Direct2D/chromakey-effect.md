---
title: Effetto chiave Chroma
description: Converte un colore specificato più o meno una tolleranza in alfa. Ad esempio, Chroma-Key può rimuovere lo sfondo di un'immagine per un effetto di sovrapposizione della schermata verde.
ms.assetid: f7bb5c65-f406-f947-c05d-2756cff99d21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a13d5558d103d6f937ed6638d0debbeddaf71dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873637"
---
# <a name="chroma-key-effect"></a>Effetto chiave Chroma

Converte un colore specificato più o meno una tolleranza in alfa. Ad esempio, Chroma-Key può rimuovere lo sfondo di un'immagine per un effetto di sovrapposizione della schermata verde.

Il CLSID per questo effetto è CLSID \_ D2D1ChromaKey.

-   [Immagine di esempio](#example-image)
-   [Codice di esempio](#sample-code)
-   [Proprietà effetto](#effect-properties)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

![esempio di output di effetto](images/chromakey-effect.png)

> [!Note]  
> In questo esempio l'output dell'effetto della chiave Chroma è la seconda immagine con lo sfondo trasparente a scacchiera. La terza immagine combina questo oggetto con un'immagine di sfondo per la sovrimpressione finale dello schermo verde.

## <a name="sample-code"></a>Codice di esempio

```cppcx
ComPtr<ID2D1Effect> chromakeyEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ChromaKey, &chromakeyEffect);
 
chromakeyEffect->SetInput(0, bitmap);
chromaKeyEffect->SetValue(D2D1_CHROMAKEY_PROP_COLOR, {0.0f, 1.0f, 0.0f, 0.0f});
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_TOLERANCE, 0.2f);
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_INVERT_ALPHA, false);
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_FEATHER, false);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(chromakeyEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Proprietà effetto

Le proprietà per l'effetto della chiave Chroma sono definite dall'enumerazione [**d2d1 \_ CHROMAKEY \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_chromakey_prop) .

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------------|---------------------------------------------------|
| Client minimo supportato | App \[ Windows 10 desktop app \| Windows Store\] |
| Server minimo supportato | App \[ Windows 10 desktop app \| Windows Store\] |
| Intestazione                   | d2d1effects \_ 2. h                                  |
| Libreria                  | d2d1. lib, dxguid. lib                              |

## <a name="related-topics"></a>Argomenti correlati

* [Interfaccia ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
