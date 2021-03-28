---
title: Registri-gs_5_0
description: I registri di input e di output seguenti vengono implementati in Geometry shader versione 5 \_ 0.
ms.assetid: 9E99F584-611F-4CFC-B69A-66F2B4545D36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 282b32dd1c8fcb327c273b0fbf3aa51bdb002c2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332012"
---
# <a name="registers---gs_5_0"></a>Registri-GS \_ 5 \_ 0

I registri di input e di output seguenti vengono implementati in Geometry shader versione 5 \_ 0.

## <a name="input-registers"></a>Registri di input



| Tipo di registro                                     | Conteggio              | L/S | Dimension         | Indicizzabile da r\# | Valori predefiniti | Richiede DCL |
|---------------------------------------------------|--------------------|-----|-------------------|------------------|----------|--------------|
| Temp a 32 bit (r \# )                                 | 4096 (r \# + x \# \[ n \] ) | L/S | 4                 | No               | nessuno     | Sì          |
| Matrice Temp indicizzabile a 32 bit (x \# \[ n \] )            | 4096 (r \# + x \# \[ n \] ) | L/S | 4                 | Sì              | nessuno     | Sì          |
| Input a 32 bit ( \[ elemento vertice v \] \[ \] )             | 32                 | R   | 4 (comp) \* 32 (Vert) | Sì              | nessuno     | Sì          |
| ID primitiva input a 32 bit (vPrim)                 | 1                  | R   | 1                 | No               | nessuno     | Sì          |
| ID istanza di input a 32 bit (vInstanceID)            | 1                  | R   | 1                 | No               | nessuno     | Sì          |
| Elemento in una risorsa di input (t \# )                | 128                | R   | 1                 | No               | nessuno     | Sì          |
| Campionatore/ \# i                                     | 16                 | R   | 1                 | No               | nessuno     | Sì          |
| Guida di riferimento a ConstantBuffer ( \# \[ Indice CB \] )          | 15                 | R   | 4                 | Sì (contenuto)    | nessuno     | Sì          |
| Riferimento ConstantBuffer immediato ( \[ Indice ICB \] ) | 1                  | R   | 4                 | Sì (contenuto)    | nessuno     | Sì          |



 

## <a name="output-registers"></a>Registri di output



| Tipo di registro                                               | Conteggio | L/S | Dimension | Indicizzabile da r\# | Valori predefiniti | Richiede DCL |
|-------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL (risultato di scarto, utile per operazioni con più risultati) | N/D   | W   | N/D       | N/D              | N/D      | No           |
| Elemento dati vertex di output a 32 bit (o \# )                     | 32    | W   | N/D       | N/D              | 4        | Sì          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




