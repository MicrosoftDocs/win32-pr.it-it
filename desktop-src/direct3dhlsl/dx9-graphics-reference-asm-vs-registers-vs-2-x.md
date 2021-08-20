---
title: Registri - vs_2_x
description: Questa sezione contiene informazioni di riferimento per i registri di input e output implementati dal vertex shader versione 2 \_ x.
ms.assetid: 35dfa3c8-be8e-4b2b-84c4-766850cf146c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4c5f75b9ff6961f6e4e80a9e98422ea88ac5521d74009d0a5062454a01c5cb22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118089962"
---
# <a name="registers---vs_2_x"></a>Registri - vs \_ 2 \_ x

Questa sezione contiene informazioni di riferimento per i registri di input e output implementati dal vertex shader versione 2 \_ x.

## <a name="input-registers"></a>Registri di input



| Registrazione | Nome                                                                                      | Conteggio      | L/S | \# Leggere le porte | \# Reads/inst | Dimensione | RelAddr | Valori predefiniti     | Richiede la DCL |
|----------|-------------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|-----------|---------|--------------|--------------|
| v\#      | [Registro di input](dx9-graphics-reference-asm-vs-registers-input.md)                       | 16         | R   | 1             | Nessuna limitazione       | 4         | No      | Vedere la nota 1   | Sì          |
| R\#      | [Registro temporaneo](dx9-graphics-reference-asm-vs-registers-temporary.md)               | Vedere la nota 2 | L/S | 3             | Nessuna limitazione       | 4         | No      | Nessuno         | No           |
| c\#      | [Registro float costante](dx9-graphics-reference-asm-vs-registers-constant-float.md)     | Vedere la nota 3 | R   | 1             | 2               | 4         | a0/aL | (0, 0, 0, 0) | No           |
| a0       | [Registro indirizzi](dx9-graphics-reference-asm-vs-registers-address.md)                   | 1          | L/S | 1             | 2               | 4         | No      | Nessuno         | No           |
| B\#      | [Registro booleano costante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) | 16         | R   | 1             | 1               | 1         | No      | FALSE        | No           |
| i\#      | [Registro di valori interi costanti](dx9-graphics-reference-asm-vs-registers-constant-integer.md) | 16         | R   | 1             | 1               | 4         | No      | (0, 0, 0, 0) | No           |
| aL       | [Registro contatori cicli](dx9-graphics-reference-asm-vs-registers-loop-counter.md)         | 1          | R   | 1             | 2               | 1         | No      | Nessuno         | No           |
| p0       | [Registro predicati](dx9-graphics-reference-asm-vs-registers-predicate.md)               | 1          | L/S | 1             | 1               | 4         | No      | Nessuno         | No           |



 

Note:

1.  Parziale (0, 0, 0, 1): se viene aggiornato solo un subset di canali, per impostazione predefinita i canali rimanenti saranno (0, 0, 0, 1).
2.  Uguale a D3DCAPS9. VS20Caps.NumTemps (almeno 12 per vs \_ 2 \_ x).
3.  Uguale a D3DCAPS9. MaxVertexShaderConst (almeno 256 per vs \_ 2 \_ x).

## <a name="output-registers"></a>Registri di output



| Registrazione | Nome                                                                                          | Conteggio | L/S | Dimensione | RelAddr | Valori predefiniti | Richiede la DCL |
|----------|-----------------------------------------------------------------------------------------------|-------|-----|-----------|---------|----------|--------------|
| Opos     | [Registro delle posizioni](dx9-graphics-reference-asm-vs-registers-position.md)                     | 1     | W   | 4         | No      | Nessuno     | No           |
| oFog     | [Register Disas](dx9-graphics-reference-asm-vs-registers-fog.md)                               | 1     | W   | 1         | No      | Nessuno     | No           |
| Opta     | [Registro dimensioni punto](dx9-graphics-reference-asm-vs-registers-point-size.md)                 | 1     | W   | 1         | No      | Nessuno     | No           |
| OD\#     | [Registro colori](dx9-graphics-reference-asm-vs-registers-color.md); Vedere la nota 1               | 2     | W   | 4         | No      | Nessuno     | No           |
| Ot\#     | [Registro delle coordinate della trama](dx9-graphics-reference-asm-vs-registers-texture-coordinate.md) | 8     | W   | 4         | No      | Nessuno     | No           |



 

Note:

-   oD0 è l'output a colori diffusi; oD1 è l'output del colore speculare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




