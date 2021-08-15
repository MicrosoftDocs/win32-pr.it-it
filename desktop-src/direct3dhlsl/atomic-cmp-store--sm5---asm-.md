---
title: atomic_cmp_store (sm5 - asm)
description: Confronto atomico e scrittura in memoria.
ms.assetid: 1B97E983-11A9-47E4-B274-E94083837C6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dbc57b14b4279b9bd4844d89492852ae915d9d900ed04421eeeccc367979a63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118795163"
---
# <a name="atomic_cmp_store-sm5---asm"></a>atomic \_ cmp \_ store (sm5 - asm)

Confronto atomico e scrittura in memoria.



| atomic \_ cmp \_ store dst, dstAddress \[ .swizzle, \] src0 \[ .select component , \_ \] src1 \[ .select \_ component\] |
|--------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                           | Descrizione                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst"></span><span id="DST"></span>*Dst*<br/>                                                   | \[in \] Componenti da confrontare con *src0*. Questo valore deve essere una visualizzazione di accesso non ordinato (UAV) (u \# ). Nello shader di calcolo può anche essere memoria condivisa del gruppo di thread (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[in \] Indirizzo di memoria.<br/>                                                                                                                                                     |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[in \] Valore a 32 bit da confrontare con *dst*.<br/>                                                                                                                                 |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                                | \[in \] Valore da scrivere in memoria se i valori confrontati sono identici. <br/>                                                                                                     |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue un confronto di valori a 32 bit di un singolo componente dell'operando *src0* con *dst* a 32 bit per ogni indirizzo del componente *dstAddress*.

Se i valori confrontati sono identici, il valore a 32 bit a componente singolo in *src1* viene scritto nella memoria di destinazione. In caso contrario, la destinazione non viene modificata.

L'intera operazione di confronto e scrittura viene eseguita in modo atomico.

Se *dst* è un u \# , può essere dichiarato come non elaborato, tipidato o strutturato. Se tipiggiato, deve essere dichiarato come UINT/SINT con il formato di risorsa associato che è R32 \_ \_ UINT/SINT.

Se *dst* è g \# , deve essere dichiarato come non elaborato o strutturato.

Il numero di componenti presi dall'indirizzo è determinato dalla dimensionalità di dst u \# o g \# .

Non viene restituito nulla allo shader.

Se la chiamata dello shader è inattiva, ad esempio se il pixel è stato eliminato in precedenza durante l'esecuzione o un'istruzione pixel/campione non modifica affatto la memoria *dst* (invisibile all'utente).

Se l'offset di byte nello struct (secondo componente dell'indirizzo) non comporta la scrittura in memoria di alcun elemento, tranne se u è strutturato e l'offset dei byte nello struct (secondo componente dell'indirizzo) causa l'accesso fuori dai limiti, l'intero contenuto dell'UAV diventa \# \# indefinito.

Fuori dai limiti che si indirizzano a g (i limiti di quel particolare g , anziché di tutta la memoria condivisa) fa sì che l'intero contenuto di tutta la memoria condivisa diventi \# \# indefinito.

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

 

 





