---
title: div (sm4 - asm)
description: Divisione per componente.
ms.assetid: B086F069-8F43-4746-A6A5-8F4462212648
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d406c5e61b4615990b445abe169619227d22124c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999098"
---
# <a name="div-sm4---asm"></a>div (sm4 - asm)

Divisione per componente.



| div \[ \_ sat \] dest \[ \] .mask, \[ - \] src0 \[ \_ abs \] \[ .swizzle \] \[ - \] src1 \[ \_ abs \] \[ .swizzle\] |
|-------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                    |
|-----------------------------------------------------------------|------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Risultato dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Dividendo.<br/>                |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Divisore.<br/>                 |



 

## <a name="remarks"></a>Commenti

Nella tabella seguente vengono illustrati i risultati ottenuti durante l'esecuzione dell'istruzione con diverse classi di numeri, presupponendo che non si verifichi alcun overflow o underflow.

Si notino le due implementazioni consentite di divide: a/b e \* a (1/b).

Un risultato è che esistono eccezioni alla tabella seguente per valori denominatori di grandi dimensioni (maggiore di 8,5070592e+37), dove 1/denominatore è un nome. Poiché le implementazioni possono eseguire la divisione come (1/b), invece di a/b direttamente e 1/b valore elevato è un denorm che potrebbe essere scaricato, alcuni casi nella tabella produrrebbe risultati \* \[ \] diversi. Ad esempio, il valore (+/-)INF/ (+/-) \[ > 8,5070592e+37 può produrre NaN in alcune implementazioni, ma \] (+/-) in altre implementazioni

In questa tabella F indica un numero finito-reale.



| **src0 src1 ->** | **-inf** | **-F**     | **-denorm** | **-0** | **+0** | **+denorm** | **+F**     | **+inf** | **Nan** |
|---------------------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| **-inf**            | -inf     | -inf       | -inf        | -inf   | -inf   | -inf        | -inf       | NaN      | NaN     |
| **-F**              | -inf     | -F         | src0        | src0   | src0   | src0        | +-F o +-0 | +inf     | NaN     |
| **-denorm**         | -inf     | src1       | -0          | -0     | +0     | +0          | src1       | +inf     | NaN     |
| **-0**              | -inf     | src1       | -0          | -0     | +0     | +0          | src1       | +inf     | NaN     |
| **+0**              | -inf     | src1       | +0          | +0     | +0     | +0          | src1       | +inf     | NaN     |
| **+denorm**         | -inf     | src1       | +0          | +0     | +0     | +0          | src1       | +inf     | NaN     |
| **+F**              | -inf     | +-F o +-0 | src0        | src0   | src0   | src0        | +F         | +inf     | NaN     |
| **+inf**            | NaN      | +inf       | +inf        | +inf   | +inf   | +inf        | +inf       | +inf     | NaN     |
| **NaN**             | NaN      | NaN        | NaN         | NaN    | NaN    | NaN         | NaN        | NaN      | NaN     |



 

Questa istruzione si applica alle fasi di shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

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

 

 





