---
title: Registri - vs_1_1
description: Questa sezione contiene informazioni di riferimento per i registri di input e output implementati dal vertex shader versione 1 \_ 1.
ms.assetid: 8b19a0da-1561-450f-a36a-35ac7ea6e17a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4bcfadae2b1dca70298ffed188de2e6075892563b27bf6f624f2139e441600cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117908005"
---
# <a name="registers---vs_1_1"></a>Registri - vs \_ 1 \_ 1

Questa sezione contiene informazioni di riferimento per i registri di input e output implementati dal vertex shader versione 1 \_ 1.

## <a name="input-registers"></a>Registri di input



| Registrazione | Nome                                                                                  | Conteggio      | L/S | \# Leggere le porte | \# Reads/inst | Dimensione  | RelAddr | Valori predefiniti     | Richiede la DCL |
|----------|---------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|------------|---------|--------------|--------------|
| a0       | [Registro indirizzi](dx9-graphics-reference-asm-vs-registers-address.md)               | 1          | L/S | 1             | Nessuna limitazione       | Vedere la nota 3 | No      | Nessuno         | No           |
| c\#      | [Registro float costante](dx9-graphics-reference-asm-vs-registers-constant-float.md) | Vedere la nota 2 | R   | 1             | Nessuna limitazione       | 4          | a0.x    | (0, 0, 0, 0) | No           |
| Presso\#      | [Registro di input](dx9-graphics-reference-asm-vs-registers-input.md)                   | 16         | R   | 1             | Nessuna limitazione       | 4          | No      | Vedere la nota 1   | Sì          |
| R\#      | [Registro temporaneo](dx9-graphics-reference-asm-vs-registers-temporary.md)           | 12         | L/S | 3             | Nessuna limitazione       | 4          | No      | Nessuno         | No           |



 

Note:

1.  Parziale (0, 0, 0, 1): se viene aggiornato solo un subset di canali, per impostazione predefinita i canali rimanenti saranno (0, 0, 0, 1).
2.  Uguale a D3DCAPS9. MaxVertexShaderConst (almeno 96 per vs \_ 1 \_ 1).
3.  È disponibile solo il canale .x.

## <a name="output-registers"></a>Registri di output



| Registrazione | Nome                        | Conteggio | L/S | Dimensione | RelAddr | Valori predefiniti | Richiede la DCL |
|----------|-----------------------------|-------|-----|-----------|---------|----------|--------------|
| Opos     | Registro delle posizioni           | 1     | W   | 4         | No      | Nessuno     | No           |
| oFog     | Register Disas                | 1     | W   | 1         | No      | Nessuno     | No           |
| Opta     | Registro dimensioni punto         | 1     | W   | 1         | No      | Nessuno     | No           |
| OD\#     | Registro colori; Vedere la nota 1  | 2     | W   | 4         | No      | Nessuno     | No           |
| Ot\#     | Registro delle coordinate della trama | 8     | W   | 4         | No      | Nessuno     | No           |



 

Note:

-   oD0 è l'output a colori diffuso. oD1 è l'output del colore speculare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




