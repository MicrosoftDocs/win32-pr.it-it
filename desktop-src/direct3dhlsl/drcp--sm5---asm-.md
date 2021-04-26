---
title: drcp (sm5 - asm)
description: Calcola un reciproco a precisione doppia per componente.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 770159f5007b08f5482ba8b58634b44e7f3e6ef0
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998338"
---
# <a name="drcp-sm5---asm"></a>drcp (sm5 - asm)

Calcola un reciproco a precisione doppia per componente.



| rcp \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle\] |
|------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] L'indirizzo dei risultati<br/> *dest*  =  **1.0**  /  *src0*. Il valore del risultato deve essere accurato a 1,0 ULP<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Numero di cui prendere il reciproco.<br/>                                                                         |



 

## <a name="remarks"></a>Commenti

L'istruzione DRCP viene generata dal compilatore HLSL solo quando viene chiamata in modo esplicito tramite la funzione intrinseca rcp(), quando come argomento viene usato un valore double. L'accuratezza di questa istruzione deve essere 1,0 ULP.

Gli shader che usano questa istruzione verranno contrassegnati con un flag shader che ne causerà l'associazione a meno che non vengano soddisfatte tutte le condizioni seguenti.

-   Il sistema supporta DirectX 11.1.
-   Il sistema include un driver WDDM 1.2.
-   Il driver segnala il supporto per questa istruzione **tramite D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS. ExtendedDoublesShaderInstructions** impostato su **TRUE.**

Nella tabella seguente vengono illustrati i risultati ottenuti durante l'esecuzione dell'istruzione con diverse classi di numeri, presupponendo che non si verifichi alcun overflow o underflow.

In questa tabella F indica un numero finito-reale.



| **Src**->  | **-inf** | **-F** | **-0** | **+0** | **+F** | **+inf** | **NaN** |
|---------------|----------|--------|--------|--------|--------|----------|---------|
| **Dest**-> | -0       | -F     | -inf   | +inf   | +F     | +0       | NaN     |



 

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
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (HLSL DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





