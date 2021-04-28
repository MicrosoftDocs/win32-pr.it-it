---
title: Temperatura ed effetto tinta
description: Temperatura e effetto tinta
ms.assetid: 8df72105-26ea-2dea-a4de-ef06902b7e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2c3628e1fdcb1c72a84a9e08736e4215d55514
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096639"
---
# <a name="temperature-and-tint-effect"></a>Temperatura e effetto tinta

Il CLSID per questo effetto è CLSID \_ D2D1TemperatureTint.

## <a name="sample-code"></a>Codice di esempio

```cpp
ComPtr<ID2D1Effect> temperatureTintEffect;
m_d2dContext->CreateEffect(CLSID_D2D1TemperatureTint, &temperatureTintEffect);
 
temperatureTintEffect->SetInput(0, bitmap);
temperatureTintEffect->SetValue(D2D1_TEMPERATUREANDTINT_PROP_TEMPERATURE, 0.5f);
temperatureTintEffect->SetValue(D2D1_TEMPERATUREANDTINT_PROP_TINT, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(temperatureTintEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Proprietà degli effetti

Le proprietà per l'effetto temperatura e tinta sono definite dall'enumerazione [**D2D1 \_ TEMPERATUREANDTINT \_ PROP.**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_temperatureandtint_prop)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|---------------------------------------------------|
| Client minimo supportato | Windows 10 app \[ desktop \| di Windows Store\] |
| Server minimo supportato | Windows 10 app \[ desktop \| di Windows Store\] |
| Intestazione                   | d2d1effects \_ 2.h                                  |
| Libreria                  | d2d1.lib, dxguid.lib                              |



 

## <a name="related-topics"></a>Argomenti correlati

* [Interfaccia ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
