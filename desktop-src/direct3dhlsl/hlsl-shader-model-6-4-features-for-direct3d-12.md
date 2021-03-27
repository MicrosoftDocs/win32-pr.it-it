---
title: Modello HLSL shader 6,4
description: Descrive gli intrinseci di Machine Learning aggiunti al modello HLSL shader 6,4.
ms.topic: article
ms.date: 02/21/2019
ms.openlocfilehash: 10e74b268243ab059c2d0945887a6d429d40bb53
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "103886050"
---
# <a name="hlsl-shader-model-64"></a>Modello HLSL shader 6,4

Descrive gli intrinseci di Machine Learning aggiunti al modello HLSL shader 6,4.

## <a name="shader-model-64"></a>Modello shader 6,4
Queste funzioni intrinseche sono una funzionalità obbligatoria/supportata del modello shader 6,4. Di conseguenza, non è necessario alcun controllo del bit di funzionalità separato, oltre a garantire l'uso del modello di shader 6,4. Il client minimo supportato per queste routine è Windows 10, versione 1903.

## <a name="shading-language-intrinsics"></a>Funzioni intrinseche di linguaggio ombreggiatura

### <a name="unsigned-integer-dot-product-of-4-elements-and-accumulate"></a>Intero senza segno Dot-Product di 4 elementi e accumulo
```syntax
uint32 dot4add_u8packed(uint32 a, uint32 b, uint32 acc); // ubyte4 a, b;
```
 
Un prodotto Unsigned Integer a 4 dimensioni con aggiunta. Moltiplica insieme ogni coppia corrispondente di byte int a 8 bit senza segno nei due DWORD di input e somma i risultati nell'accumulatore Unsigned Integer a 32 bit. Questa istruzione funziona all'interno di una singola SIMD Lane a 32 bit. Si presuppone che gli input siano anche di quantità a 32 bit.
 
### <a name="signed-integer-dot-product-of-4-elements-and-accumulate"></a>Intero con segno Dot-Product di 4 elementi e accumulo
```syntax
int32 dot4add_i8packed(uint32 a, uint32 b, int32 acc); // signed byte4 a, b;
```

Intero con segno a 4 dimensioni-prodotto con aggiunta. Moltiplica insieme ogni coppia corrispondente di byte int a 8 bit con segno nei due valori DWORD di input e somma i risultati nell'accumulatore di interi con segno a 32 bit. Questa istruzione funziona all'interno di una singola SIMD Lane a 32 bit. Si presuppone che gli input siano anche di quantità a 32 bit.
 
### <a name="single-precision-floating-point-2-element-dot-product-and-accumulate"></a>Dot-Product e accumulo a virgola mobile a precisione singola a 2 elementi
```syntax
float dot2add( half2 a, half2 b, float acc );
```

Prodotto a virgola mobile a virgola mobile bidimensionale di vettori Half2 con Add. Moltiplica gli elementi dei due vettori di input float a metà precisione insieme e somma i risultati nell'accumulatore float a 32 bit. Queste istruzioni operano all'interno di una singola SIMD Lane a 32 bit. Gli input sono quantità a 16 bit compressi nella stessa corsia.

Questa operazione viene illustrata sotto il bit di funzionalità a bassa precisione, che indica che sono presenti la metà nativa e il supporto breve.

### <a name="sv_shadingrate"></a>SV_ShadingRate
```syntax
uint shadingRate : SV_ShadingRate
```

Unsigned Integer che rappresenta il numero di pixel di destinazione scritti da ogni chiamata del pixel shader. I valori validi appartengono al set di valori di enumerazione [D3D12_SHADING_RATE](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate).

Questo valore di sistema è disponibile sulle piattaforme [D3D12_VARIABLE_SHADING_RATE_TIER_2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) o versioni successive. Può essere scritta al massimo da una delle fasi vertex o geometry shader. Può essere letto dalla fase pixel shader. Per altre informazioni, vedere [ombreggiatura a frequenza variabile](../direct3d12/vrs.md).