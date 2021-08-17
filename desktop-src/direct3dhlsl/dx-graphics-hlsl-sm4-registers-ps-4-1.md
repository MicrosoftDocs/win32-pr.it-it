---
title: Registri - ps_4_1
description: Questa sezione contiene informazioni di riferimento per i registri di input e output implementati da pixel shader versione 4 \_ 1.
ms.assetid: d3f3e264-569e-43a6-a06b-a512d36a7b53
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ff602f2f14292407b81dca9e19048e88db645a1b3514b4b279282436046e11c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119276541"
---
# <a name="registers---ps_4_1"></a>Registri - ps \_ 4 \_ 1

Questa sezione contiene informazioni di riferimento per i registri di input e output implementati da pixel shader versione 4 \_ 1.

## <a name="input-registers"></a>Registri di input



| Registrazione      | Nome | Conteggio              | L/S | Dimensione | Indicizzabile in base a r\# | Valori predefiniti | Richiede L'elenco di controllo di accesso |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| R\#           |      | 4096(r \# +x \# \[ n \] ) | L/S | 4         | No               | nessuno     | Sì          |
| x \# \[ n\]      |      | 4096(r \# +x \# \[ n \] ) | L/S | 4         | Sì              | Nessuno     | Sì          |
| v\#           |      | 32                 | R   | 4         | Sì              | Nessuno     | Sì          |
| T\#           |      | 128                | R   | 1         | No               | nessuno     | Sì          |
| s\#           |      | 16                 | R   | 1         | No               | nessuno     | Sì          |
| Indice \# cb \[\] |      | 15                 | R   | 4         | Sì(Contenuto)    | Nessuno     | Sì          |
| Indice \[ icb\]  |      | 1                  | R   | 4         | Sì(Contenuto)    | Nessuno     | Sì          |



 

## <a name="output-registers"></a>Registri di output



| Registrazione | Nome             | Conteggio | L/S | Dimensione | Indicizzabile in base a r\# | Valori predefiniti | Richiede L'elenco di controllo di accesso |
|----------|------------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | Risultato dell'eliminazione   | N/A   | W   | N/D       | N/D              | N/D      | No           |
| o\#      | Registro di output  | 8     | W   | N/D       | N/D              | 4        | No           |
| oDepth   | Profondità di output     | 1     | W   | N/D       | N/D              | 1        | N/D          |
| oMask    | Maschera MSAA di output | 1     | W   | N/D       | N/D              | 1        | N/D          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello shader 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




