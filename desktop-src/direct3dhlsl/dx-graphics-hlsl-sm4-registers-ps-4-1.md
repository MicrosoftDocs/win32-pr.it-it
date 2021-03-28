---
title: Registri-ps_4_1
description: Questa sezione contiene informazioni di riferimento per i registri di input e di output implementati da pixel shader versione 4 \_ 1.
ms.assetid: d3f3e264-569e-43a6-a06b-a512d36a7b53
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1cf70a24ad2fa7e77f7a5a90f6ec247179464f5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955468"
---
# <a name="registers---ps_4_1"></a>Registri-PS \_ 4 \_ 1

Questa sezione contiene informazioni di riferimento per i registri di input e di output implementati da pixel shader versione 4 \_ 1.

## <a name="input-registers"></a>Registri di input



| Registrazione      | Nome | Conteggio              | L/S | Dimension | Indicizzabile da r\# | Valori predefiniti | Richiede DCL |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| r\#           |      | 4096 (r \# + x \# \[ n \] ) | L/S | 4         | No               | nessuno     | Sì          |
| x \# \[ n\]      |      | 4096 (r \# + x \# \[ n \] ) | L/S | 4         | Sì              | nessuno     | Sì          |
| v\#           |      | 32                 | R   | 4         | Sì              | nessuno     | Sì          |
| t\#           |      | 128                | R   | 1         | No               | nessuno     | Sì          |
| s\#           |      | 16                 | R   | 1         | No               | nessuno     | Sì          |
| \# \[ Indice CB\] |      | 15                 | R   | 4         | Sì (contenuto)    | nessuno     | Sì          |
| \[Indice ICB\]  |      | 1                  | R   | 4         | Sì (contenuto)    | nessuno     | Sì          |



 

## <a name="output-registers"></a>Registri di output



| Registrazione | Nome             | Conteggio | L/S | Dimension | Indicizzabile da r\# | Valori predefiniti | Richiede DCL |
|----------|------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | Elimina risultato   | N/D   | W   | N/D       | N/D              | N/D      | No           |
| o\#      | Registro di output  | 8     | W   | N/D       | N/D              | 4        | No           |
| oDepth   | Profondità di output     | 1     | W   | N/D       | N/D              | 1        | N/D          |
| oMask    | Maschera MSAA di output | 1     | W   | N/D       | N/D              | 1        | N/D          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello Shader 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




