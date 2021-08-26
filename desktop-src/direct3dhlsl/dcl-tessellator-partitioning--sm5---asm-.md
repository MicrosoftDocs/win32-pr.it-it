---
title: dcl_tessellator_partitioning (sm5 - asm)
description: Dichiarare il partizionamento a tessellatore in una sezione di dichiarazione dello shader di tipo hull.
ms.assetid: 6EA00C6B-A0DE-4CE4-8B52-1337CA92CA5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae40873db4042e568ae637634e75db6f4746985a316bf9c1e092e6b0925b51b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068501"
---
# <a name="dcl_tessellator_partitioning-sm5---asm"></a>dcl \_ tessellator \_ partitioning (sm5 - asm)

Dichiarare il partizionamento a tessellatore in una sezione di dichiarazione dello shader di tipo hull.



| dcl \_ tessellator \_ partitioning {partitioning \_ integer\| partizionamento \_ pow2\|partizionamento \_ dispari \_ frazionari\| partizionamento \_ frazionaria \_ pari} |
|---------------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Descrizione                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="partitioning_integer__________________________________partitioning_pow2_partitioning_fractional_odd__________________________________partitioning_fractional_even"></span><span id="PARTITIONING_INTEGER__________________________________PARTITIONING_POW2_PARTITIONING_FRACTIONAL_ODD__________________________________PARTITIONING_FRACTIONAL_EVEN"></span>*partizionamento di \_ \| interi \_ pow2 \| partizionamento frazionaria \_ \_ frazionaria \| \_ frazionaria \_ pari*<br/> | \[in \] Partizionamento a tessellatore.<br/> |



 

## <a name="remarks"></a>Commenti

Dal punto di vista dell'hardware, \_ pow2 si comporta come \_ un numero intero. È responsabilità dell'autore dello shader HLSL e/o del codice del compilatore arrotondare TessFactors alla potenza di 2.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertice | Scafo                 | Dominio | Geometria | Pixel | Calcolo |
|--------|----------------------|--------|----------|-------|---------|
|        | Sezione Declarations |        |          |       |         |



 

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

 

 





