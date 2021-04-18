---
description: Microsoft Windows Search, basato sugli standard SQL-92 e SQL-99, migliora le ricerche basate su documenti full-text nelle applicazioni di gestione dei documenti o di gestione delle informazioni.
ms.assetid: 136af1ea-452a-491b-bec7-8c45fa01f87f
title: Estensioni SQL in Microsoft Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 340766d5db99a749e8f508e2dc0bec6a549adfc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525489"
---
# <a name="sql-extensions-in-microsoft-windows-search"></a>Estensioni SQL in Microsoft Windows Search

Microsoft Windows Search, basato sugli standard SQL-92 e SQL-99, migliora le ricerche basate su documenti full-text nelle applicazioni di gestione dei documenti o di gestione delle informazioni. I miglioramenti della ricerca di Windows sono i seguenti:

## <a name="128-character-identifier-names"></a>128-nomi di identificatori di caratteri

Mentre SQL-92 e SQL-99 limitano la colonna e altri identificatori a 18 caratteri, Windows Search supporta i nomi di colonna di 128 caratteri. Per altre informazioni, vedere [Identificatori](-search-sql-identifiers.md).

## <a name="grouping-results-by-columns"></a>Raggruppamento dei risultati per colonne

Nelle query è possibile specificare come raggruppare i risultati. È possibile specificare gli intervalli in base ai quali raggruppare ed è possibile specificare più di una colonna per il raggruppamento. È ad esempio possibile raggruppare i risultati in base a un intervallo di dimensioni dei file (Size < 100, 100 <= size < 1000; 1000 <= size) ed è possibile annidare i raggruppamenti. Per ulteriori informazioni, vedere [Group on... SOPRA... Istruzione](-search-sql-group-on-over.md).

## <a name="diacritic-insensitive-searching"></a>Ricerca Diacritic-Insensitive

Oltre alla ricerca senza distinzione tra maiuscole e minuscole, Windows Search supporta la ricerca non sensibile ai segni diacritici (contrassegni accentati). Per altre informazioni, vedere [sensibilità dei segni diacritici nelle ricerche](-search-sql-accentinsensitivitysearches.md).

## <a name="column-weighting"></a>Ponderazione delle colonne

Le query che cercano più di una colonna possono specificare l'importanza di ogni colonna. I predicati [Contains](-search-sql-contains.md) e [FREETEXT](-search-sql-freetext.md) supportano entrambi la ponderazione delle colonne.

## <a name="null-predicate"></a>Predicato NULL

Sebbene l'indicizzazione di contenuto full-text non disponga di un set di colonne definito, le query possono richiedere che i membri del set di risultati eseguano o non dispongano di colonne specificate. Non è possibile distinguere tra un documento e una proprietà specificata con il valore impostato su **null** e un documento che non dispone della proprietà.

## <a name="rank-modification"></a>Modifica del rango

È possibile modificare la classificazione dei risultati della ricerca usando i [pesi](-search-sql-understandingrelevancevalues.md) sulle proprietà e sui gruppi di proprietà con alias. La coercizione di rango supporta la manipolazione diretta della classificazione della pertinenza in base ai criteri specificati.

 

 



