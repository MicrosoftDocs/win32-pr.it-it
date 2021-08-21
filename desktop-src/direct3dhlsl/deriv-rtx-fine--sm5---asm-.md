---
title: deriv_rtx_fine (sm5 - asm)
description: Calcola la frequenza di modifica dei componenti. | deriv_rtx_fine (sm5 - asm)
ms.assetid: 5752C85B-2965-489C-BF27-968FAF5EAA52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6666750be76d673ddc6c5f0d66d23131096812c93b71be52eb7e0f6ebb403ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792656"
---
# <a name="deriv_rtx_fine-sm5---asm"></a>deriv \_ rtx \_ fine (sm5 - asm)

Calcola la frequenza di modifica dei componenti.



| deriv \_ rtx \_ fine sat \[ \_ \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swizzle \] , |
|--------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo dei risultati dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Componenti dell'operazione.<br/>             |



 

## <a name="remarks"></a>Commenti

Questa istruzione calcola la frequenza di modifica del contenuto di ogni componente float32 di *src0* (post-swizzle), in relazione alla direzione x RenderTarget (rtx) o RenderTarget y (vedere [deriv \_ rty \_ fine).](deriv-rty-fine--sm5---asm-.md) Ogni pixel nello stamp 2x2 ottiene una coppia univoca di calcoli derivati x/y

I dati nella chiamata pixel shader corrente partecipano sempre al calcolo del derivato richiesto. Nel quad da 2x2 pixel il pixel corrente rientra, il derivato x è il delta della riga di 2 pixel incluso il pixel corrente. Il derivato y è il delta della colonna di 2 pixel incluso il pixel corrente. Non esiste alcuna specifica che detta come i quad da 2x2 verranno allineati o affiancati su una primitiva.

I derivati vengono calcolati a un livello fine (calcolo univoco della coppia derivata x/y per ogni pixel in un quad 2x2). Questa istruzione e la funzione di derivazione [ \_ rty \_ fine](deriv-rty-fine--sm5---asm-.md) sono alternative a [deriv \_ rtx \_ coarse](deriv-rtx-coarse--sm5---asm-.md) e [deriv \_ rty \_ coarse](deriv-rty-coarse--sm5---asm-.md). Queste istruzioni derivate grossole e fine sono una sostituzione di \_ \_ **deriv \_ rtx** Queste istruzioni derivate grossole e fine sono una sostituzione per la derivazione \_ \_ **\_ rtx** **\_** e la derivazione rty dai modelli shader precedenti.

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

 

 





