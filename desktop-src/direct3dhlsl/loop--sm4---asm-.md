---
title: loop (SM4-ASM)
description: Specifica un ciclo che esegue l'iterazione fino a quando non viene rilevata un'istruzione break.
ms.assetid: 0BEFADF4-036E-4FDA-9681-10965D6BA9FC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 243bdf3b370d3505d787451162c22340acef3a45
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993104"
---
# <a name="loop-sm4---asm"></a>loop (SM4-ASM)

Specifica un ciclo che esegue l'iterazione fino a quando non viene rilevata un'istruzione break.



| loop |
|------|



 

## <a name="remarks"></a>Commenti

il **ciclo** può scorrere a tempo indefinito, sebbene l'esecuzione complessiva dello shader possa essere forzata per terminare dopo l'esecuzione di un certo numero di istruzioni.

I blocchi di controllo di flusso possono annidare fino a 64 di profondità per subroutine e Main. Il compilatore HLSL non genererà subroutine che superano questo limite. Il comportamento delle istruzioni del flusso di controllo oltre 64 livelli di profondità per subroutine non è definito.

Il formato del token contiene l'offset dell'istruzione [EndLoop](endloop--sm4---asm-.md) corrispondente nello shader per praticità.

Nell'esempio seguente viene illustrato come utilizzare l'istruzione Loop.

``` syntax
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




