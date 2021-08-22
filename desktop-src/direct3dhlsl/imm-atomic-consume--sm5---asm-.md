---
title: imm_atomic_consume (sm5 - asm)
description: Decrementare in modo atomico il contatore nascosto a 32 bit archiviato con una vista di accesso non ordinato (UAV, Unordered Access View) o Append non ordinata, restituisce il nuovo valore.
ms.assetid: 1115C318-2F86-4161-AC5C-2A61A262DC28
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0244b885d9d2c46b734994d5e101f79147839d0cf76e2bab5669e52700cf59e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119315"
---
# <a name="imm_atomic_consume-sm5---asm"></a>imm \_ atomic \_ consume (sm5 - asm)

Decrementare in modo atomico il contatore nascosto a 32 bit archiviato con una vista di accesso non ordinato (UAV, Unordered Access View) o Append non ordinata, restituisce il nuovo valore.



| imm \_ atomic \_ consume dst0 \[ .single component mask , \_ \_ \] dstUAV |
|---------------------------------------------------------------|



 



| Elemento                                                                                           | Descrizione                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                | \[in \] Contiene il valore del contatore originale restituito.<br/>           |
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[in \] un UAV del buffer strutturato con il flag Count o Append. <br/> |



 

## <a name="remarks"></a>Commenti

Vedere [imm \_ atomic \_ alloc](imm-atomic-alloc--sm5---asm-.md) per una discussione sulla validità del valore di conteggio restituito a seconda che l'UAV sia Count o Append. Lo stesso vale per **imm \_ atomic \_ consume**.

**imm \_ atomic \_ consume** esegue un decremento atomico del valore del contatore, restituisce il nuovo valore *a dst0*.

Non è presente alcuna chiusura del conteggio, quindi esegue il wrapping in underflow.

Lo stesso shader non può tentare sia **imm \_ atomic \_ alloc** che **imm \_ atomic \_ consume** sullo stesso UAV. Inoltre, la GPU non può consentire a più chiamate shader di combinare **imm \_ atomic \_ alloc** e **imm \_ atomic \_ consume** sullo stesso UAV.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Poiché gli UAV sono disponibili in tutte le fasi dello shader per Direct3D 11.1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11.1, disponibile a partire da Windows 8.



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

 

 





