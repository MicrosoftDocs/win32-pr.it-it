---
title: Effetto Posterize
description: L'effetto posterizza riduce il numero di colori univoci in un'immagine.
ms.assetid: e6686998-1246-b3b7-6f4f-212568c3191c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21372ee43935441168609cc81ef053ac96fd3fdbbd7cd3c16578f13d1a47fda1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636106"
---
# <a name="posterize-effect"></a>Effetto Posterize

L'effetto posterizza riduce il numero di colori univoci in un'immagine.

Il CLSID per questo effetto è CLSID \_ D2D1Posterize.

-   [Immagine di esempio](#example-image)
-   [Codice di esempio](#sample-code)
-   [Proprietà degli effetti](#effect-properties)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

![esempio di output dell'effetto](images/posterize-effect.png)

## <a name="sample-code"></a>Codice di esempio


```C++
ComPtr<ID2D1Effect> posterizeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Posterize, &posterizeEffect);
 
posterizeEffect->SetInput(0, bitmap);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_RED_VALUE_COUNT, 4);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_GREEN_VALUE_COUNT, 4);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_BLUE_VALUE_COUNT, 4);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(posterizeEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a>Proprietà degli effetti

Le proprietà per l'effetto posterize sono definite [**dall'enumerazione D2D1 \_ POSTERIZE \_ PROP.**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_posterize_prop)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|---------------------------------------------------|
| Client minimo supportato | \[Windows 10 app desktop \| Windows Store\] |
| Server minimo supportato | \[Windows 10 app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects \_ 2.h                                  |
| Libreria                  | d2d1.lib, dxguid.lib                              |

## <a name="related-topics"></a>Argomenti correlati

* [Interfaccia ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)


