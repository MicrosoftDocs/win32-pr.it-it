---
title: Registri ps_2_x
description: I pixel shader dipendono dai registri per ottenere i dati dei vertici, per l'output dei dati in pixel, per conservare i risultati temporanei durante i calcoli e per identificare le fasi di campionamento della trama.
ms.assetid: 52bb6290-46e2-4d7d-9b96-b4c3e2abfe43
keywords:
- Registri-ps_2_x
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 880c897aa3d812d1e94e5dc408e97ec18b5de106
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976682"
---
# <a name="ps_2_x-registers"></a>\_registri PS 2 \_ x

I pixel shader dipendono dai registri per ottenere i dati dei vertici, per l'output dei dati in pixel, per conservare i risultati temporanei durante i calcoli e per identificare le fasi di campionamento della trama. Sono disponibili diversi tipi di registri, ognuno con una funzionalità univoca. Questa sezione contiene informazioni di riferimento per i registri di input e di output implementati da pixel shader versione 2 \_ x.

## <a name="input-register-types"></a>Tipi di registro di input



| Registrazione | Nome                                                                                          | Conteggio      | L/S        | \# Leggere le porte | \# Letture/Inst | Dimension | Relannr | Valori predefiniti                  | Richiede DCL |
|----------|-----------------------------------------------------------------------------------------------|------------|------------|---------------|---------------|-----------|---------|---------------------------|--------------|
| v\#      | [Registro colori di input](dx9-graphics-reference-asm-ps-registers-input-color.md)               | 2          | R          | 1             | Nessuna limitazione     | 4         | N       | Partial (0001). Vedere la nota 4 | S            |
| r\#      | [Registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md)                   | Vedere la nota 1 | L/S        | 3             | Nessuna limitazione     | 4         | N       | nessuno                      | N            |
| c\#      | [Registro float costante](dx9-graphics-reference-asm-ps-registers-constant-float.md)         | 32         | R          | 1             | 2             | 4         | N       | 0000                      | N            |
| i\#      | [Registro Integer costante](dx9-graphics-reference-asm-ps-registers-constant-integer.md)     | 16         | Vedere la nota 2 | 1             | 1             | 4         | N       | 0000                      | N            |
| b\#      | [Registro booleano costante](dx9-graphics-reference-asm-ps-registers-constant-boolean.md)     | 16         | Vedere la nota 2 | 1             | 1             | 1         | N       | FALSE                     | N            |
| P0       | [Registro predicato](dx9-graphics-reference-asm-ps-registers-predicate.md)                   | 1          | Vedere la nota 2 | 1             | 1             | 1         | N       | nessuno                      | S            |
| s\#      | [Campionatore (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md)            | 16         | Vedere la nota 3 | 1             | 1             | 4         | N       | Vedere la nota 5                | S            |
| t\#      | [Registro coordinate trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) | 8          | R          | 1             | 1             | 4         | N       | nessuno                      | S            |



 

Note:

1.  12 min/32 max: il numero di \# registri r è determinato da D3DPSHADERCAPS2 \_ 0. NumTemps (compreso tra 12 e 32).
2.  Utilizzabile solo da un'istruzione di controllo di flusso.
3.  Utilizzabile solo da un'istruzione di campionamento di trama.
4.  Partial (x, y, z, w)-se nel registro viene aggiornato solo un subset di canali, i canali rimanenti utilizzeranno per impostazione predefinita i valori specificati (x, y, z, w).
5.  Sono disponibili impostazioni predefinite per le ricerche del campionatore, ma i valori dipendono dal formato di trama.

Il numero di readports è il numero di registri diversi (per ogni tipo di registro) che possono essere letti in un'unica istruzione.

## <a name="output-register-types"></a>Tipi di registro di output



| Registrazione | Nome                                                                              | Conteggio                                                                             | L/S | Dimension | Relannr | Valori predefiniti | Richiede DCL |
|----------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-----|-----------|---------|----------|--------------|
| oC #     | [Registro colori di output](dx9-graphics-reference-asm-ps-registers-output-color.md) | Vedere [trame a più elementi (Direct3D 9)](/windows/desktop/direct3d9/multiple-element-textures) | W   | 4         | N       | nessuno     | N            |
| oDepth   | [Registro profondità output](dx9-graphics-reference-asm-ps-registers-output-depth.md) | 1                                                                                 | W   | 1         | N       | nessuno     | N            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 