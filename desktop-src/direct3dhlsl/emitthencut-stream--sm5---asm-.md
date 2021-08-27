---
title: emitThenCut_stream (sm5 - asm)
description: Equivale a un comando emit seguito da un comando cut. | emitThenCut_stream (sm5 - asm)
ms.assetid: E9D84647-E29B-4E31-9E95-9F7A173293D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 522d2be28ae1d63617b8ba775f8f8839c270668aeeded8a4944ef9ae7554d598
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067961"
---
# <a name="emitthencut_stream-sm5---asm"></a>Flusso emitThenCut \_ (sm5 - asm)

Equivale a un [comando emit](emit--sm4---asm-.md) seguito da un [comando cut.](cut--sm4---asm-.md)



| flusso emitThenCut \_ streamIndex |
|---------------------------------|



 



| Elemento                                                                                                               | Descrizione                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[in \] Indice del flusso.<br/> |



 

## <a name="remarks"></a>Commenti

Questa operazione è utile quando si restituisce consapevolmente l'ultimo vertice in una topologia.

Se i flussi non sono stati dichiarati, è necessario usare [emitThenCut](emitthencut--sm4---asm-.md) anziché **emitThenCut \_ stream**.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

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

 

 





