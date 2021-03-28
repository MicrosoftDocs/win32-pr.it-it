---
title: Registri-ds_5_0
description: I registri di input e di output seguenti vengono implementati nel Domain shader versione 5 \_ 0.
ms.assetid: 8AE00EC6-0BDC-4F63-B95C-FF434B98D7CE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b787f4a1f7e647a49340d49796dc2986e442178f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332015"
---
# <a name="registers---ds_5_0"></a>Registri-DS \_ 5 \_ 0

I registri di input e di output seguenti vengono implementati nel Domain shader versione 5 \_ 0.

## <a name="input-registers"></a>Registri di input



| Tipo di registro                                              | Conteggio                | L/S | Dimension                           | Indicizzabile da r\# | Valori predefiniti | Richiede DCL |
|------------------------------------------------------------|----------------------|-----|-------------------------------------|------------------|----------|--------------|
| Temp a 32 bit (r \# )                                          | 4096 (r \# + x \# \[ n \] )   | L/S | 4                                   | No               | nessuno     | Sì          |
| Matrice Temp indicizzabile a 32 bit (x \# \[ n \] )                     | 4096 (r \# + x \# \[ n \] )   | L/S | 4                                   | Sì              | nessuno     | Sì          |
| Punti di controllo di input a 32 bit ( \[ elemento vertice VCP \] \[ \] )     | 32 vedere la nota 1 di seguito. | R   | 4 (componente) \* 32 (elemento) \* 32 (Vert) | Sì              | nessuno     | Sì          |
| Costanti patch di input a 32 bit ( \[ vertice VPC \] )               | 32 vedere la nota 2 di seguito. | R   | 4                                   | Sì              | nessuno     | Sì          |
| percorso di input a 32 bit nel dominio (vDomain. XY, vDomain.xyz)) | 1                    | R   | 3                                   | No               | N/D      | Sì          |
| PrimitiveID input UINT a 32 bit (vPrim)                      | 1                    | R   | 1                                   | No               | N/D      | Sì          |
| Elemento in una risorsa di input (t \# )                         | 128                  | R   | 128                                 | Sì              | nessuno     | Sì          |
| Campionatore/ \# i                                              | 16                   | R   | 1                                   | Sì              | nessuno     | Sì          |
| Guida di riferimento a iConstantBuffer ( \# \[ Indice CB \] )                  | 15                   | R   | 4                                   | Sì              | nessuno     | Sì          |
| Guida di riferimento a iImmediate ConstantBuffer ( \[ Indice ICB \] )         | 1                    | R   | 4                                   | Sì (contenuto)    | nessuno     | Sì          |



 

**Nota 1:** Il Domain shader Visualizza gli output dello scafo shader in 2 Set distinti di registri. I registri VCP possono visualizzare tutti i punti di controllo di output di Hull shader. I registri VPC possono visualizzare tutti i dati di output della costante patch di Hull shader.

**Nota 2:** Poiché il codice per le fasi di fork o join costanti della patch di Hull shader TessFactors usando nomi come SV \_ TessFactor, il Domain shader deve corrispondere a tali dichiarazioni sull'input VPC equivalente se desidera visualizzare tali valori.

## <a name="output-registers"></a>Registri di output



| Tipo di registro                           | Conteggio | L/S | Dimension | Indicizzabile da r\# | Valori predefiniti | Richiede DCL |
|-----------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| Elemento dati vertex di output a 32 bit (o \# ) | 32    | W   | 4         | Sì              | nessuno     | Sì          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




