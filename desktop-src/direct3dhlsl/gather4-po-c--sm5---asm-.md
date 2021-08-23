---
title: gather4_po_c (sm5 - asm)
description: Si comporta come gather4 po, ad eccezione del fatto che esegue il confronto sui \_ texel, in modo simile all'esempio \_ c.
ms.assetid: B128EEF3-3440-4F00-9792-20FB1AE075E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83342aed97663c027b0915f612b13b288192d937d29d364257004cfc8966aec9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743871"
---
# <a name="gather4_po_c-sm5---asm"></a>gather4 \_ po \_ c (sm5 - asm)

Si comporta come [**gather4 \_ po**](gather4-po--sm5---asm-.md), ad eccezione del fatto che esegue il confronto sui texel, in modo simile [**all'esempio \_ c**](sample-c--sm4---asm-.md).



| gather4 \_ po \_ c dest \[ \] .mask, srcAddress \[ .swizzle, \] srcOffset \[ .swizzle, \] srcResource \[ .swizzle, \] srcSampler \[ . R, \] srcReferenceValue |
|-------------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                                       | Descrizione                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                                            | \[in \] Indirizzo del risultato dell'operazione.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[in \] Un set di coordinate della trama.<br/>               |
| <span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*<br/>                                 | \[in \] Offset.<br/>                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[in \] Un registro trame.<br/>                         |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[in \] Un registro sampler.<br/>                         |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[in \] Componente singolo selezionato.<br/>                  |



 

## <a name="remarks"></a>Commenti

Per informazioni sul confronto di *srcReferenceValue* con ogni texel recuperato, vedere l'esempio [**\_ c.**](sample-c--sm4---asm-.md) A **differenza \_ dell'esempio c**, *gather4 po \_ \_ c* restituisce ogni risultato del confronto, anziché filtrarli.

Questa istruzione, ad **esempio gather4 \_ po**, funziona solo con trame 2D. Questa operazione è diversa [**da gather4 \_ c**](gather4-c--sm5---asm-.md), che funziona anche con TextureCubes.

Per i formati con componenti float32, se il valore recuperato è normalizzato o +-INF, viene usato nell'operazione di confronto senza touched. NaN viene usato nell'operazione di confronto come NaN, ma la rappresentazione in bit esatta del NaN può essere modificata. I denorm vengono scaricati a zero nel confronto. Per TextureCubes, una sintesi del 4° texel mancante deve verificarsi agli angoli, quindi la nozione di restituire bit invariati per il texel sintetizzato non è applicabile.

I formati supportati **per gather4 \_ po \_ c** sono gli stessi supportati per l'esempio **\_ c**. Si tratta di formati a componente singolo, quindi . R in srcSampler, anziché uno swizzle arbitrario.

**gather4 \_ po \_ c** in una risorsa non associata restituisce 0.

Usare questo metodo per il filtro delle mappe ombreggiate.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello shader minimo

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

 

 





