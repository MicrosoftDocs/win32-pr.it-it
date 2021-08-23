---
title: ishr (sm5 - asm)
description: Spostamento aritmetico a destra (estensione del segno). | ishr (sm5 - asm)
ms.assetid: 8124B6C3-4576-4616-85A9-A2DD19EB6BB9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c75d64ded9beb6cdc5660d6157b15fc989863ee9e907e67c00854fe7cfe161
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488331"
---
# <a name="ishr-sm5---asm"></a>ishr (sm5 - asm)

Spostamento aritmetico a destra (estensione del segno).



| ishl dest \[ \] .mask, src0 \[ .swizzle, \] src1 \[ .swizzle\] |
|--------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Contiene i risultati dello spostamento.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Numero di bit da spostare.<br/>       |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Valori a 32 bit da spostare.<br/>        |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue uno spostamento aritmetico a livello di componente di ogni valore a 32 bit in *src0* a destra di un numero di bit intero senza segno fornito dall'intervallo LSB a 5 bit (intervallo da 0 a 31) in *src1,* replicando il valore del bit 31. Il risultato a 32 bit per componente viene inserito in *dest*.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





