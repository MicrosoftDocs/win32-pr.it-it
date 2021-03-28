---
title: gather4_po_c (SM5-ASM)
description: Si comporta allo stesso modo di gather4 \_ po, ad eccezione delle operazioni di confronto sui Texel, in modo simile all'esempio \_ c.
ms.assetid: B128EEF3-3440-4F00-9792-20FB1AE075E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b07dcad08b4d117a453a3c97e461e6b9b4cab6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398275"
---
# <a name="gather4_po_c-sm5---asm"></a>gather4 \_ po \_ c (SM5-ASM)

Si comporta allo stesso modo di [**gather4 \_ po**](gather4-po--sm5---asm-.md), ad eccezione delle operazioni di confronto sui Texel, in modo simile all' [**esempio \_ c**](sample-c--sm4---asm-.md).



| gather4 \_ po \_ c dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcOffset \[ . Swizzle \] , srcResource \[ . Swizzle \] , srcSampler \[ . R \] , srcReferenceValue |
|-------------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                                       | Descrizione                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                                            | \[nell' \] indirizzo del risultato dell'operazione.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[in \] un set di coordinate di trama.<br/>               |
| <span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*<br/>                                 | \[nell' \] offset.<br/>                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[in \] un registro di trama.<br/>                         |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[in \] un registro del campionatore.<br/>                         |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[in \] singolo componente selezionato.<br/>                  |



 

## <a name="remarks"></a>Commenti

Vedere l' [**esempio \_ c**](sample-c--sm4---asm-.md) per informazioni sulla modalità di confronto di *srcReferenceValue* con ogni Texel recuperato. A differenza di **esempio \_ c**, *gather4 \_ po \_ c* restituisce ogni risultato del confronto, anziché filtrarli.

Questa istruzione, come **gather4 \_ po**, funziona solo con le trame 2D. A differenza di [**gather4 \_ c**](gather4-c--sm5---asm-.md), che funziona anche con TextureCubes.

Per i formati con componenti float32, se il valore recuperato è normalizzato, o +-INF, viene usato nell'operazione di confronto non toccata. NaN viene utilizzato nell'operazione di confronto come NaN, ma è possibile modificare la rappresentazione di bit esatta di NaN. Le denormazioni vengono scaricate fino a zero nel confronto. Per TextureCubes, alcune sintesi del quarto Texel mancante devono verificarsi negli angoli, quindi la nozione di restituzione di bit invariati per il Texel sintetizzato non è applicabile.

I formati supportati per **gather4 \_ po \_ c** sono identici a quelli supportati per l' **esempio \_ c**. Si tratta di formati a componente singolo, di conseguenza. R su srcSampler, anziché un swizzle arbitrario.

**gather4 \_ po \_ c** in una risorsa non associata restituisce 0.

Utilizzare questo metodo per il filtro della mappa Shadow.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





