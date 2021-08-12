---
title: utof (sm4 - asm)
description: Conversione da intero senza segno a virgola mobile.
ms.assetid: 5A52C959-7B4C-4FA1-B29C-BCAF448419F8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edd5e69476c77ee71e25c3e2286ddd53cc01027197b7ad9d83ed723438a93882
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118283009"
---
# <a name="utof-sm4---asm"></a>utof (sm4 - asm)

Conversione da intero senza segno a virgola mobile.



| utof dest \[ .mask \] , src0 \[ .swizzle\] |
|--------------------------------------|



 



| Elemento                                                            | Descrizione                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo del risultato dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Componenti da convertire.<br/>                  |



 

## <a name="remarks"></a>Commenti

*src0* deve contenere un intero senza segno a 4 tuple a 4 bit. Dopo l'esecuzione dell'istruzione, *dest* conterrà una tupla a 4 virgola mobile. La conversione viene eseguita per componente.

Quando un valore di input integer è troppo grande per essere rappresentato esattamente nel formato a virgola mobile, arrotondare alla modalità pari più vicina.

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

 

 





