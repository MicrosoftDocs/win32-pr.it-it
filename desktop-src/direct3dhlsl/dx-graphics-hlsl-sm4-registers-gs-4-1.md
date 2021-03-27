---
title: Registri-gs_4_1
description: Questa sezione contiene informazioni di riferimento per i registri di input e di output implementati da Geometry shader versioni 4 \_ 0 e 4 \_ 1.
ms.assetid: 0312707D-11D0-45D0-9E8C-8BD2BC65352C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a01f200bd4183843b1cfd2892fde5da442ca8d36
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221616"
---
# <a name="registers---gs_4_1"></a>Registri-GS \_ 4 \_ 1

Questa sezione contiene informazioni di riferimento per i registri di input e di output implementati da Geometry shader versioni 4 \_ 0 e 4 \_ 1.

## <a name="input-registers"></a>Registri di input



| Registrazione                 | Nome | Conteggio              | L/S | Dimension        | Indicizzabile da r\# | Valori predefiniti | Richiede DCL |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| r\#                      |      | 4096 (r \# + x \# \[ n \] ) | L/S | 4                | No               | nessuno     | Sì          |
| x \# \[ n\]                 |      | 4096 (r \# + x \# \[ n \] ) | L/S | 4                | Sì              | nessuno     | Sì          |
| v ( \# \[ \] \[ elemento Vertex)\] |      | 32                 | R   | 4 (comp) \* 6 (Vert) | Sì              | nessuno     | Sì          |
| vprim                    |      | 1                  | R   | 1                | No               | nessuno     | Sì          |
| t\#                      |      | 128                | R   | 1                | No               | nessuno     | Sì          |
| s\#                      |      | 16                 | R   | 1                | No               | nessuno     | Sì          |
| \# \[ Indice CB\]            |      | 15                 | R   | 4                | Sì (contenuto)    | nessuno     | Sì          |
| \[Indice ICB\]             |      | 1                  | R   | 4                | Sì (contenuto)    | nessuno     | Sì          |



 

## <a name="output-registers"></a>Registri di output



| Registrazione | Nome            | Conteggio | L/S | Dimension | Indicizzabile da r\# | Valori predefiniti | Richiede DCL |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | Elimina risultato  | N/D   | W   | N/D       | N/D              | N/D      | No           |
| o\#      | Registro di output | 32    | W   | N/D       | N/D              | 4        | Sì          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello Shader 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




