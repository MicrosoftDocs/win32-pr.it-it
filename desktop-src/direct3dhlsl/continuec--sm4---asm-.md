---
title: continuec (SM4-ASM)
description: Continua l'esecuzione in modo condizionale all'inizio del ciclo corrente.
ms.assetid: 1A5B1951-CE1E-479C-AE0F-FC5FB93E0DE9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d480d8828f8f68af1f6a2ff4f52224041d5241df
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976367"
---
# <a name="continuec-sm4---asm"></a>continuec (SM4-ASM)

Continua l'esecuzione in modo condizionale all'inizio del ciclo corrente.



| continuec { \_ z \|\_NZ} src0. Select ( \_ componente) |
|---------------------------------------------|



 



| Termine                                                            | Descrizione                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nel \] componente rispetto al quale testare la condizione.<br/> |



 

## <a name="remarks"></a>Commenti

**continuec** può essere utilizzato solo all'interno di un [ciclo](loop--sm4---asm-.md) o di [EndLoop](endloop--sm4---asm-.md).

Nell'esempio seguente viene illustrato come utilizzare l'istruzione **continuec** .


```
                loop
                    if_na r0.x
                        break
                    endif
                    continuec_z r1.x  // if all bits of r1.x are zero then
                                      // continue at beginning of loop.
                    ...
                    continuec_nz r3.y // if any bit in r3.y is set then
                                      // continue at beginning of loop.

                    ...
                endloop

```



Il formato del token contiene l'offset dell'istruzione del ciclo corrispondente nello shader come praticità.

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

 

 





