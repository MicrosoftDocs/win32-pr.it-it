---
title: deriv_rtx_fine (SM5-ASM)
description: Calcola la frequenza di modifica dei componenti. | deriv_rtx_fine (SM5-ASM)
ms.assetid: 5752C85B-2965-489C-BF27-968FAF5EAA52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73061e3220704cf2c19e28b4d6d434fda43fb941
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995608"
---
# <a name="deriv_rtx_fine-sm5---asm"></a>derivare \_ RTX \_ fine (SM5-ASM)

Calcola la frequenza di modifica dei componenti.



| derivare \_ RTX \_ fine \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , |
|--------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nell' \] indirizzo dei risultati dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nei \] componenti dell'operazione.<br/>             |



 

## <a name="remarks"></a>Commenti

Questa istruzione calcola la frequenza di modifica del contenuto di ogni componente float32 di *src0* (post-swizzle), per quanto riguarda la direzione renderTarget x (RTX) o la direzione renderTarget y (vedere [derivate \_ valore \_ fine](deriv-rty-fine--sm5---asm-.md)). Ogni pixel nell'indicatore 2x2 ottiene una coppia univoca di calcoli derivati x/y

I dati nella chiamata di pixel shader corrente partecipano sempre al calcolo della derivata richiesta. Nel quadrato 2x2 pixel, il pixel corrente rientra in, il derivato x è il Delta della riga di 2 pixel, incluso il pixel corrente. La derivata y è il Delta della colonna di 2 pixel, incluso il pixel corrente. Non esiste alcuna specifica che impone il modo in cui i quad di 2x2 verranno allineati o affiancati su una primitiva.

I derivati vengono calcolati a un livello fine (calcolo univoco della coppia di derivati x/y per ogni pixel in un quad 2x2). Questa istruzione e [derivano \_ valore \_ fine](deriv-rty-fine--sm5---asm-.md) sono alternative per [derivare \_ RTX \_ grossolane](deriv-rtx-coarse--sm5---asm-.md) e [derivare \_ valore \_ grossolane](deriv-rty-coarse--sm5---asm-.md). Queste \_ \_ istruzioni derivate grossolane e fine rappresentano una sostituzione per **derivare \_ RTX** . queste istruzioni derivate \_ grossolane e \_ belle sono una sostituzione per derivare **\_ RTX** e **derivare \_ valore** dai modelli shader precedenti.

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

 

 





