---
title: SinCos (SM4-ASM)
description: Sin (componente-Wise) e cos (THETA) per Theta in radianti.
ms.assetid: 81FDEC8F-2C1C-4C60-A6DA-699C798F8316
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2dd8fc3b011758f071cdcd273e34eb8a7f6421f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104992992"
---
# <a name="sincos-sm4---asm"></a>SinCos (SM4-ASM)

Sin (componente-Wise) e cos (THETA) per Theta in radianti.



| SinCos \[ \_ Sat \] destSIN \[ . mask \] , destCOS \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\] |
|------------------------------------------------------------------------------------|



 



| Elemento                                                                                               | Descrizione                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*<br/> | \[nell' \] indirizzo di sin (*src0*) calcolato per ogni componente.<br/> |
| <span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*<br/> | \[nell' \] indirizzo di cos (*src0*), calcolato per componente.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                    | \[nei \] componenti per i quali calcolare sin e cos.<br/>    |



 

## <a name="remarks"></a>Commenti

Se il risultato non è necessario, è possibile specificare *destSIN* e *destCOS* come null anziché specificare un registro.

I valori theta possono essere qualsiasi valore a virgola mobile IEEE a 32 bit.

L'errore assoluto massimo è 0,0008 nell'intervallo da-100 \* pi a + 100 \* pi.

Nella tabella seguente vengono illustrati i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri.

F indica un numero reale finito.



|             |          |              |             |        |        |             |              |          |         |
|-------------|----------|--------------|-------------|--------|--------|-------------|--------------|----------|---------|
| **src**     | **-INF** | **-F**       | **-denorm** | **-0** | **+0** | **+ denorm** | **+ F**       | **+ INF** | **NaN** |
| **destSIN** | NaN      | \[da-1 a + 1\] | -0          | -0     | +0     | +0          | \[da-1 a + 1\] | NaN      | NaN     |
| **destCOS** | NaN      | \[da-1 a + 1\] | +1          | +1     | +1     | +1          | \[da-1 a + 1\] | NaN      | NaN     |



 

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





