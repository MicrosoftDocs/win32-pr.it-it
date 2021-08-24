---
title: Registri - vs_5_0
description: I registri di input e output seguenti vengono implementati nel vertex shader versione 5 \_ 0.
ms.assetid: 475753C7-C055-4DB7-9DC3-6C734413A92B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f9c80125a4640e558872e29e435d48e7420bbd6c504577a5e0c84781f8a47d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853901"
---
# <a name="registers---vs_5_0"></a>Registri - vs \_ 5 \_ 0

I registri di input e output seguenti vengono implementati nel vertex shader versione 5 \_ 0.

## <a name="input-registers"></a>Registri di input



| Tipo di registrazione                                      | Conteggio              | L/S | Dimensione | Indicizzabile in base a r\# | Valori predefiniti | Richiede L'elenco di controllo di accesso |
|----------------------------------------------------|--------------------|-----|-----------|------------------|----------|--------------|
| Temp a 32 bit (r \# )                                  | 4096(r \# +x \# \[ n \] ) | L/S | 4         | No               | nessuno     | Sì          |
| Matrice temporanea indicizzabile a 32 bit (x \# \[ n \] )             | 4096(r \# +x \# \[ n \] ) | L/S | 4         | Sì              | Nessuno     | Sì          |
| Input a 32 bit (v \# )                                 | 32                 | R   | 4         | Sì              | Nessuno     | Sì          |
| Elemento in una risorsa di input (t \# )                 | 128                | R   | 1         | No               | nessuno     | Sì          |
| Campionatore \# (s)                                      | 16                 | R   | 1         | No               | nessuno     | Sì          |
| Informazioni di riferimento su ConstantBuffer (indice cb \# \[ \] )           | 15                 | R   | 4         | Sì(contenuto)    | Nessuno     | Sì          |
| Informazioni di riferimento su iImmediate ConstantBuffer (indice icb \[ \] ) | 1                  | R   | 4         | Sì(contenuto)    | Nessuno     | Sì          |



 

## <a name="output-registers"></a>Registri di output



| Tipo di registrazione                                                      | Conteggio | L/S | Dimensione | Indicizzabile in base a r\# | Valori predefiniti | Richiede L'elenco di controllo di accesso |
|--------------------------------------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL (risultato discard, utile per operazioni con più risultati) | N/A   | W   | N/D       | N/D              | N/D      | No           |
| Elemento dati vertice output a 32 bit (o \# )                            | 32    | W   | 4         | N/D              | N/D      | Sì          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




