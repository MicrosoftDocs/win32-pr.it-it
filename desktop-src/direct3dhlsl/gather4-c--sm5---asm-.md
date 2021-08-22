---
title: gather4_c (sm5 - asm)
description: Uguale a gather4, con la differenza che questa instruzione esegue il confronto sui texel, in modo simile all'esempio \_ c.
ms.assetid: 6265151A-36CE-4D31-B7B2-233CEEBDCF87
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b300e27743d08f3bbdf813de200b5a749a4ac25f16ab10458968731b9918c493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488691"
---
# <a name="gather4_c-sm5---asm"></a>gather4 \_ c (sm5 - asm)

Uguale a [**gather4**](gather4--sm5---asm-.md), con la differenza che questa instruzione esegue il confronto sui texel, in modo simile [**all'esempio \_ c**](sample-c--sm4---asm-.md).



| gather4 \_ c \[ \_ aoffimmi(u,v) \] dest \[ \] .mask, srcAddress \[ .swizzle, \] srcResource \[ .swizzle, \] srcSampler \[ . R, \] srcReferenceValue |
|-----------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                                       | Descrizione                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                                            | \[in \] Indirizzo del risultato dell'operazione<br/>                                    |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[in \] Un set di coordinate della trama.<br/>                                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[in \] Un registro trame.<br/>                                                           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[in \] Un registro sampler.<br/>                                                           |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[in \] Un registro con un singolo componente selezionato, usato nel confronto.<br/> |



 

## <a name="remarks"></a>Commenti

Vedere [**\_ l'esempio c**](sample-c--sm4---asm-.md) per una descrizione del confronto *tra srcReferenceValue* e ogni texel recuperato. A **differenza \_ dell'esempio c**, **gather4 \_ c** restituisce ogni risultato del confronto, anziché filtrarli.

Per gli angoli TextureCube, in cui sono presenti tre texel reali e un quarto deve essere sintetizzato, la sintesi deve verificarsi dopo il passaggio di confronto. Ciò significa che il risultato del confronto restituito per il texel sintetizzato può essere 0, 0,33, 0,66 o 1. Alcune implementazioni possono restituire solo 0 o 1 per il texel sintetizzato. Oltre a questo elenco di possibili risultati, il metodo per sintetizzare il texel non è specificato.

Per i formati con componenti float32, se il valore recuperato è normalizzato o +-INF, viene usato nell'operazione di confronto senza touched. NaN viene usato nell'operazione di confronto come NaN, ma la rappresentazione in bit esatta del NaN può essere modificata. I denorm vengono scaricati a zero nel confronto. Per TextureCubes, una sintesi del 4° texel mancante deve verificarsi agli angoli, quindi la nozione di restituire bit invariati per il texel sintetizzato non è applicabile.

I formati supportati *per gather4 \_ c* sono gli stessi supportati per l'esempio *\_ c*. Si tratta di formati a componente singolo, quindi . R in *srcSampler*, anziché uno swizzle arbitrario. **gather4 \_ c** in una risorsa non associata restituisce 0.

Usare questa istruzione per il filtro personalizzato della mappa ombreggiatura.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





