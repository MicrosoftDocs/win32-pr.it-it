---
description: La \_ tabella Streams elenca i flussi di dati OLE incorporati. Si tratta di una tabella temporanea, creata solo quando si fa riferimento a un'istruzione SQL.
ms.assetid: 1e30472d-6ba5-410a-a81b-07ed225dcb69
title: Tabella _Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9607097b32acc8a3c2350a00db0b9721a4aa353
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311115"
---
# <a name="_streams-table"></a><span data-ttu-id="06ffc-104">\_Tabella flussi</span><span class="sxs-lookup"><span data-stu-id="06ffc-104">\_Streams Table</span></span>

<span data-ttu-id="06ffc-105">La \_ tabella Streams elenca i flussi di dati OLE incorporati.</span><span class="sxs-lookup"><span data-stu-id="06ffc-105">The \_Streams table lists embedded OLE data streams.</span></span> <span data-ttu-id="06ffc-106">Si tratta di una tabella temporanea, creata solo quando si fa riferimento a un'istruzione SQL.</span><span class="sxs-lookup"><span data-stu-id="06ffc-106">This is a temporary table, created only when referenced by a SQL statement.</span></span>



| <span data-ttu-id="06ffc-107">Colonna</span><span class="sxs-lookup"><span data-stu-id="06ffc-107">Column</span></span> | <span data-ttu-id="06ffc-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="06ffc-108">Type</span></span>                 | <span data-ttu-id="06ffc-109">Chiave</span><span class="sxs-lookup"><span data-stu-id="06ffc-109">Key</span></span> | <span data-ttu-id="06ffc-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="06ffc-110">Nullable</span></span> |
|--------|----------------------|-----|----------|
| <span data-ttu-id="06ffc-111">Nome</span><span class="sxs-lookup"><span data-stu-id="06ffc-111">Name</span></span>   | [<span data-ttu-id="06ffc-112">Text</span><span class="sxs-lookup"><span data-stu-id="06ffc-112">Text</span></span>](text.md)     | <span data-ttu-id="06ffc-113">S</span><span class="sxs-lookup"><span data-stu-id="06ffc-113">Y</span></span>   | <span data-ttu-id="06ffc-114">N</span><span class="sxs-lookup"><span data-stu-id="06ffc-114">N</span></span>        |
| <span data-ttu-id="06ffc-115">Data</span><span class="sxs-lookup"><span data-stu-id="06ffc-115">Data</span></span>   | [<span data-ttu-id="06ffc-116">Binario</span><span class="sxs-lookup"><span data-stu-id="06ffc-116">Binary</span></span>](binary.md) | <span data-ttu-id="06ffc-117">N</span><span class="sxs-lookup"><span data-stu-id="06ffc-117">N</span></span>   | <span data-ttu-id="06ffc-118">S</span><span class="sxs-lookup"><span data-stu-id="06ffc-118">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="06ffc-119">Colonne</span><span class="sxs-lookup"><span data-stu-id="06ffc-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="06ffc-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome</span><span class="sxs-lookup"><span data-stu-id="06ffc-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="06ffc-121">Chiave univoca che identifica il flusso.</span><span class="sxs-lookup"><span data-stu-id="06ffc-121">A unique key that identifies the stream.</span></span> <span data-ttu-id="06ffc-122">La lunghezza massima del nome è di 62 caratteri.</span><span class="sxs-lookup"><span data-stu-id="06ffc-122">The maximum length of Name is 62 characters.</span></span>

</dd> <dt>

<span data-ttu-id="06ffc-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Dati</span><span class="sxs-lookup"><span data-stu-id="06ffc-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="06ffc-124">Dati binari non formattati.</span><span class="sxs-lookup"><span data-stu-id="06ffc-124">The unformatted binary data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06ffc-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="06ffc-125">Remarks</span></span>

<span data-ttu-id="06ffc-126">Per copiare un flusso di dati OLE, ad esempio un oggetto con tipo di dati [Binary](binary.md) , da un file in un database, creare un record nella \_ tabella Streams e immettere il nome del flusso di dati nella colonna Name del record e copiare i dati dal file nella colonna di dati tramite [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama).</span><span class="sxs-lookup"><span data-stu-id="06ffc-126">To copy an OLE data stream (for example, an object of the [Binary](binary.md) data type) from a file into a database, create a record in the \_Streams table and enter the name of the data stream into the Name column of this record and copy the data from the file into the Data column using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama).</span></span> <span data-ttu-id="06ffc-127">Usare [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) per inserire il nuovo record nella tabella.</span><span class="sxs-lookup"><span data-stu-id="06ffc-127">Use [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the new record into the table.</span></span>

<span data-ttu-id="06ffc-128">Per leggere un flusso di dati binario incorporato in un database, usare una query SQL per trovare e recuperare il record contenente i dati binari.</span><span class="sxs-lookup"><span data-stu-id="06ffc-128">To read a binary data stream embedded in a database, use a SQL query to find and to fetch the record containing the binary data.</span></span> <span data-ttu-id="06ffc-129">Usare [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) per leggere i dati binari in un buffer.</span><span class="sxs-lookup"><span data-stu-id="06ffc-129">Use [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) to read the binary data into a buffer.</span></span>

<span data-ttu-id="06ffc-130">Per spostare un flusso di dati binari da un database a un altro, esportare prima i dati in un file.</span><span class="sxs-lookup"><span data-stu-id="06ffc-130">To move a binary data stream from one database to another, first export the data to a file.</span></span> <span data-ttu-id="06ffc-131">Usare una query SQL per trovare il flusso di dati nel file e usare [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) per copiare i dati dal file nella colonna di dati della \_ tabella dei flussi del secondo database.</span><span class="sxs-lookup"><span data-stu-id="06ffc-131">Use a SQL query to find the data stream in the file and use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) to copy the data from the file into Data column of \_Streams table of the second database.</span></span> <span data-ttu-id="06ffc-132">In questo modo si garantisce che ogni database disponga di una propria copia dei dati binari.</span><span class="sxs-lookup"><span data-stu-id="06ffc-132">This ensures that each database has its own copy of the binary data.</span></span> <span data-ttu-id="06ffc-133">Non è possibile spostare i dati binari da un database a un altro semplicemente recuperando un record con i dati del primo database e inserendoli nel secondo database.</span><span class="sxs-lookup"><span data-stu-id="06ffc-133">You cannot move binary data from one database to another simply by fetching a record with the data from the first database and inserting it into the second database.</span></span>

<span data-ttu-id="06ffc-134">Per eliminare un flusso di dati, recuperare il record e impostare la colonna di dati su null prima di aggiornare il record.</span><span class="sxs-lookup"><span data-stu-id="06ffc-134">To delete a data stream, fetch the record and set the Data column to null before updating the record.</span></span> <span data-ttu-id="06ffc-135">Un altro metodo consiste nel rimuovere il record dalla tabella, eliminarlo utilizzando [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) o una query SQL semplice.</span><span class="sxs-lookup"><span data-stu-id="06ffc-135">Another method is to remove the record from the table, deleting it using either [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) or a plain SQL query.</span></span> <span data-ttu-id="06ffc-136">Un flusso non deve essere recuperato in un record se il flusso viene eliminato dalla tabella.</span><span class="sxs-lookup"><span data-stu-id="06ffc-136">A stream should not be fetched into a record if the stream is deleted from the table.</span></span>

<span data-ttu-id="06ffc-137">Per rinominare un flusso di dati OLE, aggiornare la colonna ' name ' del record.</span><span class="sxs-lookup"><span data-stu-id="06ffc-137">To rename an OLE data stream, update the 'Name' column of the record.</span></span>

<span data-ttu-id="06ffc-138">Se in questa tabella viene posizionata un'attesa utilizzando SQL (ALTER TABLE</span><span class="sxs-lookup"><span data-stu-id="06ffc-138">If a hold is placed on this table using SQL (ALTER TABLE</span></span> <table> <span data-ttu-id="06ffc-139">In attesa) o viene aggiunta una colonna con l'ESENZIONe, la tabella deve essere rilasciata usando FREE.</span><span class="sxs-lookup"><span data-stu-id="06ffc-139">HOLD) or a column is added with HOLD, the table must be released using FREE.</span></span> <span data-ttu-id="06ffc-140">I flussi non vengono scritti finché la tabella non viene rilasciata o sottoposta a commit.</span><span class="sxs-lookup"><span data-stu-id="06ffc-140">Streams are not written until the table has been released or committed.</span></span>

 

 



