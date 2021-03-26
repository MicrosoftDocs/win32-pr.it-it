---
title: 'ftoi (sm4 - asm) '
description: Conversione da virgola mobile a Signed Integer.
ms.assetid: 580AB4A6-0C1C-409B-B2B9-BA1D37772F46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02ce1b506d112a59d3087f59d219557575b8def
ms.sourcegitcommit: 8c658e9872a2173e3dcec94195f9067fbcd85d3d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/17/2020
ms.locfileid: "104339519"
---
# <a name="ftoi-sm4---asm"></a>ftoi (sm4 - asm) 

Conversione da virgola mobile a Signed Integer.

| Ftoi dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\] |
|-|

| Elemento | Descrizione |
|-|-|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[nell' \] indirizzo del risultato dell'operazione.<br/> *dest*  =  [round \_ z](round-z--sm4---asm-.md)(*src0*)<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nel \] componente da convertire.<br/> |

## <a name="remarks"></a>Commenti

La conversione viene eseguita per ogni componente. L'arrotondamento viene sempre eseguito verso zero, dopo la convenzione C per i cast da float a int. Le applicazioni che richiedono una semantica di arrotondamento diversa possono richiamare le istruzioni **round** prima di eseguire il cast su Integer.

Gli input vengono bloccati nell'intervallo \[ -2147483648.999 f... 2147483647.999 f \] prima della conversione e i valori NaN di input producono un risultato pari a zero.

I modificatori di valore assoluto e negazione facoltativi vengono applicati ai valori di origine prima della conversione.

Questa istruzione si applica alle fasi dello shader seguenti:

| Vertex shader | Geometry shader | Pixel shader |
|-|-|-|
| x | x | x |

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.

| Modello di shader | Supportato |
|-|-|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md) | sì |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md) | sì |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md) | sì |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no |

## <a name="related-topics"></a>Argomenti correlati

[Assembly Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
