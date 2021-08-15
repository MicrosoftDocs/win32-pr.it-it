---
title: imm_atomic_alloc (sm5 - asm)
description: Incrementare in modo atomico il contatore nascosto a 32 bit archiviato con una visualizzazione di accesso non ordinato Count o Append, che restituisce il valore originale.
ms.assetid: 534FA3C3-6FAC-41DC-AC07-0E53FEED000C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf18b7602803f5f1128d942cc59b8f5365c2e1b69fb1287aaba682f690c52a3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117907205"
---
# <a name="imm_atomic_alloc-sm5---asm"></a>imm \_ atomic \_ alloc (sm5 - asm)

Incrementare in modo atomico il contatore nascosto a 32 bit archiviato con una visualizzazione di accesso non ordinato Count o Append, che restituisce il valore originale.



| imm \_ atomic \_ alloc dst0 \[ .single component mask , \_ \_ \] dstUAV |
|-------------------------------------------------------------|



 



| Elemento                                                                                           | Descrizione                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                | \[in \] Contiene il valore del contatore restituito.<br/>                    |
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[in \] un UAV del buffer strutturato con il flag Count o Append. <br/> |



 

## <a name="remarks"></a>Commenti

È presente un valore del contatore intero senza segno a 32 bit nascosto associato a ogni visualizzazione Conteggio o Accoda buffer che viene inizializzata quando la vista è associata alla pipeline, inclusa l'opzione per mantenere il valore precedente.

Questa istruzione esegue un incremento atomico del valore del contatore, restituisce l'oggetto originale *a dst0*.

Per un UAV append, il valore restituito è valido solo per la durata della chiamata dello shader. successivamente l'implementazione può ridisporre il layout di memoria. Qualsiasi indirizzamento alla memoria basato sul valore restituito deve essere limitato alla chiamata dello shader.

Per un UAV append, all'interno della chiamata dello shader il compilatore HLSL può usare il valore restituito come indice dello struct da usare per accedere al buffer strutturato. L'accesso a qualsiasi indice di struct diverso da quelle restituite [ \_](imm-atomic-consume--sm5---asm-.md) dalle chiamate a **imm \_ atomic \_ alloc** o consume produce risultati indefiniti in quanto la posizione di memoria all'interno dell'UAV a cui si accede è casuale e fissa solo per la durata della chiamata dello shader.

Per un UAV Count, il valore restituito può essere salvato dall'applicazione come riferimento a una posizione fissa all'interno dell'UAV che è significativa al termine della chiamata dello shader. È sempre possibile accedere a qualsiasi posizione in un UAV Count indipendentemente dal valore del conteggio.

Non è presente alcuna chiusura del conteggio, quindi esegue il wrapping in caso di overflow.

Lo stesso shader non può tentare sia **l'utilizzo \_ \_ atomico imm che** **l'utilizzo \_ atomico \_ imm** sullo stesso UAV. Inoltre, la GPU non può consentire a più chiamate di shader di combinare **imm \_ atomic \_ alloc** e **imm \_ atomic \_ consume** sullo stesso UAV.

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

 

 





