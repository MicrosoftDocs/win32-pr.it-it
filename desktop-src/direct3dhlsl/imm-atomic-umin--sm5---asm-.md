---
title: imm_atomic_umin (SM5-ASM)
description: Min senza segno atomico immediato alla memoria. Restituisce un valore in memoria prima dell'operazione max.
ms.assetid: B4556DA0-EE34-4420-A3AE-B340B4B1EB83
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8c65b2b5a58859e0729f567d9575f889b589821
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046064"
---
# <a name="imm_atomic_umin-sm5---asm"></a>IMM \_ Atomic \_ Umin (SM5-ASM)

Min senza segno atomico immediato alla memoria. Restituisce un valore in memoria prima dell'operazione max.



| IMM \_ Atomic \_ Umin dst0 \[ . Single \_ Component \_ mask \] , DST1, dstAddress \[ . Swizzle \] , src0 \[ . Select \_ Component\] |
|--------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                           | Descrizione                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[in \] contiene il valore di *DST1* prima di questa istruzione.<br/>                                                         |
| <span id="dst1"></span><span id="DST1"></span>*dst1*<br/>                                                | \[in \] una visualizzazione di accesso non ordinato (UAV) (u \# ). In compute shader questo può essere anche la memoria condivisa del gruppo di thread (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[nell' \] indirizzo di memoria.<br/>                                                                                             |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[nel \] valore da confrontare con *Dst1* in *dstAddress*.<br/>                                                                 |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue un singolo componente a 32 bit senza segno di operando *src0* con *DST1* a 32 bit per indirizzo componente *dstAddress*.

Se *DST1* è un u \# , potrebbe essere stato dichiarato come RAW, tipizzato o strutturato. Se tipizzata, deve essere dichiarata come UINT/SINT con il formato di risorsa associato R32 \_ uint/ \_ Sint.

Se *DST1* è g \# , deve essere dichiarato come RAW o Structured.

Il valore in *DST1* Memory prima del valore min viene restituito a *dst0*.

Il numero di componenti presi dall'indirizzo è determinato dalla dimensionalità di *DST1*.

L'intera operazione viene eseguita in modo atomico.

Se la chiamata dello shader è inattiva, ad esempio se il pixel è stato scartato in precedenza nell'esecuzione o se una chiamata di pixel/campione esiste solo per fungere da helper per un pixel/campione reale per i derivati, questa istruzione non modifica la memoria *DST1* e il valore restituito non è definito.

L'indirizzamento fuori dall'indirizzamento su u \# non comporta la scrittura in memoria, tranne nel caso in cui l'u \# sia strutturato e l'offset dei byte nello struct (secondo componente dell'indirizzo) provochi l'accesso fuori limite, quindi l'intero contenuto del UAV diventa non definito.

L'indirizzamento fuori limite su u \# o g \# causa la restituzione di un risultato non definito allo shader in *dst0*.

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

 

 





