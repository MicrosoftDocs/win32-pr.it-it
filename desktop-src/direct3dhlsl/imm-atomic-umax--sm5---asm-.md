---
title: imm_atomic_umax (sm5 - asm)
description: Numero massimo senza segno atomico immediato in memoria. Restituisce il valore in memoria prima dell'operazione max.
ms.assetid: 6C9D2CA3-1502-41E1-8535-C94DF31201E1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399142e182cbf33a8adea3ac8236fdc81e4f4b100e562e65bbb39057b6e6e192
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986511"
---
# <a name="imm_atomic_umax-sm5---asm"></a>imm \_ atomic \_ umax (sm5 - asm)

Numero massimo senza segno atomico immediato in memoria. Restituisce il valore in memoria prima dell'operazione max.



| imm \_ atomic \_ umax dst0 \[ .single component mask , \_ \_ \] dst1, dstAddress \[ .swizzle \] , src0 \[ .select \_ component\] |
|--------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                           | Descrizione                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[in \] Contiene il valore di *dst1* prima di questa istruzione.<br/>                                                         |
| <span id="dst1"></span><span id="DST1"></span>*dst1*<br/>                                                | \[in \] Una visualizzazione di accesso non ordinato (UAV) (u \# ). Nel compute shader può anche trattarsi di memoria condivisa del gruppo di thread (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[in \] Indirizzo di memoria.<br/>                                                                                             |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[in \] Valore da confrontare con *dst1* in *dstAddress*.<br/>                                                                 |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue un singolo componente senza segno massimo a 32 bit dell'operando *src0* con *dst1* a 32 bit per indirizzo componente *dstAddress*.

Se *dst1* è un u \# , potrebbe essere stato dichiarato come raw, typed o structured. Se digitato, deve essere dichiarato come UINT/SINT con il formato di risorsa associato R32 \_ \_ UINT/SINT.

Se *dst1* è g \# , deve essere dichiarato come non elaborato o strutturato.

Il valore nella *memoria dst1* prima che max venga restituito *a dst0*.

Il numero di componenti prelevati dall'indirizzo è determinato dalla dimensionalità di *dst1*.

L'intera operazione viene eseguita in modo atomico.

Se la chiamata dello shader è inattiva, ad esempio se il pixel è stato eliminato in precedenza durante l'esecuzione o se esiste solo una chiamata pixel/campione per fungere da helper per un pixel/campione reale per i derivati, questa istruzione non modifica affatto la memoria *dst1* e il valore restituito non è definito.

All'interno dei limiti che si indirizzano su u non viene scritto nulla in memoria, tranne se u è strutturato e l'offset dei byte nello struct (secondo componente dell'indirizzo) causa l'accesso fuori dai limiti, quindi l'intero contenuto dell'UAV diventa \# \# indefinito.

Se non sono presenti limiti per l'indirizzamento in u o g, viene restituito un risultato non definito \# \# allo shader in *dst0*.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Poiché gli UAV sono disponibili in tutte le fasi dello shader per Direct3D 11.1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11.1, disponibile a partire da Windows 8.



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 





