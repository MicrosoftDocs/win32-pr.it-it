---
title: Registri-vs_3_0
description: Questa sezione contiene informazioni di riferimento per i registri di input e di output implementati da vertex shader versione 3 \_ 0.
ms.assetid: af81f1c4-9c11-455e-a565-1b80f1ee8683
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47353a3f312a2abbd6f4fe5ea1dcd1ed9495a9d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712775"
---
# <a name="registers---vs_3_0"></a>Registri-vs \_ 3 \_ 0

Questa sezione contiene informazioni di riferimento per i registri di input e di output implementati da vertex shader versione 3 \_ 0.

## <a name="input-registers"></a>Registri di input



| Registrazione | Nome                                                                                      | Conteggio      | L/S | \# Leggere le porte | \# Letture/Inst | Dimension | Relannr | Valori predefiniti     | Richiede DCL |
|----------|-------------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|-----------|---------|--------------|--------------|
| v\#      | [Registro di input](dx9-graphics-reference-asm-vs-registers-input.md)                       | 16         | R   | 1             | Nessuna limitazione       | 4         | a0/aL   | Vedere la nota 1   | Sì          |
| r\#      | [Registro temporaneo](dx9-graphics-reference-asm-vs-registers-temporary.md)               | 32         | L/S | 3             | Nessuna limitazione       | 4         | No      | nessuno         | No           |
| c\#      | [Registro float costante](dx9-graphics-reference-asm-vs-registers-constant-float.md)     | Vedere la nota 2 | R   | 1             | Nessuna limitazione       | 4         | a0/aL   | (0, 0, 0, 0) | No           |
| a0       | [Registro indirizzi](dx9-graphics-reference-asm-vs-registers-address.md)                   | 1          | L/S | 1             | Nessuna limitazione       | 4         | No      | nessuno         | No           |
| b\#      | [Registro booleano costante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) | 16         | R   | 1             | 1               | 1         | No      | FALSE        | No           |
| i\#      | [Registro Integer costante](dx9-graphics-reference-asm-vs-registers-constant-integer.md) | 16         | R   | 1             | 1               | 4         | No      | (0, 0, 0, 0) | No           |
| aL       | [Registro contatore cicli](dx9-graphics-reference-asm-vs-registers-loop-counter.md)         | 1          | R   | 1             | Nessuna limitazione       | 1         | No      | nessuno         | No           |
| P0       | [Registro predicato](dx9-graphics-reference-asm-vs-registers-predicate.md)               | 1          | L/S | 1             | 1               | 4         | no      | Nessuno         | no           |
| s\#      | [Campionatore (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)        | 4          | R   | 1             | 1               | 4         | No      | Vedere la nota 3   | Sì          |



 

Note:

1.  Partial (0, 0, 0, 1)-se viene aggiornato solo un subset di canali, i canali rimanenti saranno predefiniti (0, 0, 0, 1).
2.  Uguale a D3DCAPS9. MaxVertexShaderConst (almeno 256 per vs \_ 3 \_ 0).
3.  Le impostazioni predefinite per la ricerca del campionatore esistono, ma i valori dipendono dal formato di trama.

## <a name="output-registers"></a>Registri di output

I registri di output sono stati compressi in registri 12 o \# (output). Questi possono essere usati per qualsiasi elemento che l'utente vuole interpolare per il pixel shader: coordinate di trama, colori, nebbia e così via.



| Registrazione | Nome            | Conteggio | L/S | Dimension | Relannr | Valori predefiniti | Richiede DCL |
|----------|-----------------|-------|-----|-----------|---------|----------|--------------|
| o\#      | Registro di output | 12    | W   | 4         | aL      | nessuno     | Sì          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




