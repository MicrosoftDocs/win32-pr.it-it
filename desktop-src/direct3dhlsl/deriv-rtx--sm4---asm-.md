---
title: deriv_rtx (SM4-ASM)
description: Frequenza di modifica del contenuto di ogni componente float32 di src0 (post-swizzle), rispetto alla direzione RenderTarget x (RTX) o RenderTarget y.
ms.assetid: 2438DB36-C348-4854-AE1B-EC3C890B0B42
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d4543805c02cf70d9c6b7856461c427788f616
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398206"
---
# <a name="deriv_rtx-sm4---asm"></a>derivare \_ RTX (SM4-ASM)

Frequenza di modifica del contenuto di ogni componente float32 di *src0* (post-swizzle), rispetto alla direzione renderTarget x (RTX) o renderTarget y.



| derivare \_ RTX \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , |
|--------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nell' \] indirizzo del risultato dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nel \] componente dell'operazione.<br/>             |



 

## <a name="remarks"></a>Commenti

Viene calcolata solo una singola coppia derivata x e y per ogni timbro 2x2 di pixel.

Questa operazione dipende dall'hardware.

Implementazione dell'rasterizzazione dei riferimenti per i triangoli:

-   Pixel shader esegue sempre lo shader su 2x2 quad di pixel in contemporanea (anche attraverso il controllo di flusso, mascherando i pixel disabilitati).
-   I quad hanno sempre le coordinate dei pixel numerate (entrambe x e y) per il pixel superiore sinistro.
-   I pixel fittizi vengono spenti primitivi se la primitiva è troppo piccola per riempire un quad 2x2.
-   la **derivazione \_ RTX** viene calcolata scegliendo 2 pixel: il pixel corrente e l'altro pixel con la stessa coordinata y del quad. Il risultato viene quindi calcolato come: *src0*(Odd x pixel)- *src0*(anche x pixel) \[ per componente\]
-   la [derivazione \_ valore](deriv-rty--sm4---asm-.md) viene calcolata scegliendo 2 pixel: il pixel corrente e l'altro pixel con la stessa coordinata x del quad. Il risultato viene quindi calcolato come: *src0*(pixel dispari y)- *src0*(anche pixel y) \[ per componente\]

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
|               |                 | x            |



 

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

 

 





