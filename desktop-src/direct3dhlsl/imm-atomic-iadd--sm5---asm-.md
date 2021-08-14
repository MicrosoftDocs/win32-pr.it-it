---
title: imm_atomic_iadd (sm5 - asm)
description: Aggiunta immediata di numeri interi atomici alla memoria. Restituisce il valore in memoria prima dell'aggiunta.
ms.assetid: 24136B4C-D37C-4449-A318-57145BB8D8E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d80a24fad3731f3d55c09f232ec61f4b3b09828cc7abd698e74259efe907c6d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511416"
---
# <a name="imm_atomic_iadd-sm5---asm"></a>imm \_ atomic \_ iadd (sm5 - asm)

Aggiunta immediata di numeri interi atomici alla memoria. Restituisce il valore in memoria prima dell'aggiunta.



| imm \_ atomic \_ iadd dst0 \[ .single component mask , \_ \_ \] dst1, dstAddress \[ .swizzle, \] src0 \[ .select \_ component\] |
|--------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                           | Descrizione                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[in \] Contiene il valore in *dst1* prima della scrittura. <br/>                                                                           |
| <span id="dst1"></span><span id="DST1"></span>*dst1*<br/>                                                | Questo valore deve essere una visualizzazione di accesso non ordinato (UAV) (u \# ). Nello shader di calcolo può anche essere memoria condivisa del gruppo di thread (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[in \] Naddress di memoria.<br/>                                                                                                      |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[in \] Valore da aggiungere a *dst1*.<br/>                                                                                               |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue un singolo componente intero a 32 bit di aggiunta dell'operando *src0* con *dst1* a 32 bit per ogni indirizzo del componente *dstAddress*. La firma non fa distinzione tra maiuscole e minuscole.

Se *dst1* è un u , potrebbe essere stato dichiarato come non \# elaborato, tipiato o strutturato. Se tipiggiato, deve essere dichiarato come UINT/SINT con il formato di risorsa associato che è R32 \_ \_ UINT/SINT.

Se *dst1* è g \# , deve essere dichiarato come non elaborato o strutturato.

Valore nella memoria *dst1* prima che l'addizione venga restituita *a dst0*.

Il numero di componenti presi dall'indirizzo è determinato dalla dimensionalità di *dst1*.

L'intera operazione viene eseguita in modo atomico.

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

 

 





