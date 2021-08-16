---
title: Registri - gs_4_1
description: Questa sezione contiene informazioni di riferimento per i registri di input e output implementati dalle versioni geometry shader 4 \_ 0 e 4 \_ 1.
ms.assetid: 0312707D-11D0-45D0-9E8C-8BD2BC65352C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 262f86490e95684f0db8ce972f8fc93528cb33ed26b09989399c15ccab766205
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119945"
---
# <a name="registers---gs_4_1"></a>Registri - gs \_ 4 \_ 1

Questa sezione contiene informazioni di riferimento per i registri di input e output implementati dalle versioni geometry shader 4 \_ 0 e 4 \_ 1.

## <a name="input-registers"></a>Registri di input



| Registrazione                 | Nome | Conteggio              | L/S | Dimensione        | Indicizzabile in base a r\# | Valori predefiniti | Richiede la DCL |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| R\#                      |      | 4096(r \# +x \# \[ n \] ) | L/S | 4                | No               | nessuno     | Sì          |
| x \# \[ n\]                 |      | 4096(r \# +x \# \[ n \] ) | L/S | 4                | Sì              | Nessuno     | Sì          |
| Elemento \# \[ vertice \] \[ v\] |      | 32                 | R   | 4(comp) \* 6(vert) | Sì              | Nessuno     | Sì          |
| vprim                    |      | 1                  | R   | 1                | No               | nessuno     | Sì          |
| T\#                      |      | 128                | R   | 1                | No               | nessuno     | Sì          |
| s\#                      |      | 16                 | R   | 1                | No               | nessuno     | Sì          |
| indice \# cb \[\]            |      | 15                 | R   | 4                | Sì (Contenuto)    | Nessuno     | Sì          |
| Indice \[ icb\]             |      | 1                  | R   | 4                | Sì (Contenuto)    | Nessuno     | Sì          |



 

## <a name="output-registers"></a>Registri di output



| Registrazione | Nome            | Conteggio | L/S | Dimensione | Indicizzabile in base a r\# | Valori predefiniti | Richiede la DCL |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | Risultato della eliminazione  | N/A   | W   | N/D       | N/D              | N/D      | No           |
| o\#      | Registro di output | 32    | W   | N/D       | N/D              | 4        | Sì          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello shader 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




