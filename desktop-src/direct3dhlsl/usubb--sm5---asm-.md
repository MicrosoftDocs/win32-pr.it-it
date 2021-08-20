---
title: usubb (sm5 - asm)
description: Sottrazione di un intero senza segno con borrow.
ms.assetid: 6D42E3CA-5A37-4194-AB42-7A2337C5AB9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c2f70f39729f5245f7044945e9d3b233ec4f0893be27c5143f5c55989693b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721825"
---
# <a name="usubb-sm5---asm"></a>usubb (sm5 - asm)

Sottrazione di un intero senza segno con borrow.



| usubb dest0 \[ .mask \] , dest1 \[ .mask \] , src0 \[ .swizzle \] , src1 \[ .swizzle\] |
|--------------------------------------------------------------------------|



 



| Elemento                                                               | Descrizione                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[in \] contiene i risultati LSAB dell'istruzione .<br/>                                   |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[in \] Componente corrispondente di *dest0 che* specifica se è stato prodotto un prestito.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[in \] Valore da cui sottrarre.<br/>                                               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>    | \[in \] Quantità da sottrarre da *src0*.<br/>                                             |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue una sottrazione senza segno a livello di componente di operandi a 32 bit *src1* da *src0,* inserendo la parte LSB del risultato a 32 bit in *dest0*.

Il componente corrispondente in *dest1* viene scritto con 1 se viene prodotto un prestito, 0 in caso contrario.

*dest1* può essere NULL se il prestito non è necessario.

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

 

 





