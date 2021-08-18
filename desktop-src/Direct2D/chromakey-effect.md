---
title: Effetto chiave chroma
description: Converte un determinato colore più o meno una tolleranza in alfa. Ad esempio, chroma-key può rimuovere lo sfondo di un'immagine per un effetto di sovrimpressione su schermo verde.
ms.assetid: f7bb5c65-f406-f947-c05d-2756cff99d21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 485cec7842c8460169b9c335eb74e9cc6d5a13e0541a49fc99835dfaa591efc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075590"
---
# <a name="chroma-key-effect"></a>Effetto chiave chroma

Converte un determinato colore più o meno una tolleranza in alfa. Ad esempio, chroma-key può rimuovere lo sfondo di un'immagine per un effetto di sovrimpressione su schermo verde.

Il CLSID per questo effetto è CLSID \_ D2D1ChromaKey.

-   [Immagine di esempio](#example-image)
-   [Codice di esempio](#sample-code)
-   [Proprietà degli effetti](#effect-properties)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

![esempio di output dell'effetto](images/chromakey-effect.png)

> [!Note]  
> In questo esempio, l'output dell'effetto chiave della chroma è la seconda immagine con lo sfondo trasparente della scacchiera. La terza immagine combina questa immagine con un'immagine di sfondo per la sovrimpressione finale dello schermo verde.

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

## <a name="effect-properties"></a>Proprietà degli effetti

Le proprietà per l'effetto chiave della chroma sono definite [**dall'enumerazione D2D1 \_ CHROMAKEY \_ PROP.**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_chromakey_prop)

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------------|---------------------------------------------------|
| Client minimo supportato | \[Windows 10 app desktop \| Windows Store\] |
| Server minimo supportato | \[Windows 10 app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects \_ 2.h                                  |
| Libreria                  | d2d1.lib, dxguid.lib                              |

## <a name="related-topics"></a>Argomenti correlati

* [Interfaccia ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
