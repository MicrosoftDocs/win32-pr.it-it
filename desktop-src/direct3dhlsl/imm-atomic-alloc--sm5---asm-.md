---
title: imm_atomic_alloc (SM5-ASM)
description: Incrementare atomicamente il contatore nascosto a 32 bit archiviato con un conteggio o aggiungere la visualizzazione di accesso non ordinato (UAV), restituendo il valore originale.
ms.assetid: 534FA3C3-6FAC-41DC-AC07-0E53FEED000C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28a97709629497bae9af0298789453ef1d1172b7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719426"
---
# <a name="imm_atomic_alloc-sm5---asm"></a>IMM \_ Atomic \_ Alloc (SM5-ASM)

Incrementare atomicamente il contatore nascosto a 32 bit archiviato con un conteggio o aggiungere la visualizzazione di accesso non ordinato (UAV), restituendo il valore originale.



| IMM \_ Atomic \_ Alloc dst0 \[ . Single \_ Component \_ mask \] , dstUAV |
|-------------------------------------------------------------|



 



| Elemento                                                                                           | Descrizione                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                | \[in \] contiene il valore del contatore restituito.<br/>                    |
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[in \] un buffer strutturato UAV con il flag count o Append. <br/> |



 

## <a name="remarks"></a>Commenti

È presente un valore di contatore intero senza segno a 32 bit nascosto associato a ogni conteggio o visualizzazione buffer di Accodamento, che viene inizializzato quando la vista è associata alla pipeline, inclusa l'opzione per il mantenimento del valore precedente.

Questa istruzione esegue un incremento atomico del valore del contatore, restituendo l'originale a *dst0*.

Per un UAV Append, il valore restituito è valido solo per la durata della chiamata dello shader. Successivamente, l'implementazione può riorganizzare il layout di memoria. Tutti gli indirizzi di memoria basati sul valore restituito devono essere limitati alla chiamata dello shader.

Per un UAV Append, all'interno della chiamata dello shader il compilatore HLSL può usare il valore restituito come indice struct da usare per l'accesso al buffer strutturato. L'accesso a qualsiasi indice struct diverso da quello restituito dalle chiamate a **IMM \_ Atomic \_ Alloc** o [ \_ consume](imm-atomic-consume--sm5---asm-.md) genera risultati non definiti in quanto la posizione di memoria all'interno del UAV viene eseguita in modo casuale e fissa solo per la durata della chiamata dello shader.

Per un numero UAV, il valore restituito può essere salvato dall'applicazione come riferimento a un percorso fisso all'interno del UAV che è significativo dopo la chiamata dello shader. È possibile accedere sempre a qualsiasi posizione in un UAV di conteggio indipendentemente dal valore del conteggio.

Non è presente alcun blocco del conteggio, quindi esegue il wrapping in caso di overflow.

Lo stesso shader non è in grado di tentare di usare sia l' **\_ \_ allocazione** atomica di IMM che il **\_ \_ consumo atomico di IMM** nello stesso UAV. Inoltre, la GPU non può consentire la combinazione di più chiamate shader per la combinazione di **IMM \_ Atomic \_ Alloc** e **IMM \_ Atomic \_ consume** nello stesso UAV.

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

 

 





