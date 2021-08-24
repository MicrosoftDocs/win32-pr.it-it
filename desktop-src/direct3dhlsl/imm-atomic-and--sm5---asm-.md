---
title: imm_atomic_and (sm5 - asm)
description: AND atomico immediato in memoria. Restituisce il valore in memoria prima di AND.
ms.assetid: DA2A70C3-57BD-41F0-865C-235AA4DF1A52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53992096dccf4d4f0c4e8e98cbafd08f65ce852e28389c8c725f7f2594c7ec4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672801"
---
# <a name="imm_atomic_and-sm5---asm"></a>imm \_ atomic \_ e (sm5 - asm)

AND atomico immediato in memoria. Restituisce il valore in memoria prima di AND.



| imm \_ atomic \_ e dst0 \[ .single component mask , \_ \_ \] dst1, dstAddress \[ .swizzle, \] src0 \[ .select \_ component\] |
|-------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                           | Descrizione                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[in \] Contiene il valore di *dst1* prima di AND.<br/>                                                                      |
| <span id="dst1"></span><span id="DST1"></span>*dst1*<br/>                                                | \[in \] Una visualizzazione di accesso non ordinato (UAV) (u \# ). Nello shader di calcolo può anche essere memoria condivisa del gruppo di thread (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[in \] Memoria di destinazione.<br/>                                                                                         |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | Valore di and con *dst*.<br/>                                                                                           |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue un singolo componente a 32 bit AND bit per bit dell'operando *src0* con *dst1* a 32 bit per ogni indirizzo del componente *dstAddress*.

Se *dst1* è un u , potrebbe essere stato dichiarato come non \# elaborato, tipidato o strutturato. Se tipiggiato, deve essere dichiarato come UINT/SINT con il formato di risorsa associato che è R32 \_ \_ UINT/SINT.

Se *dst1* è g \# , deve essere dichiarato come non elaborato o strutturato.

Valore in *memoria dst1* prima che AND venga restituito *a dst0*.

L'intera operazione viene eseguita in modo atomico.

Il numero di componenti presi dall'indirizzo è determinato dalla dimensionalità della risorsa dichiarata *in dst1*.

Se la chiamata dello shader è inattiva, ad esempio se il pixel è stato eliminato in precedenza durante l'esecuzione o esiste solo una chiamata pixel/campione per fungere da helper per un pixel/campione reale per i derivati, questa istruzione non modifica affatto la memoria *dst1* e il valore restituito non è definito.

Se l'offset di byte nello struct (secondo componente dell'indirizzo) non comporta la scrittura in memoria di alcun elemento, tranne se u è strutturato e l'offset dei byte nello struct (secondo componente dell'indirizzo) causa l'accesso fuori dai limiti, l'intero contenuto dell'UAV diventa \# \# indefinito.

Fuori dai limiti che si indirizzano a u o g, viene restituito un risultato non definito allo \# \# shader in *dst0*.

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

 

 





