---
title: Registri - ps_5_0
description: I registri di input e output seguenti vengono implementati nel pixel shader versione 5 \_ 0.
ms.assetid: F16E5CB8-E1DB-48CD-8C20-DBF1DF971110
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d432e53626d547bcaf421a4b4ffd9c2aa0f5d0a78ecc3aff9f0b87059c40c0ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095341"
---
# <a name="registers---ps_5_0"></a>Registri - ps \_ 5 \_ 0

I registri di input e output seguenti vengono implementati nel pixel shader versione 5 \_ 0.

## <a name="input-registers"></a>Registri di input



| Tipo di registrazione                                     | Conteggio              | L/S | Dimensione | Indicizzabile in base a r\# | Valori predefiniti | Richiede L'elenco di controllo di accesso |
|---------------------------------------------------|--------------------|-----|-----------|------------------|----------|--------------|
| Temp a 32 bit (r \# )                                 | 4096(r \# +x \# \[ n \] ) | L/S | 4         | No               | nessuno     | Sì          |
| Matrice temporanea indicizzabile a 32 bit (x \# \[ n \] )            | 4096(r \# +x \# \[ n \] ) | L/S | 4         | Sì              | Nessuno     | Sì          |
| Attributo di input a 32 bit (v \# )                      | 32                 | R   | 4         | Sì              | Nessuno     | Sì          |
| Elemento in una risorsa di input (t \# )                | 128                | R   | 1         | No               | nessuno     | Sì          |
| Campionatore \# (s)                                     | 16                 | R   | 1         | No               | nessuno     | Sì          |
| Informazioni di riferimento su ConstantBuffer (indice cb \# \[ \] )          | 15                 | R   | 4         | Sì(contenuto)    | Nessuno     | Sì          |
| Riferimento immediato a ConstantBuffer (indice icb \[ \] ) | 1                  | R   | 4         | Sì(contenuto)    | Nessuno     | Sì          |



 

## <a name="output-registers"></a>Registri di output



| Tipo di registrazione                                                      | Conteggio                   | L/S | Dimensione                                | Indicizzabile in base a r\# | Valori predefiniti | Richiede L'elenco di controllo di accesso |
|--------------------------------------------------------------------|-------------------------|-----|------------------------------------------|------------------|----------|--------------|
| NULL (risultato discard, utile per operazioni con più risultati) | N/A                     | W   | N/D                                      | N/D              | N/D      | No           |
| Elemento output a 32 bit (o \# )                                        | 8                       | W   | 4                                        | N/D              | N/D      | No           |
| Unordered Access View (u \# )                                        | 8 - \# di rendertarget | L/S | COMPONENTI DEL REGISTRO \_ \_ \_ UAV \_ DI D3D11 PS CS \_ | No               | No       | Sì          |
| \[0.0f a 32 bit. 1,0f \] float output depth (oDepth)                  | 1                       | W   | 1                                        | N/D              | N/D      | Sì          |
| Maschera di esempio di output UINT a 32 bit (oMask)                             | 1                       | W   | 1                                        | N/D              | N/D      | Sì          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




