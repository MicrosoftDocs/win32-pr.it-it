---
title: usubb (SM5-ASM)
description: Sottrazione di interi senza segno con prestito.
ms.assetid: 6D42E3CA-5A37-4194-AB42-7A2337C5AB9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111ffd134a75b8cfe19f63597cd80655201359c4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398202"
---
# <a name="usubb-sm5---asm"></a>usubb (SM5-ASM)

Sottrazione di interi senza segno con prestito.



| usubb dest0 \[ . mask \] , DesT1 \[ . mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\] |
|--------------------------------------------------------------------------|



 



| Elemento                                                               | Descrizione                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[in \] contiene i risultati di LSAB dell'istruzione.<br/>                                   |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[nel \] componente corrispondente di *dest0* che specifica se è stato generato un prestito.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[\]valore da cui sottrarre.<br/>                                               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>    | \[\]valore da sottrarre da *src0*.<br/>                                             |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue una sottrazione senza segno a livello di componente di operandi a 32 bit *src1* da *src0*, inserendo la parte LSB del risultato 32 bit in *dest0*.

Il componente corrispondente in *DesT1* viene scritto con 1 se viene prodotto un prestito, 0 in caso contrario.

*DesT1* può essere null se il prestito non è necessario.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





