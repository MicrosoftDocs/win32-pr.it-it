---
title: dfma (sm5 - asm)
description: Esegue un'aggiunta a moltiplicazione fusa.
ms.assetid: 5BE96CDB-1756-4EBE-B4CC-69EFF098A4F1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84952ed594ba8541223df072fa59550aded581e5517dee3d6f4168b7661a87aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068391"
---
# <a name="dfma-sm5---asm"></a>dfma (sm5 - asm)

Esegue un'aggiunta a moltiplicazione fusa.



| dfma \[ \_ sat \] dest \[ \] .mask, \[ - \] src0 \[ \_ abs \] \[ .swizzle, \] \[ - \] src1 \[ \_ abs \] \[ .swizzle, \] \[ - \] src2 \[ \_ abs \] \[ .swizzle\] |
|----------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo del risultato dell'operazione. Il valore del risultato deve essere preciso a 0,5 ULP.<br/> *dest*  =  *src0* \* *src1*  +  *src2*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] I componenti da moltiplicare con *src1*.<br/>                                                                                                 |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] I componenti da moltiplicare con *src0*.<br/>                                                                                                 |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[in \] Componenti da aggiungere a *src0* \* *src1*.<br/>                                                                                               |



 

## <a name="remarks"></a>Commenti

Gli shader che usano questa istruzione verranno contrassegnati con un flag shader che ne causerà l'esito negativo, a meno che non vengano soddisfatte tutte le condizioni seguenti.

-   Il sistema supporta DirectX 11.1.
-   Il sistema include un driver WDDM 1.2.
-   Il driver segnala il supporto per questa istruzione **tramite D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS. ExtendedDoublesShaderInstructions** impostato su **TRUE.**

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



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

 

 





