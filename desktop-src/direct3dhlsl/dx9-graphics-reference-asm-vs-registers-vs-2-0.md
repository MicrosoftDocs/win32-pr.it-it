---
title: Registri-vs_2_0
description: Questa sezione contiene informazioni di riferimento per i registri di input e di output implementati da vertex shader versione 2 \_ 0.
ms.assetid: e5ef015e-1e4d-41b3-95da-3b44ef0bd73e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 156367ec08a5f1ecd94181be56558f4ba07005b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044561"
---
# <a name="registers---vs_2_0"></a>Registri-vs \_ 2 \_ 0

Questa sezione contiene informazioni di riferimento per i registri di input e di output implementati da vertex shader versione 2 \_ 0.

## <a name="input-registers"></a>Registri di input



| Registrazione | Nome                                                                                      | Conteggio      | L/S | \# Leggere le porte | \# Letture/Inst | Dimension | Relannr | Valori predefiniti     | Richiede DCL |
|----------|-------------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|-----------|---------|--------------|--------------|
| v\#      | [Registro di input](dx9-graphics-reference-asm-vs-registers-input.md)                       | 16         | R   | 1             | Nessuna limitazione       | 4         | No      | Vedere la nota 1   | Sì          |
| r\#      | [Registro temporaneo](dx9-graphics-reference-asm-vs-registers-temporary.md)               | 12         | L/S | 3             | Nessuna limitazione       | 4         | No      | nessuno         | No           |
| c\#      | [Registro float costante](dx9-graphics-reference-asm-vs-registers-constant-float.md)     | Vedere la nota 2 | R   | 1             | 2               | 4         | a0/aL | (0, 0, 0, 0) | No           |
| a0       | [Registro indirizzi](dx9-graphics-reference-asm-vs-registers-address.md)                   | 1          | L/S | 1             | 2               | 4         | No      | nessuno         | No           |
| b\#      | [Registro booleano costante](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) | 16         | R   | 1             | 1               | 1         | No      | FALSE        | No           |
| i\#      | [Registro Integer costante](dx9-graphics-reference-asm-vs-registers-constant-integer.md) | 16         | R   | 1             | 1               | 4         | No      | (0, 0, 0, 0) | No           |
| aL       | [Registro contatore cicli](dx9-graphics-reference-asm-vs-registers-loop-counter.md)         | 1          | R   | 1             | 2               | 1         | No      | nessuno         | No           |



 

Note:

1.  Partial (0, 0, 0, 1)-se viene aggiornato solo un subset di canali, i canali rimanenti saranno predefiniti (0, 0, 0, 1).
2.  Uguale a D3DCAPS9. MaxVertexShaderConst (almeno 256 per vs \_ 2 \_ 0).

## <a name="output-registers"></a>Registri di output



| Registrazione | Nome                                                                                          | Conteggio | L/S | Dimension | Relannr | Valori predefiniti | Richiede DCL |
|----------|-----------------------------------------------------------------------------------------------|-------|-----|-----------|---------|----------|--------------|
| oPos     | [Posizione registro](dx9-graphics-reference-asm-vs-registers-position.md)                     | 1     | W   | 4         | No      | nessuno     | No           |
| oFog     | [Registro di nebbia](dx9-graphics-reference-asm-vs-registers-fog.md)                               | 1     | W   | 1         | No      | nessuno     | No           |
| oPts     | [Registro dimensioni punti](dx9-graphics-reference-asm-vs-registers-point-size.md)                 | 1     | W   | 1         | No      | nessuno     | No           |
| oD\#     | [Registro colori](dx9-graphics-reference-asm-vs-registers-color.md); Vedere la nota 1               | 2     | W   | 4         | No      | nessuno     | No           |
| oT\#     | [Registro coordinate trama](dx9-graphics-reference-asm-vs-registers-texture-coordinate.md) | 8     | W   | 4         | No      | nessuno     | No           |



 

Note:

-   oD0 è l'output del colore diffuso; oD1 è l'output del colore speculare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




