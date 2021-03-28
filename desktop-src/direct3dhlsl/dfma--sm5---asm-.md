---
title: DFMA (SM5-ASM)
description: Esegue un'aggiunta di moltiplicazione con fusione.
ms.assetid: 5BE96CDB-1756-4EBE-B4CC-69EFF098A4F1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e6cafc71dbc7d57655524b1b87c9c5b9ba20f3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335503"
---
# <a name="dfma-sm5---asm"></a>DFMA (SM5-ASM)

Esegue un'aggiunta di moltiplicazione con fusione.



| DFMA \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . Swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . Swizzle\] |
|----------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nell' \] indirizzo del risultato dell'operazione. Il valore del risultato deve essere accurato per 0,5 ULP rispetto.<br/> *dest*  =  *src0* \* *src1*  +  *src2*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nei \] componenti da moltiplicare con *src1*.<br/>                                                                                                 |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nei \] componenti da moltiplicare con *src0*.<br/>                                                                                                 |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[nei \] componenti da aggiungere a *src0* \* *src1*.<br/>                                                                                               |



 

## <a name="remarks"></a>Commenti

Gli shader che usano questa istruzione verranno contrassegnati con un flag shader che ne causerà la mancata associazione a meno che non vengano soddisfatte tutte le condizioni seguenti.

-   Il sistema supporta DirectX 11,1.
-   Il sistema include un driver WDDM 1,2.
-   Il driver segnala il supporto per questa istruzione tramite le **\_ \_ Opzioni d3d11 dei dati della funzionalità d3d11 \_ \_ . ExtendedDoublesShaderInstructions** impostato su **true**.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 





