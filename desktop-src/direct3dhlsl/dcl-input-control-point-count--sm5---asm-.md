---
title: dcl_input_control_point_count (sm5 - asm)
description: Dichiarare il conteggio dei punti di controllo di input di hull shader nella sezione della dichiarazione dello shader di tipo hull.
ms.assetid: 2E524BF0-3DD0-446A-8437-0CF17B348D83
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68c5414d5c660cf0bbce2b6219769cd36d4da9bbf3e59d9d130bfce0e0dceea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789881"
---
# <a name="dcl_input_control_point_count-sm5---asm"></a>dcl \_ input control point count \_ \_ \_ (sm5 - asm)

Dichiarare il conteggio dei punti di controllo di input di hull shader nella sezione della dichiarazione dello shader di tipo hull.



| dcl \_ input control point count \_ \_ \_ {1..32} |
|-------------------------------------------|



 



| Elemento                                                   | Descrizione                                      |
|--------------------------------------------------------|--------------------------------------------------|
| <span id="N"></span><span id="n"></span>*N*<br/> | \[in \] Conteggio dei punti di controllo di input.<br/> |



 

## <a name="remarks"></a>Commenti

È necessario almeno un punto di controllo di input. Può essere vuoto se non è necessario.

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

 

 





