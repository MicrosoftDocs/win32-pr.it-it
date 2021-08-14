---
title: Registri - gs_4_0
description: Questa sezione contiene informazioni di riferimento per i registri di input e output implementati da geometry shader versione 4 \_ 0.
ms.assetid: 1f3ebd71-19de-4e26-87f0-4fb5c8e2a343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a27cbd13cba06ebb05fe1155bc97d13debe3154da48c05cf97a31d889ba88fbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118513624"
---
# <a name="registers---gs_4_0"></a>Registri - gs \_ 4 \_ 0

Questa sezione contiene informazioni di riferimento per i registri di input e output implementati da geometry shader versione 4 \_ 0.

## <a name="input-registers"></a>Registri di input



| Registrazione                 | Nome | Conteggio              | L/S | Dimensione        | Indicizzabile in base a r\# | Valori predefiniti | Richiede L'elenco di controllo di accesso |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| R\#                      |      | 4096(r \# +x \# \[ n \] ) | L/S | 4                | No               | nessuno     | Sì          |
| x \# \[ n\]                 |      | 4096(r \# +x \# \[ n \] ) | L/S | 4                | Sì              | Nessuno     | Sì          |
| elemento \# \[ vertice \] \[ v\] |      | 32                 | R   | 4(comp) \* 6(vert) | Sì              | Nessuno     | Sì          |
| vprim                    |      | 1                  | R   | 1                | No               | nessuno     | Sì          |
| T\#                      |      | 128                | R   | 1                | No               | nessuno     | Sì          |
| s\#                      |      | 16                 | R   | 1                | No               | nessuno     | Sì          |
| Indice \# cb \[\]            |      | 15                 | R   | 4                | Sì(Contenuto)    | Nessuno     | Sì          |
| Indice \[ icb\]             |      | 1                  | R   | 4                | Sì(Contenuto)    | Nessuno     | Sì          |



 

## <a name="output-registers"></a>Registri di output



| Registrazione | Nome            | Conteggio | L/S | Dimensione | Indicizzabile in base a r\# | Valori predefiniti | Richiede L'elenco di controllo di accesso |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | Risultato dell'eliminazione  | N/A   | W   | N/D       | N/D              | N/D      | No           |
| o\#      | Registro di output | 32    | W   | N/D       | N/D              | 4        | Sì          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello shader 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




