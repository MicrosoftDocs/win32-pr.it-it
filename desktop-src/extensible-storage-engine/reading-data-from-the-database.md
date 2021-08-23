---
description: 'Altre informazioni su: Lettura di dati dal database'
title: Lettura di dati dal database
TOCTitle: Reading Data from the Database
ms:assetid: c3c48918-ccd6-4c34-849c-93bd7533ce92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294080(v=EXCHG.10)
ms:contentKeyID: 32765695
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 7d33aa2640c07018186a5516d985fd4e46194d39cd4b12b7254f430f889e2484
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780261"
---
# <a name="reading-data-from-the-database"></a>Lettura di dati dal database


_**Si applica a:** Windows | Windows Server_

## <a name="reading-data-from-the-database"></a>Lettura di dati dal database

La lettura dei dati dal database deve essere eseguita all'interno di una transazione.

Nella procedura seguente viene illustrato come eseguire una semplice operazione di lettura nel database.

### <a name="to-read-data-from-a-database"></a>Per leggere dati da un database

1.  Chiamare [JetBeginTransaction o](./jetbegintransaction-function.md) [JetBeginTransaction2 con](./jetbegintransaction2-function.md) l'ID sessione per avviare la transazione.

2.  Spostare il cursore nel record desiderato chiamando [JetMove](./jetmove-function.md) con JET_MoveFirst nel *parametro cRow.* Per altre informazioni su come spostare il cursore, vedere [l'argomento Indicizzazione nell'argomento Tabella](./indexing-in-the-table.md) .

3.  Chiamare [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) sul record corrente con JET_ColInfo specificato nel *parametro InfoLevel* per recuperare l'ID colonna per la colonna. L'ID colonna viene restituito [nella JET_COLUMNDEF](./jet-columndef-structure.md) struttura .

4.  Leggere i dati dalla colonna chiamando [JetRetrieveColumn con](./jetretrievecolumn-function.md) l'ID di colonna recuperato nel passaggio 3 nel parametro columnid. Il *parametro pvData* contiene il tipo di dati specificato nella [struttura JET_COLUMNDEF](./jet-columndef-structure.md) recuperata nel passaggio 3.

5.  Chiamare [JetCommitTransaction per](./jetcommittransaction-function.md) eseguire il commit della transazione nel database.
