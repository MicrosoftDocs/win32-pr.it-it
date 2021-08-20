---
description: Il linguaggio Windows query di Ricerca di Microsoft supporta sei predicati di ricerca non full-text. I predicati descritti in questa sezione sono elencati nella tabella seguente.
ms.assetid: 74aa6dbc-5c0d-433e-96d9-a8db63907342
title: Predicati non full-text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2915120106e98fd031571b1b974bb09957c9fa02790c050e81374e7717b269d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117680512"
---
# <a name="non-full-text-predicates"></a>Predicati non full-text

Il linguaggio Windows query di Ricerca di Microsoft supporta sei predicati di ricerca non full-text. I predicati descritti in questa sezione sono elencati nella tabella seguente.



| Predicato non full-text                                                    | Descrizione                                                                                                                                                                             |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ALL BITWISE e SOME BITWISE](all-bitwise.md)                            | Set di parole chiave che riguardano il test dei bit in un tipo integrale.                                                                                                               |
| [Funzione DATEADD](-search-sql-dateadd.md)                                | Esegue calcoli di data e ora per la corrispondenza di proprietà con tipi di data. Usare la funzione DATEADD per ottenere date e ore in un periodo di tempo specificato prima del presente.     |
| [Predicato LIKE](-search-sql-like.md)                                     | Confronta i valori di colonna usando criteri di ricerca semplici con caratteri jolly.                                                                                                          |
| [Confronto tra valori letterali](-search-sql-literalvaluecomparison.md)         | Confronta i valori di colonna con valori stringa, data, timestamp, numerici e altri valori letterali. Questo predicato supporta le disuguaglianze, ad esempio maggiore di ('>') e minore di ('<'). |
| [Confronti multivalore (ARRAY)](-search-sql-multivaluedcomparisons.md) | Confronta colonne multivalore con una matrice multivalore di valori letterali.                                                                                                                   |
| [Predicato NULL](-search-sql-null.md)                                     | Rileva i valori di colonna non definiti per il documento.                                                                                                                              |



 

> [!IMPORTANT]
> Le query di ricerca che usano il predicato **NULL** possono richiedere Windows'analisi dell'intero catalogo da parte di Ricerca, che potrebbe rallentare le prestazioni della query.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Predicati full-text](-search-sql-fulltextpredicates.md)
</dt> </dl>

 

 



