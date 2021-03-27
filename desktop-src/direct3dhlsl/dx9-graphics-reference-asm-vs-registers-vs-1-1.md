---
title: Registri-vs_1_1
description: Questa sezione contiene informazioni di riferimento per i registri di input e di output implementati da vertex shader versione 1 \_ .
ms.assetid: 8b19a0da-1561-450f-a36a-35ac7ea6e17a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e6776fef206f9ced0608e86cbf596585399d4a12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856578"
---
# <a name="registers---vs_1_1"></a>Registri-vs \_ 1 \_ 1

Questa sezione contiene informazioni di riferimento per i registri di input e di output implementati da vertex shader versione 1 \_ .

## <a name="input-registers"></a>Registri di input



| Registrazione | Nome                                                                                  | Conteggio      | L/S | \# Leggere le porte | \# Letture/Inst | Dimension  | Relannr | Valori predefiniti     | Richiede DCL |
|----------|---------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|------------|---------|--------------|--------------|
| a0       | [Registro indirizzi](dx9-graphics-reference-asm-vs-registers-address.md)               | 1          | L/S | 1             | Nessuna limitazione       | Vedere la nota 3 | No      | nessuno         | No           |
| c\#      | [Registro float costante](dx9-graphics-reference-asm-vs-registers-constant-float.md) | Vedere la nota 2 | R   | 1             | Nessuna limitazione       | 4          | a0. x    | (0, 0, 0, 0) | No           |
| v\#      | [Registro di input](dx9-graphics-reference-asm-vs-registers-input.md)                   | 16         | R   | 1             | Nessuna limitazione       | 4          | No      | Vedere la nota 1   | Sì          |
| r\#      | [Registro temporaneo](dx9-graphics-reference-asm-vs-registers-temporary.md)           | 12         | L/S | 3             | Nessuna limitazione       | 4          | No      | nessuno         | No           |



 

Note:

1.  Partial (0, 0, 0, 1)-se viene aggiornato solo un subset di canali, i canali rimanenti saranno predefiniti (0, 0, 0, 1).
2.  Uguale a D3DCAPS9. MaxVertexShaderConst (almeno 96 per Visual Studio \_ 1 \_ ).
3.  È disponibile solo il canale con estensione x.

## <a name="output-registers"></a>Registri di output



| Registrazione | Nome                        | Conteggio | L/S | Dimension | Relannr | Valori predefiniti | Richiede DCL |
|----------|-----------------------------|-------|-----|-----------|---------|----------|--------------|
| oPos     | Posizione registro           | 1     | W   | 4         | No      | nessuno     | No           |
| oFog     | Registro di nebbia                | 1     | W   | 1         | No      | nessuno     | No           |
| oPts     | Registro dimensioni punti         | 1     | W   | 1         | No      | nessuno     | No           |
| oD\#     | Registro colori; Vedere la nota 1  | 2     | W   | 4         | No      | nessuno     | No           |
| oT\#     | Registro coordinate trama | 8     | W   | 4         | No      | nessuno     | No           |



 

Note:

-   oD0 è l'output del colore diffuso; oD1 è l'output del colore speculare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




