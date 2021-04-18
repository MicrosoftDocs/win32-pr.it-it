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
# <a name="reading-data-from-the-database"></a><span data-ttu-id="2f0d9-103">Lettura di dati dal database</span><span class="sxs-lookup"><span data-stu-id="2f0d9-103">Reading Data from the Database</span></span>


<span data-ttu-id="2f0d9-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2f0d9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="reading-data-from-the-database"></a><span data-ttu-id="2f0d9-105">Lettura di dati dal database</span><span class="sxs-lookup"><span data-stu-id="2f0d9-105">Reading Data from the Database</span></span>

<span data-ttu-id="2f0d9-106">La lettura dei dati dal database deve essere eseguita all'interno di una transazione.</span><span class="sxs-lookup"><span data-stu-id="2f0d9-106">Reading data from the database should be performed within a transaction.</span></span>

<span data-ttu-id="2f0d9-107">Nella procedura riportata di seguito viene illustrato come eseguire una semplice operazione di lettura nel database.</span><span class="sxs-lookup"><span data-stu-id="2f0d9-107">The following procedure shows how to perform a simple read operation in the database.</span></span>

### <a name="to-read-data-from-a-database"></a><span data-ttu-id="2f0d9-108">Per leggere i dati da un database</span><span class="sxs-lookup"><span data-stu-id="2f0d9-108">To read data from a database</span></span>

1.  <span data-ttu-id="2f0d9-109">Chiamare [JetBeginTransaction](./jetbegintransaction-function.md) o [JETBEGINTRANSACTION2](./jetbegintransaction2-function.md) con l'ID sessione per avviare la transazione.</span><span class="sxs-lookup"><span data-stu-id="2f0d9-109">Call [JetBeginTransaction](./jetbegintransaction-function.md) or [JetBeginTransaction2](./jetbegintransaction2-function.md) with the session ID to start the transaction.</span></span>

2.  <span data-ttu-id="2f0d9-110">Spostare il cursore sul record desiderato chiamando [JetMove](./jetmove-function.md) con JET_MoveFirst nel parametro *Crow* .</span><span class="sxs-lookup"><span data-stu-id="2f0d9-110">Move the cursor to the desired record by calling [JetMove](./jetmove-function.md) with JET_MoveFirst in the *cRow* parameter.</span></span> <span data-ttu-id="2f0d9-111">Per ulteriori informazioni su come spostare il cursore, vedere l'argomento [indicizzazione nell'](./indexing-in-the-table.md) argomento della tabella.</span><span class="sxs-lookup"><span data-stu-id="2f0d9-111">For more information on how to move the cursor, see the [Indexing in the Table](./indexing-in-the-table.md) topic.</span></span>

3.  <span data-ttu-id="2f0d9-112">Chiamare [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) sul record corrente con JET_ColInfo specificato nel parametro *InfoLevel* per recuperare l'ID di colonna per la colonna.</span><span class="sxs-lookup"><span data-stu-id="2f0d9-112">Call [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) on the current record with JET_ColInfo specified in the *InfoLevel* parameter to retrieve the column ID for the column.</span></span> <span data-ttu-id="2f0d9-113">L'ID di colonna viene restituito nella struttura [JET_COLUMNDEF](./jet-columndef-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="2f0d9-113">The column ID is returned in the [JET_COLUMNDEF](./jet-columndef-structure.md) structure.</span></span>

4.  <span data-ttu-id="2f0d9-114">Leggere i dati dalla colonna chiamando [JetRetrieveColumn](./jetretrievecolumn-function.md) con l'ID di colonna recuperato nel passaggio 3 nel parametro columnid.</span><span class="sxs-lookup"><span data-stu-id="2f0d9-114">Read the data from the column by calling [JetRetrieveColumn](./jetretrievecolumn-function.md) with the column ID retrieved in step 3 in the columnid parameter.</span></span> <span data-ttu-id="2f0d9-115">Il parametro *pvData* contiene il tipo di dati specificato nella struttura [JET_COLUMNDEF](./jet-columndef-structure.md) recuperata nel passaggio 3.</span><span class="sxs-lookup"><span data-stu-id="2f0d9-115">The *pvData* parameter contains the type of data specified in the [JET_COLUMNDEF](./jet-columndef-structure.md) structure retrieved in step 3.</span></span>

5.  <span data-ttu-id="2f0d9-116">Chiamare [JetCommitTransaction](./jetcommittransaction-function.md) per eseguire il commit della transazione nel database.</span><span class="sxs-lookup"><span data-stu-id="2f0d9-116">Call [JetCommitTransaction](./jetcommittransaction-function.md) to commit the transaction to the database.</span></span>
