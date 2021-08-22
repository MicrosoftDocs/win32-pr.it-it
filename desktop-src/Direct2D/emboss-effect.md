---
title: Effetto Rilievo
description: Crea una versione in scala di grigi dell'immagine che viene visualizzata come se fosse stata stampata su carta.
ms.assetid: 74f63875-35cd-f335-62cd-410a953e53ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d0fe9b779cbad2b73b877338871f7adff3a36fb4bfb1c291be6de94f736088f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586966"
---
# <a name="emboss-effect"></a>Effetto Rilievo

Crea una versione in scala di grigi dell'immagine che viene visualizzata come se fosse stata stampata su carta.

Il CLSID per questo effetto è CLSID \_ D2D1Emboss.

-   [Immagine di esempio](#example-image)
-   [Codice di esempio](#sample-code)
-   [Proprietà degli effetti](#effect-properties)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

![Esempio di output dell'effetto](images/emboss-effect.png)

## <a name="sample-code"></a>Codice di esempio

```cpp
ComPtr<ID2D1Effect> embossEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Emboss, &embossEffect);
 
embossEffect->SetInput(0, bitmap);
embossEffect->SetValue(D2D1_EMBOSS_PROP_HEIGHT, 1.0f);
embossEffect->SetValue(D2D1_EMBOSS_PROP_DIRECTION, 0.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(embossEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Proprietà degli effetti

Le proprietà per l'effetto rilievo sono definite dall'enumerazione [**PROP D2D1 \_ EMBOSS. \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_emboss_prop)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|---------------------------------------------------|
| Client minimo supportato | \[Windows 10 app desktop \| Windows Store\] |
| Server minimo supportato | \[Windows 10 app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects \_ 2.h                                  |
| Libreria                  | d2d1.lib, dxguid.lib                              |

## <a name="related-topics"></a>Argomenti correlati

* [Interfaccia ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
