---
title: deriv_rtx (sm4 - asm)
description: Frequenza di modifica del contenuto di ogni componente float32 di src0 (post-swizzle), in relazione alla direzione x RenderTarget (rtx) o RenderTarget y.
ms.assetid: 2438DB36-C348-4854-AE1B-EC3C890B0B42
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7a9697372964135e5ecb3cb5e916b0509a6a6a860ff8fa01ea0daeb1b8be4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986651"
---
# <a name="deriv_rtx-sm4---asm"></a>deriv \_ rtx (sm4 - asm)

Frequenza di modifica del contenuto di ogni componente float32 di *src0* (post-scorrimento), per quanto riguarda la direzione x RenderTarget (rtx) o RenderTarget y.



| deriv \_ rtx \[ \_ sat \] dest \[ \] .mask, \[ - \] src0 \[ \_ abs \] \[ .swizzle \] , |
|--------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo del risultato dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Componente nell'operazione.<br/>             |



 

## <a name="remarks"></a>Commenti

Viene calcolata una sola coppia derivata x,y per ogni timbro 2x2 di pixel.

Questa operazione dipende dall'hardware.

Implementazione del rasterizzatore di riferimento per i triangoli:

-   Pixel Shader esegue sempre Shader su 2x2 quad di pixel in lockstep (anche tramite il controllo di flusso, mascherando i pixel disabilitati).
-   I quad hanno sempre coordinate pixel pari numerate (x e y) per i pixel in alto a sinistra.
-   I pixel fittizi eseguono la primitiva se la primitiva è troppo piccola per riempire un quad 2x2.
-   **deriv \_ rtx** viene calcolato scegliendo prima 2 pixel: il pixel corrente e l'altro pixel con la stessa coordinata y del quad. Il risultato viene quindi calcolato come: *src0*(x pixel dispari) - *src0*(anche x pixel) \[ per componente\]
-   [La \_ derivazione viene](deriv-rty--sm4---asm-.md) calcolata scegliendo prima 2 pixel: il pixel corrente e l'altro pixel con la stessa coordinata x del quad. Il risultato viene quindi calcolato come: *src0*(pixel y dispari) - *src0*(pixel y pari) \[ per componente\]

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Shader Model 4 Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





