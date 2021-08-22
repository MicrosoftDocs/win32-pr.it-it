---
description: Microsoft Windows Search, basato sugli standard SQL-92 e SQL-99, migliora le ricerche full-text basate su documenti nelle applicazioni di gestione dei documenti o di gestione delle informazioni.
ms.assetid: 136af1ea-452a-491b-bec7-8c45fa01f87f
title: SQL Estensioni in Microsoft Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c300b0960e97cba14237bd355e33ae7e42788b1925525e60462d15a5d014e6f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462459"
---
# <a name="sql-extensions-in-microsoft-windows-search"></a>SQL Estensioni in Microsoft Windows Search

Microsoft Windows Search, basato sugli standard SQL-92 e SQL-99, migliora le ricerche full-text basate su documenti nelle applicazioni di gestione dei documenti o di gestione delle informazioni. Windows I miglioramenti della ricerca includono quanto segue:

## <a name="128-character-identifier-names"></a>Nomi di identificatori di 128 caratteri

Mentre SQL-92 e SQL-99 limitano la colonna e altri identificatori a 18 caratteri, Windows Search supporta nomi di colonna di 128 caratteri. Per altre informazioni, vedere [Identificatori](-search-sql-identifiers.md).

## <a name="grouping-results-by-columns"></a>Raggruppamento dei risultati per colonne

Le query possono specificare come raggruppare i risultati. È possibile specificare gli intervalli in base ai quali raggruppare e specificare più di una colonna per il raggruppamento. Ad esempio, è possibile raggruppare i risultati in un intervallo di dimensioni di file (dimensioni < 100, 100 <= dimensioni < 1000; 1000 <= dimensioni) ed è possibile annidare i raggruppamenti. Per altre informazioni, vedere [GROUP ON ... Oltre... Istruzione](-search-sql-group-on-over.md).

## <a name="diacritic-insensitive-searching"></a>Diacritic-Insensitive ricerca

Oltre alla ricerca senza distinzione tra maiuscole e minuscole, Windows ricerca supporta la ricerca che non è sensibile ai segni diacritici (segni accentati). Per altre informazioni, vedere [Riservatezza dei segni diacritici nelle ricerche.](-search-sql-accentinsensitivitysearches.md)

## <a name="column-weighting"></a>Ponderazione delle colonne

Le query in cui vengono eseguite ricerche in più di una colonna possono specificare l'importanza di ogni colonna. I [predicati CONTAINS](-search-sql-contains.md) [e FREETEXT](-search-sql-freetext.md) supportano entrambi la ponderazione delle colonne.

## <a name="null-predicate"></a>Predicato NULL

Anche se l'indicizzazione del contenuto full-text non dispone di un set definito di colonne, le query possono richiedere che i membri del set di risultati ese possano o meno avere colonne specificate. Non è possibile distinguere tra un documento con una proprietà specificata con il valore impostato su **NULL** e un documento che non dispone della proprietà .

## <a name="rank-modification"></a>Modifica della classificazione

È possibile modificare la classificazione dei risultati della ricerca [usando pesi](-search-sql-understandingrelevancevalues.md) sulle proprietà e sui gruppi di proprietà con alias. La coercizione di classificazione supporta la manipolazione diretta della classificazione per pertinenza in base ai criteri specificati.

 

 



