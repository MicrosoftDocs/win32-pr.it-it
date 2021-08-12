---
title: ushr (sm5 - asm)
description: Maiusc a destra. | ushr (sm5 - asm)
ms.assetid: C695CB6C-A6C9-4DC8-8EBE-70A0CFFC4981
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b4f0cacaa785b34eb8910f12ecfe3578bd47781e41110adc71f4a7a7d52858a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118283047"
---
# <a name="ushr-sm5---asm"></a>ushr (sm5 - asm)

Maiusc a destra.



| ubfe dest \[ \] .mask, src0 \[ .swizzle, \] src1 \[ .swizzle\] |
|--------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Contiene i risultati dell'istruzione .<br/>                   |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Valori a 32 bit da spostare.<br/>                                |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] I 5 bit LSB forniscono il numero di bit da spostare (0-31).<br/> |



 

Questa istruzione esegue uno spostamento a livello di componente di ogni valore a 32 bit in *src0* a destra di un conteggio di bit intero senza segno fornito dai 5 bit LSB (intervallo 0-31) in *src1,* inserendo 0. I risultati a 32 bit per componente vengono inseriti in *dest*.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 





