---
title: add (sm4 - asm)
description: Aggiunta di 2 vettori a livello di componente.
ms.assetid: 405A513C-B2DD-43B9-A86D-1D173B084C51
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e34f0a95ad9ee9ae4bdeed317eef133e3773311
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994978"
---
# <a name="add-sm4---asm"></a>add (sm4 - asm)

Aggiunta di 2 vettori a livello di componente.



| add \[ \_ sat \] dest \[ \] .mask, \[ - \] src0 \[ \_ abs \] \[ .swizzle, \] \[ - \] src1 \[ \_ abs \] \[ .swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo del risultato dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Vettore da aggiungere a *src1.*<br/>                |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Vettore da aggiungere a *src0*.<br/>                |



 

## <a name="remarks"></a>Commenti

La tabella seguente mostra i risultati ottenuti durante l'esecuzione dell'istruzione con diverse classi di numeri, presupponendo che non si verifichino overflow o underflow. F indica un numero reale finito.



| **src0 src1->** | **-inf** | **-F**     | **-denorm** | **-0** | **+0** | **denorm** | **+F**     | **+inf** | **NaN** |
|--------------------|----------|------------|-------------|--------|--------|------------|------------|----------|---------|
| **-inf**           | -inf     | -inf       | -inf        | -inf   | -inf   | -inf       | -inf       | NaN      | NaN     |
| **-F**             | -inf     | -F         | src0        | src0   | src0   | src0       | +-F o +-0 | +inf     | NaN     |
| **-denorm**        | -inf     | src1       | -0          | -0     | +0     | +0         | src1       | +inf     | NaN     |
| **-0**             | -inf     | src1       | -0          | -0     | +0     | +0         | src1       | +inf     | NaN     |
| **+0**             | i-inf    | src1       | +0          | +0     | +0     | +0         | src1       | +inf     | NaN     |
| **+denorm**        | -inf     | src1       | +0          | +0     | +0     | +0         | src1       | +inf     | NaN     |
| **+F**             | -inf     | +-F o +-0 | src0        | src0   | src0   | src0       | +F         | +inf     | NaN     |
| **+inf**           | NaN      | +inf       | +inf        | +inf   | +inf   | +inf       | +inf       | +inf     | NaN     |
| **NaN**            | NaN      | NaN        | NaN         | NaN    | NaN    | NaN        | NaN        | NaN      | NaN     |



 

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
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 4 (HLSL DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





