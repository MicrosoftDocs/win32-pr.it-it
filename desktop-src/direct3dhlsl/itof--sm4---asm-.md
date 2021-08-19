---
title: itof (sm4 - asm)
description: Conversione da intero con segno a virgola mobile.
ms.assetid: 60652168-25FA-4084-8CC1-73F12984ECED
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f473b5cc9664ee1c9acab88381bc9de6a5b4897fac3899923c6bb20c22bba7fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986481"
---
# <a name="itof-sm4---asm"></a>itof (sm4 - asm)

Conversione da intero con segno a virgola mobile.



| itof dest \[ .mask \] , \[ - \] src0 \[ .swizzle\] |
|-------------------------------------------|



 



| Elemento                                                            | Descrizione                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Contiene il risultato dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Contiene il valore da convertire.<br/>        |



 

## <a name="remarks"></a>Commenti

Questa istruzione di conversione da intero a float con segno presuppone che *src0* contenga una tupla integer a 4 bit con segno. Dopo l'esecuzione dell'istruzione, *dest* conterrà una tupla a 4 virgola mobile.

La conversione viene eseguita per componente.

Quando un valore di input integer è troppo grande per essere rappresentato esattamente nel formato a virgola mobile, l'arrotondamento alla modalità pari più vicina è fortemente consigliato ma non obbligatorio.

Il modificatore di negazione facoltativo nell'operando di origine accetta il complemento 2 prima di eseguire un'operazione aritmetica.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 4 (HLSL DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





