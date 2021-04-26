---
title: ddiv (sm5 - asm)
description: Calcola una divisione a precisione doppia per componente.
ms.assetid: 0A67FC35-7F2F-4258-83CE-1CA398E57952
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fc039b222b28a5fb1217d23c78470aff1739f7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999158"
---
# <a name="ddiv-sm5---asm"></a>ddiv (sm5 - asm)

Calcola una divisione a precisione doppia per componente.



| ddiv \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle \] \[ - \] src1 \[ \_ abs \] \[ .swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                   |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Risultato dell'operazione. Il valore del risultato deve essere preciso a 0,5 ULP. <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Dividendo.<br/>                                                               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Divisore.<br/>                                                                |



 

## <a name="remarks"></a>Commenti

L'istruzione DDIV verrà generata dal compilatore HLSL ogni volta che l'operatore di divisione viene usato con valori double. L'accuratezza di questa istruzione deve essere 0,5 ULP.

Gli shader che usano questa istruzione verranno contrassegnati con un flag shader che ne causerà l'associazione a meno che non vengano soddisfatte tutte le condizioni seguenti.

-   Il sistema supporta DirectX 11.1.
-   Il sistema include un driver WDDM 1.2.
-   Il driver segnala il supporto per questa istruzione **tramite D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS. ExtendedDoublesShaderInstructions** impostato su **TRUE.**

Nella tabella seguente vengono illustrati i risultati relativi all'esecuzione dell'istruzione con diverse classi di numeri, presupponendo che non si verifichi alcun overflow o underflow.

In questa tabella F indica un numero finito-reale.



| **src0 src1 ->** | **-inf** | **-F** | **-1.0** | **-0** | **+0** | **+1.0** | **+F** | **+inf** | **NaN** |
|---------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| **-inf**            | NaN      | +inf   | +inf     | +inf   | -inf   | -inf     | -inf   | NaN      | NaN     |
| **-F**              | +0       | +F     | -src0    | +inf   | -inf   | src0     | -F     | -0       | NaN     |
| **-0**              | +0       | +0     | +0       | NaN    | NaN    | -0       | -0     | -0       | NaN     |
| **+0**              | -0       | -0     | -0       | NaN    | NaN    | +0       | +0     | +0       | NaN     |
| **+F**              | -0       | -F     | -src0    | -inf   | +inf   | src0     | +F     | +0       | NaN     |
| **+inf**            | NaN      | -inf   | -inf     | -inf   | +inf   | +inf     | +inf   | NaN      | NaN     |
| **NaN**             | NaN      | NaN    | NaN      | NaN    | NaN    | NaN      | NaN    | NaN      | NaN     |



 

Questa istruzione si applica alle fasi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa istruzione è supportata nei modelli di shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





