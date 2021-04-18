---
title: deriv_rtx_coarse (SM5-ASM)
description: Calcola la frequenza di modifica dei componenti. | deriv_rtx_coarse (SM5-ASM)
ms.assetid: 57743BB2-251C-4EA7-BDA9-70B2ECEE3B3F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2355b6db6aef9e85959d6359053fea76b48af0a5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995397"
---
# <a name="deriv_rtx_coarse-sm5---asm"></a>derivate \_ RTX \_ grossolane (SM5-ASM)

Calcola la frequenza di modifica dei componenti.



| derivate \_ RTX a \_ grosse \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , |
|----------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nell' \] indirizzo dei risultati dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nei \] componenti dell'operazione.<br/>             |



 

## <a name="remarks"></a>Commenti

Questa istruzione calcola la frequenza di modifica del contenuto di ogni componente float32 di *src0* (post-swizzle), per quanto riguarda la direzione renderTarget x (RTX) o la direzione renderTarget y (vedere [derivate \_ valore \_ grossolane](deriv-rty-coarse--sm5---asm-.md)). Viene calcolata solo una singola coppia derivata x e y per ogni timbro 2x2 di pixel.

I dati nella chiamata di pixel shader corrente possono o non possono partecipare al calcolo del derivato richiesto, perché il derivato verrà calcolato solo una volta per ogni Quad 2x2. Ad esempio, il derivato x può essere un Delta dalla prima riga di pixel e la direzione y ([derivate \_ valore \_ grossolane](deriv-rty-coarse--sm5---asm-.md)) potrebbe essere un Delta dalla colonna di sinistra di pixel. Il calcolo esatto spetta al fornitore dell'hardware. Non esiste inoltre alcuna specifica che impone il modo in cui i quadrupli 2x2 verranno allineati o affiancati su una primitiva.

I derivati vengono calcolati a un livello grossolano, una volta per ogni quad di 2x2 pixel. Questa istruzione e [derivano \_ valore \_ grossolane](deriv-rty-coarse--sm5---asm-.md) sono alternative alla [derivazione di \_ RTX \_ fine](deriv-rtx-fine--sm5---asm-.md) e [derivano \_ valore \_ fine](deriv-rty-fine--sm5---asm-.md). Queste \_ \_ istruzioni derivate grossolane e fine rappresentano una sostituzione per **derivare \_ rtxderiv \_ valore** dai modelli shader precedenti.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     |         |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

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

 

 





