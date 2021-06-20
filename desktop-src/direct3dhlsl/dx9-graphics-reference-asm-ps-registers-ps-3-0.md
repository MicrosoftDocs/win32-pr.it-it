---
title: ps_3_0 registri
description: Questo articolo contiene informazioni di riferimento per i registri di input e output implementati pixel shader versione 3_0.
ms.assetid: 01bee50a-c1b7-4b15-9df8-1dd52d9ff163
keywords:
- vPos
- Registro delle posizioni, pixel shader
- Registri - ps_3_0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e1cd0173beabc8fbe21ad15e88e23fc1b6e84892
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405494"
---
# <a name="ps_3_0-registers"></a>ps \_ 3 \_ 0 Registri

I pixel shader dipendono dai registri per ottenere i dati dei vertici, per l'output dei dati pixel, per contenere i risultati temporanei durante i calcoli e per identificare le fasi di campionamento delle trame. Esistono diversi tipi di registri, ognuno con una funzionalità univoca. Questa sezione contiene informazioni di riferimento per i registri di input e output implementati pixel shader versione 3 \_ 0.

## <a name="new-registers"></a>Nuovi registri

### <a name="input-register"></a>Registro di input

I registri di input (v ) sono ora completamente a virgola mobile e i registri delle coordinate della trama (t ) sono stati \# consolidati al suo [](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) \# interno. La [semantica dcl \_ (sm3 - ps asm)](dcl-usage---ps.md) all'inizio dello shader viene usata per descrivere il contenuto di un registro di input \_ specifico. Viene introdotta una semantica per i tipi di pixel (analoga al lato vertice) per questo modello. Non viene eseguito alcun blocco quando i registri di input sono definiti come colori (ad esempio le coordinate della trama). La valutazione dei registri definiti come colore differisce dalle coordinate della trama quando si esegue il multicampionamento.

### <a name="face-register"></a>Registro viso

Il registro dei visi (vFace) è una novità per questo modello. Si tratta di un registro scalare a virgola mobile che conterrà l'area primitiva. In ps \_ 3 \_ 0, tuttavia, è valido solo il segno di questo registro. Di conseguenza, se il valore è minore di zero (il bit di segno è impostato come negativo), la primitiva è la faccia posteriore (l'area è negativa, in senso antiorario). Pertanto, in ps 3 0 è opportuno confrontare solo questo registro con \_ \_ 0 (> 0 o < 0). All'pixel shader, l'applicazione può decidere quale tecnica di illuminazione usare. L'illuminazione a due lati può essere ottenuta in questo modo. Questo registro richiede una dichiarazione, quindi l'utilizzo non dichiarato verrà contrassegnato come errore. Per le linee e le primitive di punti, questo registro non è definito. Il registro dei visi può essere usato solo come condizione con le istruzioni seguenti: [setp \_ comp - ps](setp-comp---ps.md), if comp - [ \_ ps](if-comp---ps.md)o [break comp - \_ ps](break-comp---ps.md).

### <a name="loop-counter-register"></a>Registro contatori cicli

Loop [Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL) è una novità per questo modello. Viene incrementato automaticamente in ogni esecuzione del [blocco loop - ps](loop---ps.md) / [endloop - ps.](endloop---ps.md) Può essere usato nel blocco per l'indirizzamento relativo, se necessario. L'uso del registro dei contatori dei cicli all'esterno del ciclo non è valido.

### <a name="position-register"></a>Registro delle posizioni

Position Register (vPos) è una novità per questo modello. Contiene i pixel correnti (x, y) nei canali corrispondenti. I canali (z, w) non sono definiti. Questo registro richiede una dichiarazione, quindi l'utilizzo non dichiarato verrà contrassegnato come errore. Quando viene dichiarato, questo registro deve avere esattamente una delle maschere seguenti: .x, .y, .xy.

## <a name="input-register-types"></a>Tipi di registro di input



| Registrazione | Nome                                                                                      | Conteggio | L/S | \# Leggere le porte | \# Reads/inst | Dimensione | RelAddr | Valori predefiniti   | Richiede la DCL |
|----------|-------------------------------------------------------------------------------------------|-------|-----|---------------|---------------|-----------|---------|------------|--------------|
| v\#      | [Registro di input](dx9-graphics-reference-asm-ps-registers-input-color.md)                 | 10    | R   | 1             | Nessuna limitazione     | 4         | aL      | Nessuno       | Sì          |
| R\#      | [Registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md)               | 32    | L/S | 3             | Nessuna limitazione     | 4         | No      | nessuno       | No           |
| c\#      | [Registro float costante](dx9-graphics-reference-asm-ps-registers-constant-float.md)     | 224   | R   | 1             | Nessuna limitazione     | 4         | No      | 0000       | No           |
| Ho\#      | [Registro Di tipo Integer costante](dx9-graphics-reference-asm-ps-registers-constant-integer.md) | 16    | R   | 1             | 1             | 4         | No      | 0000       | No           |
| B\#      | [Registro booleano costante](dx9-graphics-reference-asm-ps-registers-constant-boolean.md) | 16    | R   | 1             | 1             | 1         | No      | FALSE      | No           |
| p0       | [Registro predicati](dx9-graphics-reference-asm-ps-registers-predicate.md)               | 1     | R   | 1             | 1             | 1         | No      | nessuno       | No           |
| s\#      | [Campionatore (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md)        | 16    | R   | 1             | 1             | 4         | No      | Vedere la nota 1 | Sì          |
| vFace    | Registro \_ viso                                                                            | 1     | R   | 1             | Nessuna limitazione     | 1         | No      | nessuno       | Sì          |
| vPos     | Registro \_ delle posizioni                                                                        | 1     | R   | 1             | Nessuna limitazione     | 4         | No      | nessuno       | Sì          |
| aL       | Registro \_ contatori \_ cicli                                                                   | 1     | R   | 1             | Nessuna limitazione     | 1         | n/d     | Nessuno       | No           |



 

Note:

-   I valori predefiniti per le ricerche del campionatore esistono, ma i valori dipendono dal formato della trama.

Il numero di readport è il numero di registri diversi (per ogni tipo di registro) che possono essere letti in una singola istruzione.

## <a name="output-register-types"></a>Tipi di registri di output



| Registrazione | Nome                                                                              | Conteggio                                                                             | L/S | Dimensione | RelAddr | Valori predefiniti | Richiede la DCL |
|----------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-----|-----------|---------|----------|--------------|
| Oc #     | [Output Color Register](dx9-graphics-reference-asm-ps-registers-output-color.md) | Vedere [Trame a più elementi (Direct3D 9)](/windows/desktop/direct3d9/multiple-element-textures) | W   | 4         | No      | nessuno     | No           |
| oDepth   | [Output Depth Register](dx9-graphics-reference-asm-ps-registers-output-depth.md) | 1                                                                                 | W   | 1         | No      | nessuno     | No           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 