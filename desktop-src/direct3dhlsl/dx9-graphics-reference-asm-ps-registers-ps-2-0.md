---
title: ps_2_0 registri
description: Questo articolo contiene informazioni di riferimento per i registri di input e output implementati pixel shader versione 2_0.
ms.assetid: 8002e3eb-b9d4-4ecb-a9e5-ae58a9e20ace
keywords:
- Registri - ps_2_0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b8e4300765f340b99da5d06b7651c4daaae4c97b043c6ceb5017aa43b2e2dcb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024151"
---
# <a name="ps_2_0-registers"></a>ps \_ 2 \_ 0 Registri

I pixel shader dipendono dai registri per ottenere i dati dei vertici, per l'output dei dati pixel, per contenere i risultati temporanei durante i calcoli e per identificare le fasi di campionamento delle trame. Esistono diversi tipi di registri, ognuno con una funzionalità univoca. Questa sezione contiene informazioni di riferimento per i registri di input e output implementati da pixel shader versione 2 \_ x.

## <a name="input-register-types"></a>Tipi di registro di input



| Registrazione | Nome                                                                                          | Conteggio      | L/S        | \# Leggere le porte | \# Reads/inst | Dimensione | RelAddr | Valori predefiniti                  | Richiede la DCL |
|----------|-----------------------------------------------------------------------------------------------|------------|------------|---------------|---------------|-----------|---------|---------------------------|--------------|
| v\#      | [Registro colori di input](dx9-graphics-reference-asm-ps-registers-input-color.md)               | 2          | R          | 1             | Nessuna limitazione     | 4         | N       | Partial(0001). Vedere la nota 4 | S            |
| R\#      | [Registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md)                   | Vedere la nota 1 | L/S        | 3             | Nessuna limitazione     | 4         | N       | Nessuno                      | N            |
| c\#      | [Registro float costante](dx9-graphics-reference-asm-ps-registers-constant-float.md)         | 32         | R          | 1             | 2             | 4         | N       | 0000                      | N            |
| i\#      | [Registro di valori interi costanti](dx9-graphics-reference-asm-ps-registers-constant-integer.md)     | 16         | Vedere la nota 2 | 1             | 1             | 4         | N       | 0000                      | N            |
| B\#      | [Registro booleano costante](dx9-graphics-reference-asm-ps-registers-constant-boolean.md)     | 16         | Vedere la nota 2 | 1             | 1             | 1         | N       | FALSE                     | N            |
| p0       | [Registro predicati](dx9-graphics-reference-asm-ps-registers-predicate.md)                   | 1          | Vedere la nota 2 | 1             | 1             | 1         | N       | Nessuno                      | S            |
| s\#      | [Campionatore (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md)            | 16         | Vedere la nota 3 | 1             | 1             | 4         | N       | Vedere la nota 5                | S            |
| T\#      | [Registro delle coordinate della trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) | 8          | R          | 1             | 1             | 4         | N       | Nessuno                      | S            |



 

Note:

1.  12 min/32 max: il numero di registri r è determinato da \# D3DPSHADERCAPS2 \_ 0.NumTemps (che varia da 12 a 32).
2.  Utilizzabile solo da un'istruzione di controllo del flusso.
3.  Utilizzabile solo da un'istruzione di campionamento della trama.
4.  partial(x, y, z, w): se nel registro viene aggiornato solo un subset di canali, i canali rimanenti verranno utilizzati per impostazione predefinita sui valori specificati (x, y, z, w).
5.  Le impostazioni predefinite per le ricerche del campionatore esistono, ma i valori dipendono dal formato della trama.

Il numero di readport è il numero di registri diversi (per ogni tipo di registro) che possono essere letti in una singola istruzione.

## <a name="output-register-types"></a>Tipi di registro di output



| Registrazione | Nome                                                                              | Conteggio                                                                             | L/S | Dimensione | RelAddr | Valori predefiniti | Richiede L'elenco di controllo di accesso |
|----------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-----|-----------|---------|----------|--------------|
| Oc #     | [Registro colori di output](dx9-graphics-reference-asm-ps-registers-output-color.md) | Vedere [Trame a più elementi (Direct3D 9)](/windows/desktop/direct3d9/multiple-element-textures) | W   | 4         | N       | Nessuno     | N            |
| oDepth   | [Registro di profondità dell'output](dx9-graphics-reference-asm-ps-registers-output-depth.md) | 1                                                                                 | W   | 1         | N       | Nessuno     | N            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 