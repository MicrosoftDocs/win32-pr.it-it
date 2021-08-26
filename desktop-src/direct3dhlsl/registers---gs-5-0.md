---
title: Registri - gs_5_0
description: I registri di input e output seguenti vengono implementati nella versione geometry shader 5 \_ 0.
ms.assetid: 9E99F584-611F-4CFC-B69A-66F2B4545D36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e0bac8baf9be8428b53fa7949229361edf04132079a7a6ca6989dab92c44aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023501"
---
# <a name="registers---gs_5_0"></a>Registri - gs \_ 5 \_ 0

I registri di input e output seguenti vengono implementati nella versione geometry shader 5 \_ 0.

## <a name="input-registers"></a>Registri di input



| Tipo di registro                                     | Conteggio              | L/S | Dimensione         | Indicizzabile in base a r\# | Valori predefiniti | Richiede la DCL |
|---------------------------------------------------|--------------------|-----|-------------------|------------------|----------|--------------|
| Temp a 32 bit (r \# )                                 | 4096(r \# +x \# \[ n \] ) | L/S | 4                 | No               | nessuno     | Sì          |
| Matrice temporanea indicizzabile a 32 bit (x \# \[ n \] )            | 4096(r \# +x \# \[ n \] ) | L/S | 4                 | Sì              | Nessuno     | Sì          |
| Input a 32 bit (elemento \[ vertice \] \[ v \] )             | 32                 | R   | 4(comp) \* 32(vert) | Sì              | Nessuno     | Sì          |
| ID primitivo di input a 32 bit (vPrim)                 | 1                  | R   | 1                 | No               | nessuno     | Sì          |
| ID istanza di input a 32 bit (vInstanceID)            | 1                  | R   | 1                 | No               | nessuno     | Sì          |
| Elemento in una risorsa di input (t \# )                | 128                | R   | 1                 | No               | nessuno     | Sì          |
| Campionatore (s \# )                                     | 16                 | R   | 1                 | No               | nessuno     | Sì          |
| Riferimento ConstantBuffer (indice cb \# \[ \] )          | 15                 | R   | 4                 | Sì (contenuto)    | Nessuno     | Sì          |
| Riferimento ConstantBuffer immediato (indice icb \[ \] ) | 1                  | R   | 4                 | Sì (contenuto)    | Nessuno     | Sì          |



 

## <a name="output-registers"></a>Registri di output



| Tipo di registro                                               | Conteggio | L/S | Dimensione | Indicizzabile in base a r\# | Valori predefiniti | Richiede la DCL |
|-------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL (risultato discard, utile per operazioni con più risultati) | N/A   | W   | N/D       | N/D              | N/D      | No           |
| Elemento dati vertice di output a 32 bit (o \# )                     | 32    | W   | N/D       | N/D              | 4        | Sì          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




