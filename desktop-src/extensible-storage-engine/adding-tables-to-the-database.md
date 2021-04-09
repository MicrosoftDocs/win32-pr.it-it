---
description: 'Altre informazioni su: aggiunta di tabelle al database'
title: Aggiunta di tabelle al database
TOCTitle: Adding Tables to the Database
ms:assetid: 176d4fea-c856-441b-bd58-165b37c35095
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269195(v=EXCHG.10)
ms:contentKeyID: 32765498
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 67569f8efc164cc7156f346b6754f13b296d3b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966417"
---
# <a name="adding-tables-to-the-database"></a><span data-ttu-id="20d02-103">Aggiunta di tabelle al database</span><span class="sxs-lookup"><span data-stu-id="20d02-103">Adding Tables to the Database</span></span>


<span data-ttu-id="20d02-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="20d02-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="adding-tables-to-the-database"></a><span data-ttu-id="20d02-105">Aggiunta di tabelle al database</span><span class="sxs-lookup"><span data-stu-id="20d02-105">Adding Tables to the Database</span></span>

<span data-ttu-id="20d02-106">Le tabelle sono una raccolta eterogenea di record che raggruppano fisicamente e logicamente i dati nel database.</span><span class="sxs-lookup"><span data-stu-id="20d02-106">Tables are a heterogeneous collection of records that physically and logically group the data in the database.</span></span> <span data-ttu-id="20d02-107">Le tabelle vengono identificate in modo univoco in base al nome.</span><span class="sxs-lookup"><span data-stu-id="20d02-107">Tables are uniquely identified by their name.</span></span> <span data-ttu-id="20d02-108">L'ID tabella ([JET_TABLEID](./jet-tableid.md)) è un handle per un cursore utilizzato per aggiornare e spostarsi tra le tabelle.</span><span class="sxs-lookup"><span data-stu-id="20d02-108">The table ID ([JET_TABLEID](./jet-tableid.md)) is a handle to a cursor that is used to update and navigate tables.</span></span> <span data-ttu-id="20d02-109">È possibile aprire più [JET_TABLEID](./jet-tableid.md) nella stessa tabella.</span><span class="sxs-lookup"><span data-stu-id="20d02-109">You may open multiple [JET_TABLEID](./jet-tableid.md) on the same table.</span></span>

<span data-ttu-id="20d02-110">Una tabella esistente viene aperta nella chiamata a [JetOpenTable](./jetopentable-function.md)e viene creata una nuova tabella senza righe o colonne con [JetCreateTable](./jetcreatetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="20d02-110">An existing table is opened in the call to [JetOpenTable](./jetopentable-function.md), and a new table is created without rows or columns with [JetCreateTable](./jetcreatetable-function.md).</span></span> <span data-ttu-id="20d02-111">Per creare una tabella in modo atomico con un set iniziale di colonne e indici, chiamare [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) o [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).</span><span class="sxs-lookup"><span data-stu-id="20d02-111">To atomically create a table with an initial set of columns and indices, call [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) or [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).</span></span> <span data-ttu-id="20d02-112">Le dimensioni iniziali della tabella sono fornite nel parametro *lPages* in [JetCreateTable](./jetcreatetable-function.md) o nel membro **ulPages** della struttura [JET_TABLECREATE](./jet-tablecreate-structure.md) della chiamata a [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="20d02-112">The initial size of the table is given in the *lPages* parameter in [JetCreateTable](./jetcreatetable-function.md) or the **ulPages** member of the [JET_TABLECREATE](./jet-tablecreate-structure.md) structure in the call to [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span> <span data-ttu-id="20d02-113">Le tabelle aumentano automaticamente quando i dati vengono aggiunti alla tabella.</span><span class="sxs-lookup"><span data-stu-id="20d02-113">Tables grow automatically when data is added to the table.</span></span> <span data-ttu-id="20d02-114">La crescita è proporzionale alle dimensioni iniziali della tabella.</span><span class="sxs-lookup"><span data-stu-id="20d02-114">The growth is proportional to the initial size of the table.</span></span> <span data-ttu-id="20d02-115">Le colonne possono essere aggiunte alla tabella in qualsiasi momento con [JetAddColumn](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="20d02-115">Columns may be added to the table at any time with [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="20d02-116">Quando l'applicazione non deve più accedere alla tabella, è possibile chiudere il cursore con [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="20d02-116">When the application no longer needs to access the table, the cursor can be closed with [JetCloseTable](./jetclosetable-function.md).</span></span> <span data-ttu-id="20d02-117">La tabella può essere eliminata tramite una chiamata a [JetDeleteTable](./jetdeletetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="20d02-117">The table may be deleted via a call to [JetDeleteTable](./jetdeletetable-function.md).</span></span>

<span data-ttu-id="20d02-118">Le operazioni di tabella devono essere eseguite nel contesto di una transazione.</span><span class="sxs-lookup"><span data-stu-id="20d02-118">Table operations should be performed within the context of a transaction.</span></span>

## <a name="see-also"></a><span data-ttu-id="20d02-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="20d02-119">See Also</span></span>

[<span data-ttu-id="20d02-120">Transazioni</span><span class="sxs-lookup"><span data-stu-id="20d02-120">Transactions</span></span>](./transactions.md)
