---
title: itof (SM4-ASM)
description: Intero con segno alla conversione a virgola mobile.
ms.assetid: 60652168-25FA-4084-8CC1-73F12984ECED
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f9d262f65801cd2caa0e6432b335ce32fff0d4e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857782"
---
# <a name="itof-sm4---asm"></a>itof (SM4-ASM)

Intero con segno alla conversione a virgola mobile.



| itof dest \[ . mask \] , \[ - \] src0 \[ . Swizzle\] |
|-------------------------------------------|



 



| Elemento                                                            | Descrizione                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] contiene il risultato dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] contiene il valore da convertire.<br/>        |



 

## <a name="remarks"></a>Commenti

Questa istruzione di conversione da Integer a float con segno presuppone che *src0* contenga una tupla con valore intero a 32 bit con segno 4. Dopo l'esecuzione dell'istruzione, *dest* conterrà una tupla a virgola mobile a 4 elementi.

La conversione viene eseguita per ogni componente.

Quando un valore di input di tipo Integer è troppo grande per essere rappresentato esattamente nel formato a virgola mobile, l'arrotondamento alla modalità pari più vicina è fortemente consigliato ma non obbligatorio.

Il modificatore negazioni facoltativo nell'operando di origine accetta il complemento di 2 prima di eseguire un'operazione aritmetica.

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

 

 





