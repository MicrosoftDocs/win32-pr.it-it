---
title: firstbit (sm5 - asm)
description: Trova il primo bit impostato in un numero, da LSB o MSB.
ms.assetid: E3066676-5218-470A-944A-7B221E1BF64D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ea47c8e0674db5dc0349e5d6a8a041fa7d3623e6578eee542edeb1749577d7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511945"
---
# <a name="firstbit-sm5---asm"></a>firstbit (sm5 - asm)

Trova il primo bit impostato in un numero, da LSB o MSB.



| firstbit{ \_ hi\|\_lo\|\_shi} dest \[ .mask \] , src0 \[ .swizzle\] |
|-------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Posizione integer del primo bit impostato in *src0 a* partire dall'LSB per firstbit lo o \_ MSB per firstbit \_ hi.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Numero intero di input.<br/>                                                                                                  |



 

## <a name="remarks"></a>Commenti

Questa operazione restituisce la posizione integer del primo bit impostato nell'input a 32 bit a partire dall'LSB per firstbit lo o MSB per \_ firstbit \_ hi. Ad esempio, firstbit \_ lo in 0x00000001 restituisce 0. firstbit \_ hi on 0x10000000 restituisce 3.

firstbit shi (s per signed) restituisce il primo 0 da MSB se il numero è negativo; in caso contrario, restituisce il primo \_ 1 da MSB.

Tutte le varianti dell'istruzione restituiscono ~0 (0xffffffff nel registro a 32 bit) se non viene trovata alcuna corrispondenza.

Usare questa istruzione per enumerare rapidamente i bit impostati in un campo di bit o trovare la potenza più grande di 2 in un numero.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="mimimum-shader-model"></a>Modello di shader Mimimum

Questa istruzione è supportata nei modelli di shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (HLSL DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





