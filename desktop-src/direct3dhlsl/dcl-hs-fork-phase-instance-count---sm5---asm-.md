---
title: dcl_hs_fork_phase_instance_count (sm5 - asm)
description: Dichiarare il numero di istanze della fase di fork in una fase di fork dello shader di tipo hull shader.
ms.assetid: E38C48BB-3439-4F63-8DF8-21CF562CF5E6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d87117da3947ef9993a5e4d84616f8e62957b591848cf8b9668bfe8f7cba378
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024881"
---
# <a name="dcl_hs_fork_phase_instance_count-sm5---asm"></a>dcl \_ hs \_ fork \_ phase instance count \_ \_ (sm5 - asm)

Dichiarare il numero di istanze della fase di fork in una fase di fork dello shader di tipo hull shader.



| dcl \_ hs \_ fork \_ phase instance count \_ \_ {1...max 32-bit UINT} |
|-------------------------------------------------------------|



 



| Elemento                                                   | Descrizione                           |
|--------------------------------------------------------|---------------------------------------|
| <span id="N"></span><span id="n"></span>*N*<br/> | \[in \] Numero di istanze.<br/> |



 

## <a name="remarks"></a>Commenti

Questa istruzione si applica alle fasi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        | X    |        |          |       |         |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa istruzione è supportata nei modelli di shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (HLSL DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





