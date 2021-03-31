---
title: firstbit (SM5-ASM)
description: Trova il primo bit impostato in un numero, sia da LSB che da MSB.
ms.assetid: E3066676-5218-470A-944A-7B221E1BF64D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b88fa9291ce64fcc8c94510bd09bed31e7b7f96
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335623"
---
# <a name="firstbit-sm5---asm"></a>firstbit (SM5-ASM)

Trova il primo bit impostato in un numero, sia da LSB che da MSB.



| firstbit { \_ Hi \|\_lo|\_Shi} dest \[ . mask \] , src0 \[ . Swizzle\] |
|-------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nella \] posizione integer del primo bit impostato in *src0* a partire da LSB per FIRSTBIT \_ lo o MSB per firstbit \_ Hi.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nell' \] Integer di input.<br/>                                                                                                  |



 

## <a name="remarks"></a>Commenti

Questa operazione restituisce la posizione integer del primo bit impostato nell'input a 32 bit a partire da LSB per firstbit \_ lo o MSB per firstbit \_ Hi. Ad esempio \_ , firstbit lo in 0x00000001 restituisce 0. firstbit \_ Hi on 0x10000000 restituisce 3.

firstbit \_ Shi (s per Signed) restituisce il primo 0 da MSB se il numero è negativo. in caso contrario, restituisce il primo 1 da MSB.

Tutte le varianti dell'istruzione restituiscono ~ 0 (0xFFFFFFFF nel registro a 32 bit) se non viene trovata alcuna corrispondenza.

Usare questa istruzione per enumerare rapidamente i bit impostati in un bit o trovare la maggiore potenza di 2 in un numero.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="mimimum-shader-model"></a>Modello Shader minimo

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

 

 





