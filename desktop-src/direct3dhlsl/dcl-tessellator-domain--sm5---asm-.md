---
title: dcl_tessellator_domain (sm5 - asm)
description: Dichiarare il dominio del tessellatore in una sezione della dichiarazione dello shader di struttura e lo shader del dominio.
ms.assetid: 11A1D9D0-D848-4750-875B-7060CE1CF42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52a027e9fab091cf31e8577266015e974ec78033fe19a9542f0aa3c6ca4651db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986711"
---
# <a name="dcl_tessellator_domain-sm5---asm"></a>dcl \_ tessellator \_ domain (sm5 - asm)

Dichiarare il dominio del tessellatore in una sezione della dichiarazione dello shader di struttura e lo shader del dominio.



| dcl \_ tessellator \_ domain {domain \_ isoline \| domain \_ tri \| domain \_ quad} |
|---------------------------------------------------------------------------|



 



| Elemento                                                                                                                                                                                | Descrizione                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="domain_isoline___domain_tri___domain_quad"></span><span id="DOMAIN_ISOLINE___DOMAIN_TRI___DOMAIN_QUAD"></span>*domain \_ isoline \| domain tri domain \_ \| \_ quad*<br/> | \[in \] Il dominio.<br/> |



 

## <a name="remarks"></a>Commenti

Il comportamento non è definito se lo hull shader e il domain shader forniscono domini non corrispondenti o qualsiasi altra dealarazione in conflitto.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertice | Scafo                 | Dominio | Geometria | Pixel | Calcolo |
|--------|----------------------|--------|----------|-------|---------|
|        | Sezione Declarations | X      |          |       |         |



 

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

 

 





