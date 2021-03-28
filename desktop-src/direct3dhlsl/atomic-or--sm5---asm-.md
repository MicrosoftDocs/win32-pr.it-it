---
title: atomic_or (SM5-ASM)
description: Bit per bit atomico o alla memoria.
ms.assetid: 5AFB96AA-267B-454E-9526-BA61A876ED42
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 245f1b02edd74712471206b095f0c8a9040962b6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104516501"
---
# <a name="atomic_or-sm5---asm"></a>Atomic \_ o (SM5-ASM)

Bit per bit atomico o alla memoria.



| \_componente Atomic o DST, dstAddress \[ . Swizzle \] , src0 \[ . Select \_\] |
|--------------------------------------------------------------------|



 



| Elemento                                                                                                           | Descrizione                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst"></span><span id="DST"></span>*DST*<br/>                                                   | \[nei \] componenti a o con *src0*. Questo valore deve essere una visualizzazione di accesso non ordinato (UAV) (u \# ). Nel compute shader può anche essere la memoria condivisa del gruppo di thread (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[nell' \] indirizzo di memoria.<br/>                                                                                                                                                |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[nei \] componenti a o con l' *ora legale*.<br/>                                                                                                                                   |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue un singolo componente bit per bit a 32 bit di *src0* dell'operando nell' *ora legale* a 32 bit per indirizzo componente *dstAddress*, eseguito atomicamente.

Il numero di componenti presi dall'indirizzo è determinato dalla dimensionalità dell' *ora legale* u \# o g \# .

Se *DST* è un u \# , può essere dichiarato come RAW, tipizzato o strutturato. Se tipizzata, deve essere dichiarata come UINT/SINT con il formato di risorsa associato R32 \_ uint/ \_ Sint.

Se *DST* è g \# , deve essere dichiarato come RAW o Structured.

Non viene restituito nulla allo shader.

Se la chiamata dello shader è inattiva, ad esempio se il pixel è stato scartato in precedenza nell'esecuzione o se una chiamata di pixel/campione esiste solo per fungere da helper per un pixel/campione reale per i derivati, questa istruzione non modifica la memoria *DST* (in modo invisibile all'utente).

Al di fuori dell'indirizzamento su u \# non viene scritto alcun elemento nella memoria, tranne nel caso in cui l'u \# sia strutturata e l'offset dei byte nello struct (secondo componente dell'indirizzo) provochi l'accesso fuori limite, quindi l'intero contenuto del UAV diventa non definito.

All'esterno dei limiti che puntano a g \# (i limiti di tale particolare g \# , anziché di tutta la memoria condivisa), l'intero contenuto di tutta la memoria condivisa diventa indefinito.

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

 

 





