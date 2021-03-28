---
title: if (SM4-ASM)
description: Ramo basato sul risultato logico o.
ms.assetid: 9F4CF9E0-4D9D-4300-B432-432C560F34BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 653c84be0d30a036bf93d852268e44bcca08bbcb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104992965"
---
# <a name="if-sm4---asm"></a>if (SM4-ASM)

Ramo basato sul risultato logico o.



| Se { \_ z \|\_NZ} src0. Select ( \_ componente) |
|--------------------------------------|



 



| Elemento                                                            | Descrizione                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] contiene il componente su cui eseguire il test della condizione.<br/> |



 

## <a name="remarks"></a>Commenti

Il formato del token contiene l'offset dell'istruzione endif corrispondente nello shader per praticità.

Nell'esempio seguente viene illustrato come utilizzare questa istruzione.

``` syntax
                if_z r0.x // if all bits in r0.x are zero
                   ...
                else // (optional)
                   ...
                endif
                if_nz r1.x // if any bit in r0.x is nonzero
                   ...
                else // (optional)
                   ...
                endif
```

### <a name="restrictions"></a>Restrizioni

-   Gli operandi di origine (se 4 vettori componenti) devono usare un singolo selettore di componenti.
-   Il registro a 32 bit fornito da *src0* viene testato a livello di bit. Se un bit è diverso da zero, **se \_ z** sarà true. Se tutti i bit sono zero, **se \_ NZ** sarà true.
-   I blocchi di controllo di flusso possono annidare fino a 64 di profondità per subroutine (e Main). Il compilatore HLSL non genererà subroutine che superano questo limite. Il comportamento delle istruzioni del flusso di controllo oltre 64 livelli di profondità (per subroutine) non è definito.

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

 

 





