---
title: deriv_rtx_coarse (sm5 - asm)
description: Calcola la frequenza di modifica dei componenti. | deriv_rtx_coarse (sm5 - asm)
ms.assetid: 57743BB2-251C-4EA7-BDA9-70B2ECEE3B3F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50066fe58c3d0a0cdd903de9fbb479a8fbab2c3a20c622ebca138c0937aaf0dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986641"
---
# <a name="deriv_rtx_coarse-sm5---asm"></a>deriv \_ rtx \_ coarse (sm5 - asm)

Calcola la frequenza di modifica dei componenti.



| deriv \_ rtx \_ coarse \[ \_ sat \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swizzle \] , |
|----------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo dei risultati dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Componenti dell'operazione.<br/>             |



 

## <a name="remarks"></a>Commenti

Questa istruzione calcola la frequenza di modifica del contenuto di ogni componente float32 di *src0* (post-swizzle), in relazione alla direzione x RenderTarget (rtx) o RenderTarget y (vedere [deriv \_ rty \_ coarse).](deriv-rty-coarse--sm5---asm-.md) Viene calcolata una sola coppia derivata x,y per ogni stamp di pixel 2x2.

I dati nella chiamata pixel shader corrente possono partecipare o meno al calcolo del derivato richiesto, perché il derivato verrà calcolato una sola volta per quad 2x2. Ad esempio, il derivato x potrebbe essere un delta dalla riga superiore di pixel e la direzione y[ \_ (derivazione rty grosso \_ modo)](deriv-rty-coarse--sm5---asm-.md)potrebbe essere un delta dalla colonna sinistra di pixel. Il calcolo esatto è a livello del fornitore dell'hardware. Non è inoltre disponibile alcuna specifica che detta come i quad 2x2 verranno allineati o affiancati su una primitiva.

I derivati vengono calcolati a livello grossolano, una volta per quad da 2x2 pixel. Questa istruzione [e derivazione \_ rty \_ coarse](deriv-rty-coarse--sm5---asm-.md) sono alternative a [deriv \_ rtx \_ fine](deriv-rtx-fine--sm5---asm-.md) e [deriv \_ rty \_ fine](deriv-rty-fine--sm5---asm-.md). Queste istruzioni derivate grossole e fine sono una sostituzione di \_ \_ **deriv \_ rtxderiv \_ rty** dai modelli di shader precedenti.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     |         |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

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

 

 





