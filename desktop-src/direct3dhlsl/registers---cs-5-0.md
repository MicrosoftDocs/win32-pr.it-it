---
title: Registri - cs_5_0
description: I registri di input e output seguenti vengono implementati nel compute shader versione 5 \_ 0.
ms.assetid: A602BA9F-0934-472F-BB07-5E7A97763CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01d761fba2b126559e18caf7cf917482d83fec952798b80c3ffc756a5bf3418
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023581"
---
# <a name="registers---cs_5_0"></a>Registri - cs \_ 5 \_ 0

I registri di input e output seguenti vengono implementati nel compute shader versione 5 \_ 0.

## <a name="input-registers"></a>Registri di input



| Tipo di registrazione                                        | Conteggio                                                  | L/S | Dimensione                        | Indicizzabile in base a r\# | Valori predefiniti | Richiede L'elenco di controllo di accesso |
|------------------------------------------------------|--------------------------------------------------------|-----|----------------------------------|------------------|----------|--------------|
| Temp a 32 bit (r \# )                                    | 4096(r \# +x \# \[ n \] )                                     | L/S | 4                                | No               | nessuno     | Sì          |
| Matrice temporanea indicizzabile a 32 bit (x \# \[ n \] )               | 4096(r \# +x \# \[ n \] )                                     | L/S | 4                                | Sì              | Nessuno     | Sì          |
| Memoria condivisa del gruppo di thread a 32 bit (g \# \[ n \] )         | 8192 (somma di tutti i decli di memoria condivisa per il gruppo di thread) | L/S | 1 (può essere dichiarato in diversi modi) | Sì              | Nessuno     | Sì          |
| Elemento in una risorsa di input (t \# )                   | 128                                                    | R   | 1                                | No               | nessuno     | Sì          |
| Campionatore \# (s)                                        | 16                                                     | R   | 1                                | No               | nessuno     | Sì          |
| Informazioni di riferimento su ConstantBuffer (indice cb \# \[ \] )             | 15                                                     | R   | 4                                | Sì (contenuto)   | Nessuno     | Sì          |
| Riferimento immediato a ConstantBuffer (indice icb \[ \] )    | 1                                                      | R   | 4                                | Sì(contenuto)    | Nessuno     | Sì          |
| ThreadID (vThreadID.xyz)                             | 1                                                      | R   | 3                                | No               | N/D      | Sì          |
| ThreadGroupID (vThreadGroupID.xyz)                   | 1                                                      | R   | 3                                | No               | N/D      | Sì          |
| ThreadIDInGroup (vThreadIDInGroup.xyz)               | 1                                                      | R   | 3                                | No               | N/D      | Sì          |
| ThreadIDInGroupFlattened (vThreadIDInGroupFlattened) | 1                                                      | R   | 1                                | No               | N/D      | Sì          |



 

## <a name="output-registers"></a>Registri di output



| Tipo di registrazione                                               | Conteggio | L/S | Dimensione | Indicizzabile in base a r\# | Valori predefiniti | Richiede L'elenco di controllo di accesso |
|-------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL (risultato discard, utile per operazioni con più risultati) | N/A   | W   | N/D       | N/D              | N/D      | No           |
| Unordered Access View (u \# )                                 | 8     | L/S | 1         | No               | No       | Sì          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




