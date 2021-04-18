---
description: 'Altre informazioni su: lettura dei dati dal database'
title: Lettura di dati dal database
TOCTitle: Reading Data from the Database
ms:assetid: c3c48918-ccd6-4c34-849c-93bd7533ce92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294080(v=EXCHG.10)
ms:contentKeyID: 32765695
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 176cd3189dd1c2701331eff0ef5387827da19b94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313080"
---
# <a name="reading-data-from-the-database"></a>Lettura di dati dal database


_**Si applica a:** Windows | Windows Server_

## <a name="reading-data-from-the-database"></a>Lettura di dati dal database

La lettura dei dati dal database deve essere eseguita all'interno di una transazione.

Nella procedura riportata di seguito viene illustrato come eseguire una semplice operazione di lettura nel database.

### <a name="to-read-data-from-a-database"></a>Per leggere i dati da un database

1.  Chiamare [JetBeginTransaction](./jetbegintransaction-function.md) o [JETBEGINTRANSACTION2](./jetbegintransaction2-function.md) con l'ID sessione per avviare la transazione.

2.  Spostare il cursore sul record desiderato chiamando [JetMove](./jetmove-function.md) con JET_MoveFirst nel parametro *Crow* . Per ulteriori informazioni su come spostare il cursore, vedere l'argomento [indicizzazione nell'](./indexing-in-the-table.md) argomento della tabella.

3.  Chiamare [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) sul record corrente con JET_ColInfo specificato nel parametro *InfoLevel* per recuperare l'ID di colonna per la colonna. L'ID di colonna viene restituito nella struttura [JET_COLUMNDEF](./jet-columndef-structure.md) .

4.  Leggere i dati dalla colonna chiamando [JetRetrieveColumn](./jetretrievecolumn-function.md) con l'ID di colonna recuperato nel passaggio 3 nel parametro columnid. Il parametro *pvData* contiene il tipo di dati specificato nella struttura [JET_COLUMNDEF](./jet-columndef-structure.md) recuperata nel passaggio 3.

5.  Chiamare [JetCommitTransaction](./jetcommittransaction-function.md) per eseguire il commit della transazione nel database.
