---
title: atomic_iadd (sm5 - asm)
description: Integer atomico aggiunto alla memoria.
ms.assetid: 093C7FA5-41BF-4BDD-A35D-1AACE8CB9B5C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d582cdb4951cecc845cb868e7eee64be61b8f2d7387a0548c43e094cf308226f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118287754"
---
# <a name="atomic_iadd-sm5---asm"></a>atomic \_ iadd (sm5 - asm)

Integer atomico aggiunto alla memoria.



| atomic \_ iadd dst, dstAddress \[ .swizzle \] , src0 \[ .select \_ component\] |
|----------------------------------------------------------------------|



 



| Elemento                                                                                                           | Descrizione                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst"></span><span id="DST"></span>*Dst*<br/>                                                   | \[in \] Componenti da aggiungere con *src0*. Questo valore deve essere una visualizzazione di accesso non ordinato (UAV) (u \# ). Nello shader di calcolo può anche essere la memoria condivisa del gruppo di thread (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[in \] Indirizzo di memoria.<br/>                                                                                                                                                 |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[in \] Componenti da aggiungere a *dst*.<br/>                                                                                                                                     |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue un singolo componente con integer a 32 bit dell'operando *src0* *in dst* a 32 bit per indirizzo componente *dstAddress,* eseguito in modo atomico. Questa istruzione non è disensibile da firmare.

Il numero di componenti prelevati dall'indirizzo è determinato dalla dimensionalità di *dst* u \# o g \# .

Se *dst* è un u \# , può essere dichiarato come raw, typed o structured. Se digitato, deve essere dichiarato come UINT/SINT con il formato di risorsa associato R32 \_ \_ UINT/SINT.

Se *dst* è g \# , deve essere dichiarato come non elaborato o strutturato.

Non viene restituito nulla allo shader.

Se la chiamata dello shader è inattiva, ad esempio se il pixel è stato eliminato in precedenza durante l'esecuzione o se esiste una chiamata pixel/campione solo per fungere da helper per un pixel/campione reale per i derivati, questa istruzione non modifica affatto la memoria *dst* (in modo invisibile all'utente).

All'interno dei limiti che si indirizzano su u non viene scritto nulla in memoria, tranne se u è strutturato e l'offset dei byte nello struct (secondo componente dell'indirizzo) causa l'accesso fuori dai limiti, quindi l'intero contenuto dell'UAV diventa \# \# indefinito.

Se non sono definiti limiti per g (i limiti di quel particolare g , anziché tutta la memoria condivisa), l'intero contenuto di tutta la memoria condivisa diventa \# \# indefinito.

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

 

 





