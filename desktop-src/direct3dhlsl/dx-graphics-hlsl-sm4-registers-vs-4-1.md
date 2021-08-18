---
title: Registri - vs_4_1
description: Questa sezione contiene informazioni di riferimento per i registri di input e output implementati da vertex shader versione 4 \_ 1.
ms.assetid: ea449195-d012-4a14-9760-b738a8623343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0164b1d82a9d371e735177f381e2a1a97aa062aaca8c65a00d4959a32279ed11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119925"
---
# <a name="registers---vs_4_1"></a>Registri - vs \_ 4 \_ 1

Questa sezione contiene informazioni di riferimento per i registri di input e output implementati da vertex shader versione 4 \_ 1.

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



| Registrazione | Nome            | Conteggio | L/S | Dimensione | Indicizzabile in base a r\# | Valori predefiniti | Richiede L'elenco di controllo di accesso |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| NULL     | Risultato dell'eliminazione  | N/A   | W   | N/D       | N/D              | N/D      | No           |
| o\#      | Registro di output | 32    | W   | N/D       | N/D              | 4        | Sì          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello shader 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




