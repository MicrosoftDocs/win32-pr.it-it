---
title: imm_atomic_consume (SM5-ASM)
description: Decrementa atomicamente il contatore nascosto a 32 bit archiviato con un conteggio o accodare una visualizzazione di accesso non ordinato (UAV), restituendo il nuovo valore.
ms.assetid: 1115C318-2F86-4161-AC5C-2A61A262DC28
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a1c6fe01ddb92b2ce870b16254f75c52cadd341
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993128"
---
# <a name="imm_atomic_consume-sm5---asm"></a>\_utilizzo atomico \_ di IMM (SM5-ASM)

Decrementa atomicamente il contatore nascosto a 32 bit archiviato con un conteggio o accodare una visualizzazione di accesso non ordinato (UAV), restituendo il nuovo valore.



| IMM \_ Atomic \_ USA dst0 \[ . Single \_ Component \_ mask \] , dstUAV |
|---------------------------------------------------------------|



 



| Elemento                                                                                           | Descrizione                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                | \[in \] contiene il valore del contatore originale restituito.<br/>           |
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[in \] un buffer strutturato UAV con il flag count o Append. <br/> |



 

## <a name="remarks"></a>Commenti

Per una discussione sulla validità del valore del conteggio restituito, vedere l'argomento relativo alla presenza di un UAV in base al conteggio o all'accodamento. [ \_ \_ ](imm-atomic-alloc--sm5---asm-.md) Lo stesso vale per **l' \_ \_ utilizzo atomico di IMM**.

**IMM \_ Atomic \_ consume** esegue un decremento atomico del valore del contatore, restituendo il nuovo valore a *dst0*.

Non è previsto alcun blocco del conteggio, quindi viene eseguito il wrapping in caso di underflow.

Lo stesso shader non è in grado di tentare di usare sia l' **\_ \_ allocazione** atomica di IMM che il **\_ \_ consumo atomico di IMM** nello stesso UAV. Inoltre, la GPU non può consentire la combinazione di più chiamate shader per la combinazione di **IMM \_ Atomic \_ Alloc** e **IMM \_ Atomic \_ consume** nello stesso UAV.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11,1, disponibile a partire da Windows 8.



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

 

 





