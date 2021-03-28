---
title: drcp (SM5-ASM)
description: Calcola un reciproco a precisione doppia a livello di componente.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b678f4e8b3464817215de9132298fdde1f6feec
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335551"
---
# <a name="drcp-sm5---asm"></a>drcp (SM5-ASM)

Calcola un reciproco a precisione doppia a livello di componente.



| RCP \[ \_ Sat \] dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\] |
|------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nell' \] indirizzo dei risultati<br/> *dest*  =  **1,0**  /  *src0*. Il valore del risultato deve essere accurato per 1,0 ULP rispetto<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nel \] numero da cui assumere il reciproco.<br/>                                                                         |



 

## <a name="remarks"></a>Commenti

L'istruzione DRCP viene generata dal compilatore HLSL solo quando viene chiamata in modo esplicito tramite l'oggetto intrinseco RCP (), quando viene usato un valore Double come argomento. L'accuratezza di questa istruzione deve essere 1,0 ULP rispetto.

Gli shader che usano questa istruzione verranno contrassegnati con un flag shader che ne causerà la mancata associazione a meno che non vengano soddisfatte tutte le condizioni seguenti.

-   Il sistema supporta DirectX 11,1.
-   Il sistema include un driver WDDM 1,2.
-   Il driver segnala il supporto per questa istruzione tramite le **\_ \_ Opzioni d3d11 dei dati della funzionalità d3d11 \_ \_ . ExtendedDoublesShaderInstructions** impostato su **true**.

Nella tabella seguente vengono illustrati i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri, presupponendo che non si verifichino overflow o underflow.

In questa tabella F indica un numero reale finito.



|               |          |        |        |        |        |          |         |
|---------------|----------|--------|--------|--------|--------|----------|---------|
| **src**->  | **-INF** | **-F** | **-0** | **+0** | **+ F** | **+ INF** | **NaN** |
| **dest**-> | -0       | -F     | -inf   | +inf   | + F     | +0       | NaN     |



 

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

 

 





