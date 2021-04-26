---
title: log (sm4 - asm)
description: Log per componente in base 2.
ms.assetid: 6D28864A-C2BA-44AF-9E78-7C2B34F5E462
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88e4b89b4dcc085cf4fd4fda762d96fb71271af2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998318"
---
# <a name="log-sm4---asm"></a>log (sm4 - asm)

Log per componente in base 2.



| log \[ \_ sat \] dest \[ \] .mask, \[ - \] src0 \[ \_ abs \] \[ .swizzle |
|----------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                                |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo del risultato dell'operazione.<br/> dest = log2(src0)<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Valore per l'operazione.<br/>                                             |



 

## <a name="remarks"></a>Commenti

### <a name="restrictions"></a>Restrizioni

-   Segue la teoria dei limiti.
-   Tolleranza di errore: se *src0* è \[ 0.5..2, l'errore absolue non deve essere \] maggiore di 2-21. Se *src0* è (0..0.5) o (2..+INF), l'errore relativo non deve essere \] maggiore di 2-21.

Nella tabella seguente vengono illustrati i risultati ottenuti durante l'esecuzione dell'istruzione con diverse classi di numeri, presupponendo che non si verifichi alcun overflow o underflow. F indica un numero finito-reale.



| **src**  | **-inf** | **-F** | **-denorm** | **-0** | **+0** | **+denorm** | **+F** | **+inf** | **NaN** |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| **Dest** | NaN      | NaN    | -inf        | -inf   | -inf   | -inf        | F      | +inf     | NaN     |



 

Questa istruzione si applica alle fasi di shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

### <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 4 (HLSL DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





