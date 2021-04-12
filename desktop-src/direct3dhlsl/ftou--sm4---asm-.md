---
title: ftou (SM4-ASM)
description: Conversione da virgola mobile a Unsigned Integer.
ms.assetid: 0E3E090B-72C0-4CED-AFA5-2DDCF67D7263
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4a5e65e4bb9d4e71e4a2000f00861cf63e7c181
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335487"
---
# <a name="ftou-sm4---asm"></a>ftou (SM4-ASM)

Conversione da virgola mobile a Unsigned Integer.



| ftou dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\] |
|----------------------------------------------------|



 



| Ftoi dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\] |
|----------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nell' \] indirizzo del risultato dell'operazione. <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nel \] valore da convertire.<br/>                        |



 

## <a name="remarks"></a>Commenti

La conversione viene eseguita per ogni componente. L'arrotondamento viene sempre eseguito verso zero, dopo la convenzione C per i cast da float a int.

Le applicazioni che richiedono una semantica di arrotondamento diversa possono richiamare le istruzioni **round** prima di eseguire il cast su Integer.

Gli input vengono fissati nell'intervallo \[ 0,0 f... 4294967295.999 f \] prima della conversione e i valori NaN di input producono un risultato pari a zero.

I modificatori di valore assoluto e negazione facoltativi vengono applicati ai valori di origine prima della conversione.

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

 

 





