---
title: Registri-cs_5_0
description: I registri di input e di output seguenti sono implementati in compute shader versione 5 \_ 0.
ms.assetid: A602BA9F-0934-472F-BB07-5E7A97763CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be9a1164a1b3b4d623ced8453bbee50f561d4666
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396707"
---
# <a name="registers---cs_5_0"></a>Registri-CS \_ 5 \_ 0

I registri di input e di output seguenti sono implementati in compute shader versione 5 \_ 0.

## <a name="input-registers"></a>Registri di input



| Tipo di registro                                        | Conteggio                                                  | L/S | Dimension                        | Indicizzabile da r\# | Valori predefiniti | Richiede DCL |
|------------------------------------------------------|--------------------------------------------------------|-----|----------------------------------|------------------|----------|--------------|
| Temp a 32 bit (r \# )                                    | 4096 (r \# + x \# \[ n \] )                                     | L/S | 4                                | No               | nessuno     | Sì          |
| Matrice Temp indicizzabile a 32 bit (x \# \[ n \] )               | 4096 (r \# + x \# \[ n \] )                                     | L/S | 4                                | Sì              | nessuno     | Sì          |
| Memoria condivisa del gruppo di thread a 32 bit (g \# \[ n \] )         | 8192 (somma di tutti i decls di memoria condivisa per il gruppo di thread) | L/S | 1 (può essere dichiarata in diversi modi) | Sì              | nessuno     | Sì          |
| Elemento in una risorsa di input (t \# )                   | 128                                                    | R   | 1                                | No               | nessuno     | Sì          |
| Campionatore/ \# i                                        | 16                                                     | R   | 1                                | No               | nessuno     | Sì          |
| Guida di riferimento a ConstantBuffer ( \# \[ Indice CB \] )             | 15                                                     | R   | 4                                | Sì (contenuto)   | nessuno     | Sì          |
| Riferimento ConstantBuffer immediato ( \[ Indice ICB \] )    | 1                                                      | R   | 4                                | Sì (contenuto)    | nessuno     | Sì          |
| ThreadID (vThreadID.xyz)                             | 1                                                      | R   | 3                                | No               | N/D      | Sì          |
| ThreadGroupID (vThreadGroupID.xyz)                   | 1                                                      | R   | 3                                | No               | N/D      | Sì          |
| ThreadIDInGroup (vThreadIDInGroup.xyz)               | 1                                                      | R   | 3                                | No               | N/D      | Sì          |
| ThreadIDInGroupFlattened (vThreadIDInGroupFlattened) | 1                                                      | R   | 1                                | No               | N/D      | Sì          |



 

## <a name="output-registers"></a>Registri di output



| Tipo di registro                                               | Conteggio | L/S | Dimension | Indicizzabile da r\# | Valori predefiniti | Richiede DCL |
|-------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL (risultato di scarto, utile per operazioni con più risultati) | N/D   | W   | N/D       | N/D              | N/D      | No           |
| Unordered Access View (u \# )                                 | 8     | L/S | 1         | No               | No       | Sì          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




