---
title: Modello shader HLSL 6.4
description: Descrive le funzioni intrinseche di Machine Learning aggiunte al modello shader HLSL 6.4.
ms.topic: article
ms.date: 02/21/2019
ms.openlocfilehash: 5e161d77439eef63547d92fcc4f47e3185ac798141d20017d7e7102ee86a38cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511835"
---
# <a name="hlsl-shader-model-64"></a>Modello shader HLSL 6.4

Descrive le funzioni intrinseche di Machine Learning aggiunte al modello shader HLSL 6.4.

## <a name="shader-model-64"></a>Modello shader 6.4
Queste funzioni intrinseche sono una funzionalità obbligatoria/supportata del modello Shader 6.4. Di conseguenza, non è necessario alcun controllo separato dei bit di funzionalità, oltre a assicurare l'uso di Shader Model 6.4. Il client minimo supportato per queste routine è Windows 10 versione 1903.

## <a name="shading-language-intrinsics"></a>Intrinseci del linguaggio di ombreggiatura

### <a name="unsigned-integer-dot-product-of-4-elements-and-accumulate"></a>Numero intero senza segno Dot-Product di 4 elementi e accumulato
```syntax
uint32 dot4add_u8packed(uint32 a, uint32 b, uint32 acc); // ubyte4 a, b;
```
 
Intero senza segno a 4 dimensioni dot-product con add. Moltiplica ogni coppia corrispondente di byte int senza segno a 8 bit nei due DWORD di input e somma i risultati nell'accumulatore di interi senza segno a 32 bit. Questa istruzione opera all'interno di una singola corsia SIMD a 32 bit. Si presuppone anche che gli input siano quantità a 32 bit.
 
### <a name="signed-integer-dot-product-of-4-elements-and-accumulate"></a>Numero intero Dot-Product di 4 elementi e accumulato
```syntax
int32 dot4add_i8packed(uint32 a, uint32 b, int32 acc); // signed byte4 a, b;
```

Intero con segno a 4 dimensioni dot-product con add. Moltiplica insieme ogni coppia corrispondente di byte int con segno a 8 bit nei due DWORD di input e somma i risultati nell'accumulatore di interi con segno a 32 bit. Questa istruzione opera all'interno di una singola corsia SIMD a 32 bit. Si presuppone anche che gli input siano quantità a 32 bit.
 
### <a name="single-precision-floating-point-2-element-dot-product-and-accumulate"></a>Single Precision Floating Point 2-Element Dot-Product e Accumulate
```syntax
float dot2add( half2 a, half2 b, float acc );
```

Punto a virgola mobile bidimensionale di half2 vettori con add. Moltiplica gli elementi dei due vettori di input float a mezza precisione e somma i risultati nell'accumulatore float a 32 bit. Queste istruzioni funzionano all'interno di una singola corsia SIMD a 32 bit. Gli input sono quantità a 16 bit imballate nella stessa corsia.

Questo problema è trattato nel bit di funzionalità a bassa precisione ( che indica che sono presenti il supporto nativo di metà e breve).

### <a name="sv_shadingrate"></a>SV_ShadingRate
```syntax
uint shadingRate : SV_ShadingRate
```

Intero senza segno che rappresenta il numero di pixel di destinazione scritti da ogni chiamata del pixel shader. I valori validi appartengono al set di valori di [enumerazione D3D12_SHADING_RATE](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate).

Questo valore di sistema è disponibile nelle piattaforme che sono [D3D12_VARIABLE_SHADING_RATE_TIER_2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) o successive. Può essere scritto al massimo da una delle fasi vertex o geometry shader. Può essere letto dalla pixel shader passaggio. Per altre informazioni, vedere [l'oggetto Shading a velocità variabile.](../direct3d12/vrs.md)