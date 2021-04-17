---
description: Il linguaggio di query di ricerca di Microsoft Windows supporta sei predicati di ricerca non full-text. I predicati descritti in questa sezione sono elencati nella tabella seguente.
ms.assetid: 74aa6dbc-5c0d-433e-96d9-a8db63907342
title: Predicati non full-text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d41076ebc61aa56ed547f13f717ac40bed35959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306119"
---
# <a name="non-full-text-predicates"></a>Predicati non full-text

Il linguaggio di query di ricerca di Microsoft Windows supporta sei predicati di ricerca non full-text. I predicati descritti in questa sezione sono elencati nella tabella seguente.



| Predicato non full-text                                                    | Descrizione                                                                                                                                                                             |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ALL bit per bit e SOME bit per bit](all-bitwise.md)                            | È un set di parole chiave per il testing dei bit in un tipo integrale.                                                                                                               |
| [DATEADD (funzione)](-search-sql-dateadd.md)                                | Esegue calcoli di data e ora per le proprietà corrispondenti con tipi di dati. Utilizzare la funzione DATEADD per ottenere le date e le ore in un intervallo di tempo specificato prima del presente.     |
| [Predicato LIKE](-search-sql-like.md)                                     | Confronta i valori delle colonne usando semplici criteri di ricerca con caratteri jolly.                                                                                                          |
| [Confronto di valori letterali](-search-sql-literalvaluecomparison.md)         | Confronta i valori delle colonne con valori di stringa, data, timestamp, numerici e di altro valore letterale. Questo predicato supporta le disuguaglianze quali maggiore di (' >') e minore di (' <'). |
| [Confronti multivalore (matrice)](-search-sql-multivaluedcomparisons.md) | Confronta le colonne multivalore con una matrice multivalore di valori letterali.                                                                                                                   |
| [Predicato NULL](-search-sql-null.md)                                     | Rileva i valori di colonna che non sono definiti per il documento.                                                                                                                              |



 

> [!IMPORTANT]
> Le query di ricerca che usano il predicato **null** possono richiedere che Windows Search analizzi l'intero catalogo, che potrebbe rallentare le prestazioni della query.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Predicati full-text](-search-sql-fulltextpredicates.md)
</dt> </dl>

 

 



