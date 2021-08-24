---
title: imm_atomic_cmp_exch (sm5 - asm)
description: Confronto immediato e scambio con la memoria.
ms.assetid: 317A69E1-0E0A-45C8-8E0A-B88659ADBECC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba1014d338687a0798675ed407c0db844c80491833b45628020249bf94b6061b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562408"
---
# <a name="imm_atomic_cmp_exch-sm5---asm"></a>imm \_ atomic \_ cmp \_ exch (sm5 - asm)

Confronto immediato e scambio con la memoria.



| imm \_ atomic \_ cmp \_ exch dst0 \[ .single component mask , \_ \_ \] dst1, dstAddress \[ .swizzle \] , src0 \[ .select component , \_ \] src1 \[ .select \_ component\] |
|-----------------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                           | Descrizione                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[out \] Contiene *dst1* prima della scrittura.<br/>                                                                              |
| <span id="dst1"></span><span id="DST1"></span>*dst1*<br/>                                                | \[in \] Una visualizzazione di accesso non ordinato (UAV) (u \# ). Nel compute shader può anche trattarsi di memoria condivisa del gruppo di thread (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[in \] Memoria di destinazione.<br/>                                                                                         |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[in \] Valore da confrontare con *dst1*.<br/>                                                                                 |
| <span id="scr1"></span><span id="SCR1"></span>*scr1*<br/>                                                | \[in \] Valore scritto nella memoria di destinazione se i valori confrontati sono identici.<br/>                               |



 

Questa istruzione esegue un confronto di valori a 32 bit singolo componente dell'operando *src0* con *dst1* a 32 bit per indirizzo componente *dstAddress*.

Se *dst1* è un u \# , potrebbe essere stato dichiarato come raw, typed o structured. Se digitato, deve essere dichiarato come UINT/SINT con il formato di risorsa associato R32 \_ \_ UINT/SINT.

Se *dst1* è g \# , deve essere dichiarato come non elaborato o strutturato.

Se i valori confrontati sono identici, il valore a 32 bit a componente singolo in *src1* viene scritto nella memoria di destinazione. In caso contrario, la memoria di destinazione non viene modificata.

Il valore originale a 32 bit nella memoria di destinazione viene sempre scritto in *dst0*.

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

 

 





