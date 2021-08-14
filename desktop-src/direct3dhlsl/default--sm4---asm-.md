---
title: default (sm4 - asm)
description: Etichetta facoltativa in un'istruzione switch.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d54c3bbe83bd2499bdc2d50a30153bbc8b66e6ee53c29125b6a66416e419aa1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792677"
---
# <a name="default-sm4---asm"></a>default (sm4 - asm)

Etichetta facoltativa in [un'istruzione switch.](switch--sm4---asm-.md)



| default |
|---------|



 

## <a name="remarks"></a>Commenti

Questa istruzione funziona esattamente come il valore predefinito **in** C. Il controllo è valido solo se non è stato aggiunto codice, quindi più case (incluso il valore predefinito **)** possono condividere lo stesso blocco di codice.

In un **costrutto** switch è consentita una **sola istruzione** predefinita.

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

 

 




