---
title: deriv_rty (sm4 - asm)
description: Equivalente y della destinazione di rendering di deriv \_ rtx.
ms.assetid: F78F2DBD-9428-4F34-85AD-276DF54C52D1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb522076435b525252e8cab40590c649e5cc8af8a83023ebd6cace1695fbb729
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515469"
---
# <a name="deriv_rty-sm4---asm"></a>deriv \_ rty (sm4 - asm)

Equivalente y della destinazione di rendering [di deriv \_ rtx.](deriv-rtx--sm4---asm-.md)



| deriv \_ rty \[ \_ sat \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swizzle \] , |
|--------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo del risultato dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Componente nell'operazione.<br/>             |



 

## <a name="remarks"></a>Commenti

Viene calcolata una sola coppia derivata x,y per ogni stamp di pixel 2x2.

Questa operazione dipende dall'hardware.

Implementazione del rasterizzatore di riferimento per i triangoli:

-   Il pixel shader esegue sempre shader su 2x2 quad di pixel nel passaggio di blocco (anche tramite il controllo di flusso, mascherando i pixel disabilitati).
-   I quad hanno sempre coordinate pixel numerate pari (x e y) per i pixel in alto a sinistra.
-   I pixel fittizi eseguono la primitiva se la primitiva è troppo piccola per riempire un quad 2x2.
-   [deriv \_ rtx](deriv-rtx--sm4---asm-.md) viene calcolato scegliendo prima 2 pixel: il pixel corrente e l'altro pixel con la stessa coordinata y del quad. Il risultato viene quindi calcolato come: *src0*(x pixel dispari) - *src0*(anche x pixel) \[ per componente\]
-   **Il valore \_ di deriv rty** viene calcolato scegliendo prima 2 pixel: il pixel corrente e l'altro pixel con la stessa coordinata x del quad. Il risultato viene quindi calcolato come: *src0*(pixel y dispari) - *src0*(anche y pixel) \[ per componente\]

Questa istruzione si applica alle fasi di shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
|               |                 | x            |



 

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

 

 





