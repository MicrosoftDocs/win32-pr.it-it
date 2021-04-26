---
title: frc (sm4 - asm)
description: Componente per componente, estrazione del componente frazionario.
ms.assetid: 17C88BCE-7F2F-446C-9BB4-860098B5E42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f59b747f38fb970b92b5e48610873efe781d63d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993918"
---
# <a name="frc-sm4---asm"></a>frc (sm4 - asm)

Componente per componente, estrazione del componente frazionario.



| frc \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle\] |
|-------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo del risultato dell'operazione.<br/> *dest*  =  *src0*  -  [round \_ ni](round-ni--sm4---asm-.md)(*src0*)<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Componente nell'operazione.<br/>                                                                                        |



 

## <a name="remarks"></a>Commenti

La tabella seguente mostra i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri.



| **src**  | **-inf** | **-F**     | **-denorm** | **-0** | **+0** | **+denorm** | **+F**     | **+inf** | **NaN** |
|----------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| **Dest** | NaN      | \[+0 a 1) | +0          | +0     | +0     | +0          | \[+0 a 1) | NaN      | NaN     |



 

F indica un numero finito reale.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Shader Model 4 Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





