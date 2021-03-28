---
title: Registri-ps_5_0
description: I registri di input e di output seguenti sono implementati nella pixel shader versione 5 \_ 0.
ms.assetid: F16E5CB8-E1DB-48CD-8C20-DBF1DF971110
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d945e06ed3ae1847e15a32da973709b8ceb241ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955776"
---
# <a name="registers---ps_5_0"></a>Registri-PS \_ 5 \_ 0

I registri di input e di output seguenti sono implementati nella pixel shader versione 5 \_ 0.

## <a name="input-registers"></a>Registri di input



| Tipo di registro                                     | Conteggio              | L/S | Dimension | Indicizzabile da r\# | Valori predefiniti | Richiede DCL |
|---------------------------------------------------|--------------------|-----|-----------|------------------|----------|--------------|
| Temp a 32 bit (r \# )                                 | 4096 (r \# + x \# \[ n \] ) | L/S | 4         | No               | nessuno     | Sì          |
| Matrice Temp indicizzabile a 32 bit (x \# \[ n \] )            | 4096 (r \# + x \# \[ n \] ) | L/S | 4         | Sì              | nessuno     | Sì          |
| Attributo di input a 32 bit (v \# )                      | 32                 | R   | 4         | Sì              | nessuno     | Sì          |
| Elemento in una risorsa di input (t \# )                | 128                | R   | 1         | No               | nessuno     | Sì          |
| Campionatore/ \# i                                     | 16                 | R   | 1         | No               | nessuno     | Sì          |
| Guida di riferimento a ConstantBuffer ( \# \[ Indice CB \] )          | 15                 | R   | 4         | Sì (contenuto)    | nessuno     | Sì          |
| Riferimento ConstantBuffer immediato ( \[ Indice ICB \] ) | 1                  | R   | 4         | Sì (contenuto)    | nessuno     | Sì          |



 

## <a name="output-registers"></a>Registri di output



| Tipo di registro                                                      | Conteggio                   | L/S | Dimension                                | Indicizzabile da r\# | Valori predefiniti | Richiede DCL |
|--------------------------------------------------------------------|-------------------------|-----|------------------------------------------|------------------|----------|--------------|
| NULL (risultato di scarto, utile per operazioni con più risultati) | N/D                     | W   | N/D                                      | N/D              | N/D      | No           |
| Elemento output a 32 bit (o \# )                                        | 8                       | W   | 4                                        | N/D              | N/D      | No           |
| Unordered Access View (u \# )                                        | 8 \# Rendertargets | L/S | D3D11 \_ PS \_ cs \_ UAV \_ registro \_ componenti | No               | No       | Sì          |
| 32 bit \[ 0,0 f.. 1,0 f \] float Depth output (oDepth)                  | 1                       | W   | 1                                        | N/D              | N/D      | Sì          |
| maschera di esempio di output UINT a 32 bit (oMask)                             | 1                       | W   | 1                                        | N/D              | N/D      | Sì          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




