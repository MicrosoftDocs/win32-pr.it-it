---
title: Registri ps_3_0
description: I pixel shader dipendono dai registri per ottenere i dati dei vertici, per l'output dei dati in pixel, per conservare i risultati temporanei durante i calcoli e per identificare le fasi di campionamento della trama.
ms.assetid: 01bee50a-c1b7-4b15-9df8-1dd52d9ff163
keywords:
- vPos
- Posizione registro, pixel shader
- Registri-ps_3_0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ef4eef435857968246ab0413841ef072b5391a5e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399175"
---
# <a name="ps_3_0-registers"></a>\_registri PS 3 \_ 0

I pixel shader dipendono dai registri per ottenere i dati dei vertici, per l'output dei dati in pixel, per conservare i risultati temporanei durante i calcoli e per identificare le fasi di campionamento della trama. Sono disponibili diversi tipi di registri, ognuno con una funzionalità univoca. Questa sezione contiene informazioni di riferimento per i registri di input e di output implementati da pixel shader versione 3 \_ 0.

## <a name="new-registers"></a>Nuovi registri

### <a name="input-register"></a>Registro di input

I registri di input (v \# ) sono ora completamente a virgola mobile e il [registro delle coordinate di trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)s (t) è \# stato consolidato al suo interno. La [ \_ semantica DCL (SM3-PS ASM)](dcl-usage---ps.md) nella parte superiore dello shader viene usata per descrivere ciò che è conforme in un particolare Registro di input \_ . Per questo modello viene introdotta una semantica per i tipi di pixel (analogo al lato vertice). Quando i registri di input sono definiti come colori (ad esempio coordinate di trama), non viene eseguita alcuna operazione di bloccaggio. La valutazione dei registri definiti come colore è diversa dalle coordinate di trama durante il campionamento multiplo.

### <a name="face-register"></a>Registro viso

Il registro visi (vFace) è una novità di questo modello. Si tratta di un registro scalare a virgola mobile che conterrà infine l'area primitiva. In PS \_ 3 \_ 0, tuttavia, solo il segno di questo registro è valido. Di conseguenza, se il valore è minore di zero (il bit del segno è impostato su negativo) la primitiva è la faccia posteriore (l'area è negativa, in senso antiorario). Pertanto, in PS \_ 3 \_ 0 è opportuno confrontare il registro con 0 (> 0 o < 0). All'interno del pixel shader, l'applicazione può prendere una decisione relativa alla tecnica di illuminazione da usare. In questo modo, è possibile ottenere l'illuminazione a due lati. Questo registro richiede una dichiarazione, quindi l'utilizzo non dichiarato verrà contrassegnato come un errore. Per le primitive di linee e punti, questo registro non è definito. Il registro viso può essere usato solo come condizione con le istruzioni seguenti: [setp \_ comp-PS](setp-comp---ps.md), [if \_ comp-PS](if-comp---ps.md)o [break \_ comp-PS](break-comp---ps.md).

### <a name="loop-counter-register"></a>Registro contatore cicli

Il [registro del contatore di cicli](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al) è nuovo per questo modello. Viene incrementato automaticamente in ogni esecuzione del blocco [loop-PS](loop---ps.md) / [EndLoop-PS](endloop---ps.md) . Può essere usato nel blocco per l'indirizzamento relativo, se necessario. Non è possibile usare la registrazione del contatore di cicli all'esterno del ciclo.

### <a name="position-register"></a>Posizione registro

Il registro di posizione (vPos) è una novità per questo modello. Contiene i pixel correnti (x, y) nei canali corrispondenti. I canali (z, w) non sono definiti. Questo registro richiede una dichiarazione, quindi l'utilizzo non dichiarato verrà contrassegnato come un errore. Quando viene dichiarata, questo registro deve avere esattamente una delle maschere seguenti:. x,. y,. XY.

## <a name="input-register-types"></a>Tipi di registro di input



| Registrazione | Nome                                                                                      | Conteggio | L/S | \# Leggere le porte | \# Letture/Inst | Dimension | Relannr | Valori predefiniti   | Richiede DCL |
|----------|-------------------------------------------------------------------------------------------|-------|-----|---------------|---------------|-----------|---------|------------|--------------|
| v\#      | [Registro di input](dx9-graphics-reference-asm-ps-registers-input-color.md)                 | 10    | R   | 1             | Nessuna limitazione     | 4         | aL      | nessuno       | Sì          |
| r\#      | [Registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md)               | 32    | L/S | 3             | Nessuna limitazione     | 4         | No      | nessuno       | No           |
| c\#      | [Registro float costante](dx9-graphics-reference-asm-ps-registers-constant-float.md)     | 224   | R   | 1             | Nessuna limitazione     | 4         | No      | 0000       | No           |
| i\#      | [Registro Integer costante](dx9-graphics-reference-asm-ps-registers-constant-integer.md) | 16    | R   | 1             | 1             | 4         | No      | 0000       | No           |
| b\#      | [Registro booleano costante](dx9-graphics-reference-asm-ps-registers-constant-boolean.md) | 16    | R   | 1             | 1             | 1         | No      | FALSE      | No           |
| P0       | [Registro predicato](dx9-graphics-reference-asm-ps-registers-predicate.md)               | 1     | R   | 1             | 1             | 1         | No      | nessuno       | No           |
| s\#      | [Campionatore (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md)        | 16    | R   | 1             | 1             | 4         | No      | Vedere la nota 1 | Sì          |
| vFace    | \_Registro viso                                                                            | 1     | R   | 1             | Nessuna limitazione     | 1         | No      | nessuno       | Sì          |
| vPos     | Posizione \_ Registro                                                                        | 1     | R   | 1             | Nessuna limitazione     | 4         | No      | nessuno       | Sì          |
| aL       | \_Registro contatore \_ cicli                                                                   | 1     | R   | 1             | Nessuna limitazione     | 1         | n/d     | nessuno       | No           |



 

Note:

-   Sono disponibili impostazioni predefinite per le ricerche del campionatore, ma i valori dipendono dal formato di trama.

Il numero di readports è il numero di registri diversi (per ogni tipo di registro) che possono essere letti in un'unica istruzione.

## <a name="output-register-types"></a>Tipi di registro di output



| Registrazione | Nome                                                                              | Conteggio                                                                             | L/S | Dimension | Relannr | Valori predefiniti | Richiede DCL |
|----------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-----|-----------|---------|----------|--------------|
| oC #     | [Registro colori di output](dx9-graphics-reference-asm-ps-registers-output-color.md) | Vedere [trame a più elementi (Direct3D 9)](/windows/desktop/direct3d9/multiple-element-textures) | W   | 4         | No      | nessuno     | No           |
| oDepth   | [Registro profondità output](dx9-graphics-reference-asm-ps-registers-output-depth.md) | 1                                                                                 | W   | 1         | No      | nessuno     | No           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 