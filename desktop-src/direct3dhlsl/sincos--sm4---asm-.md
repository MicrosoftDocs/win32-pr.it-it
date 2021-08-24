---
title: sincos (sm4 - asm)
description: Sin per componente (theta) e cos(theta) per theta in radianti.
ms.assetid: 81FDEC8F-2C1C-4C60-A6DA-699C798F8316
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e0b8ba0f6a8ed5076b8918d23d42653fe661e334101257d19d3ad23ab27a60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788591"
---
# <a name="sincos-sm4---asm"></a>sincos (sm4 - asm)

Sin per componente (theta) e cos(theta) per theta in radianti.



| sincos \[ \_ sat \] destSIN \[ .mask \] , destCOS \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swizzle\] |
|------------------------------------------------------------------------------------|



 



| Elemento                                                                                               | Descrizione                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*<br/> | \[in \] L'indirizzo di sin(*src0*), calcolato per componente.<br/> |
| <span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*<br/> | \[in \] Indirizzo di cos(*src0*), calcolato per componente.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                    | \[in \] Componenti per cui calcolare sin e cos.<br/>    |



 

## <a name="remarks"></a>Commenti

Se il risultato non è necessario, è possibile specificare *destSIN* e *destCOS* come NULL anziché specificare un registro.

I valori theta possono essere qualsiasi valore a virgola mobile IEEE a 32 bit.

L'errore assoluto massimo è 0,0008 nell'intervallo da -100 \* Pi a +100 \* Pi.

La tabella seguente mostra i risultati ottenuti quando si esegue l'istruzione con varie classi di numeri.

F indica un numero finito reale.



| **src**     | **-inf** | **-F**       | **-denorm** | **-0** | **+0** | **+denorm** | **+F**       | **+inf** | **NaN** |
|-------------|----------|--------------|-------------|--------|--------|-------------|--------------|----------|---------|
| **destSIN** | NaN      | \[Da -1 a +1\] | -0          | -0     | +0     | +0          | \[Da -1 a +1\] | NaN      | NaN     |
| **destCOS** | NaN      | \[Da -1 a +1\] | +1          | +1     | +1     | +1          | \[Da -1 a +1\] | NaN      | NaN     |



 

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

 

 





