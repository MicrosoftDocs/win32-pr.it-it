---
title: Registri - vs_3_0
description: Questa sezione contiene informazioni di riferimento per i registri di input e output implementati dal vertex shader versione 3 \_ 0.
ms.assetid: af81f1c4-9c11-455e-a565-1b80f1ee8683
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d658d2d14d149d5d83d673269f2a414d7feaa22f13f1b32f57c4b80500fb1398
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673101"
---
# <a name="registers---vs_3_0"></a>Registri - vs \_ 3 \_ 0

Questa sezione contiene informazioni di riferimento per i registri di input e output implementati dal vertex shader versione 3 \_ 0.

## <a name="input-registers"></a>Registri di input



| Registrazione | Nome                                                                                      | Conteggio      | L/S | \# Leggere le porte | \# Reads/inst | Dimensione | RelAddr | Valori predefiniti     | Richiede la DCL |
|----------|-------------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|-----------|---------|--------------|--------------|
| v\#      | [Registro di input](dx9-graphics-reference-asm-vs-registers-input.md)                       | 16         | R   | 1             | Nessuna limitazione       | 4         | a0/aL   | Vedere la nota 1   | Sì          |
| R\#      | [Registro temporaneo](dx9-graphics-reference-asm-vs-registers-temporary.md)               | 32         | L/S | 3             | Nessuna limitazione       | 4         | No      | Nessuno         | No           |
| c\#      | [Registro float costante](dx9-graphics-reference-asm-vs-registers-constant-float.md)     | Vedere la nota 2 | R   | 1             | Nessuna limitazione       | 4         | a0/aL   | (0, 0, 0, 0) | No           |
| a0       | [Registro indirizzi](dx9-graphics-reference-asm-vs-registers-address.md)                   | 1          | L/S | 1             | Nessuna limitazione       | 4         | No      | Nessuno         | No           |
| B\#      | [Registro booleano costante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) | 16         | R   | 1             | 1               | 1         | No      | FALSE        | No           |
| i\#      | [Registro di valori interi costanti](dx9-graphics-reference-asm-vs-registers-constant-integer.md) | 16         | R   | 1             | 1               | 4         | No      | (0, 0, 0, 0) | No           |
| aL       | [Registro contatori cicli](dx9-graphics-reference-asm-vs-registers-loop-counter.md)         | 1          | R   | 1             | Nessuna limitazione       | 1         | No      | Nessuno         | No           |
| p0       | [Registro predicati](dx9-graphics-reference-asm-vs-registers-predicate.md)               | 1          | L/S | 1             | 1               | 4         | no      | Nessuno         | no           |
| s\#      | [Campionatore (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)        | 4          | R   | 1             | 1               | 4         | No      | Vedere la nota 3   | Sì          |



 

Note:

1.  Parziale (0, 0, 0, 1): se viene aggiornato solo un subset di canali, per impostazione predefinita i canali rimanenti saranno (0, 0, 0, 1).
2.  Uguale a D3DCAPS9. MaxVertexShaderConst (almeno 256 per vs \_ 3 \_ 0).
3.  I valori predefiniti per la ricerca del campionatore esistono, ma i valori dipendono dal formato della trama.

## <a name="output-registers"></a>Registri di output

I registri di output sono stati compressi in 12 o \# registri (output). Possono essere usati per qualsiasi elemento che l'utente vuole interpolare per il pixel shader: coordinate della trama, colori, nebbia e così via.



| Registrazione | Nome            | Conteggio | L/S | Dimensione | RelAddr | Valori predefiniti | Richiede L'elenco di controllo di accesso |
|----------|-----------------|-------|-----|-----------|---------|----------|--------------|
| o\#      | Registro di output | 12    | W   | 4         | aL      | Nessuno     | Sì          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




