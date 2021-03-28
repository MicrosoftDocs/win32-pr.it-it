---
title: Registri-vs_5_0
description: I registri di input e di output seguenti vengono implementati in vertex shader versione 5 \_ 0.
ms.assetid: 475753C7-C055-4DB7-9DC3-6C734413A92B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1dc211f5f3dd8819577c796849dcb86012cc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104976135"
---
# <a name="registers---vs_5_0"></a>Registri-vs \_ 5 \_ 0

I registri di input e di output seguenti vengono implementati in vertex shader versione 5 \_ 0.

## <a name="input-registers"></a>Registri di input



| Tipo di registro                                      | Conteggio              | L/S | Dimension | Indicizzabile da r\# | Valori predefiniti | Richiede DCL |
|----------------------------------------------------|--------------------|-----|-----------|------------------|----------|--------------|
| Temp a 32 bit (r \# )                                  | 4096 (r \# + x \# \[ n \] ) | L/S | 4         | No               | nessuno     | Sì          |
| Matrice Temp indicizzabile a 32 bit (x \# \[ n \] )             | 4096 (r \# + x \# \[ n \] ) | L/S | 4         | Sì              | nessuno     | Sì          |
| input a 32 bit (v \# )                                 | 32                 | R   | 4         | Sì              | nessuno     | Sì          |
| Elemento in una risorsa di input (t \# )                 | 128                | R   | 1         | No               | nessuno     | Sì          |
| Campionatore/ \# i                                      | 16                 | R   | 1         | No               | nessuno     | Sì          |
| Guida di riferimento a ConstantBuffer ( \# \[ Indice CB \] )           | 15                 | R   | 4         | Sì (contenuto)    | nessuno     | Sì          |
| Guida di riferimento a iImmediate ConstantBuffer ( \[ Indice ICB \] ) | 1                  | R   | 4         | Sì (contenuto)    | nessuno     | Sì          |



 

## <a name="output-registers"></a>Registri di output



| Tipo di registro                                                      | Conteggio | L/S | Dimension | Indicizzabile da r\# | Valori predefiniti | Richiede DCL |
|--------------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL (risultato di scarto, utile per operazioni con più risultati) | N/D   | W   | N/D       | N/D              | N/D      | No           |
| Elemento dati vertex di output a 32 bit (o \# )                            | 32    | W   | 4         | N/D              | N/D      | Sì          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




