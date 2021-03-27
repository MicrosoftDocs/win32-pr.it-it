---
title: atomic_cmp_store (SM5-ASM)
description: Confronto atomico e scrittura in memoria.
ms.assetid: 1B97E983-11A9-47E4-B274-E94083837C6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26a5292d65b32988017044a2ec52680848dffbef
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719441"
---
# <a name="atomic_cmp_store-sm5---asm"></a>\_ \_ Archivio di CMP atomico (SM5-ASM)

Confronto atomico e scrittura in memoria.



| Atomic \_ CMP \_ Store DST, dstAddress \[ . Swizzle \] , src0 \[ . Select \_ Component \] , src1 \[ . Select \_ Component\] |
|--------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                           | Descrizione                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst"></span><span id="DST"></span>*DST*<br/>                                                   | \[nei \] componenti da confrontare con *src0*. Questo valore deve essere una visualizzazione di accesso non ordinato (UAV) (u \# ). Nel compute shader può anche essere la memoria condivisa del gruppo di thread (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[nell' \] indirizzo di memoria.<br/>                                                                                                                                                     |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[nel \] valore a 32 bit da confrontare con l' *ora legale*.<br/>                                                                                                                                 |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                                | \[nel \] valore da scrivere in memoria se i valori confrontati sono identici. <br/>                                                                                                     |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue un confronto tra i valori a 32 bit del singolo componente dell'operando *src0* con *DST* a 32 bit per ogni indirizzo del componente *dstAddress*.

Se i valori confrontati sono identici, il valore a 32 bit a singolo componente in *src1* viene scritto nella memoria di destinazione. In caso contrario, la destinazione non viene modificata.

L'intera operazione di confronto e scrittura viene eseguita in modo atomico.

Se *DST* è un u \# , può essere dichiarato come RAW, tipizzato o strutturato. Se tipizzata, deve essere dichiarata come UINT/SINT con il formato di risorsa associato R32 \_ uint/ \_ Sint.

Se *DST* è g \# , deve essere dichiarato come RAW o Structured.

Il numero di componenti presi dall'indirizzo è determinato dalla dimensionalità dell'ora legale u \# o g \# .

Non viene restituito nulla allo shader.

Se la chiamata dello shader è inattiva, ad esempio se il pixel è stato scartato in precedenza durante l'esecuzione o se un'istruzione pixel/Sample non modifica la memoria *DST* (in modo invisibile all'utente).

L'indirizzamento fuori dall'indirizzamento su u \# non comporta la scrittura in memoria, tranne nel caso in cui l'u \# sia strutturato e l'offset dei byte nello struct (secondo componente dell'indirizzo) provochi l'accesso fuori limite, quindi l'intero contenuto del UAV diventa non definito.

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

 

 





