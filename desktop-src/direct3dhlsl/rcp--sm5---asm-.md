---
title: rcp (sm5 - asm)
description: Reciproco a livello di componente.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa37499a981bae86333b071c2e96a37ccb8ac1a6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998248"
---
# <a name="rcp-sm5---asm"></a>rcp (sm5 - asm)

Reciproco a livello di componente.



| rcp \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle\] |
|------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                         |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo dei risultati<br/> *dest*  =  **1.0f**  /  *src0*.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Numero di cui prendere il reciproco.<br/>                             |



 

## <a name="remarks"></a>Commenti

Usare questa istruzione per il reciproco a precisione ridotta, indipendentemente dai requisiti rigorosi per la divisione.

L'errore relativo massimo è 2-21. (La tolleranza di errore corrisponde solo a rsq)

La tabella seguente mostra i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri.



| *src*  | **-inf** | **-F** | **-denorm** | **-0** | **+0** | **+denorm** | **+F** | **+inf** | **NaN** |
|--------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| *Dest* | -0       | -F     | -inf        | -inf   | +inf   | +inf        | +F     | +0       | NaN     |



 

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

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

 

 





