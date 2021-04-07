---
description: La \_ tabella Storages elenca le archiviazioni di dati OLE embedded. Si tratta di una tabella temporanea, creata solo quando si fa riferimento a un'istruzione SQL.
ms.assetid: b2f2907d-6966-4b63-9589-c1580f8db574
title: Tabella _Storages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27995dd61c7d25100fc0e1ae2297695e361f44f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881193"
---
# <a name="_storages-table"></a><span data-ttu-id="84118-104">\_Tabella Storages</span><span class="sxs-lookup"><span data-stu-id="84118-104">\_Storages Table</span></span>

<span data-ttu-id="84118-105">La \_ tabella Storages elenca le archiviazioni di dati OLE embedded.</span><span class="sxs-lookup"><span data-stu-id="84118-105">The \_Storages table lists embedded OLE data storages.</span></span> <span data-ttu-id="84118-106">Si tratta di una tabella temporanea, creata solo quando si fa riferimento a un'istruzione SQL.</span><span class="sxs-lookup"><span data-stu-id="84118-106">This is a temporary table, created only when referenced by a SQL statement.</span></span>



| <span data-ttu-id="84118-107">Colonna</span><span class="sxs-lookup"><span data-stu-id="84118-107">Column</span></span> | <span data-ttu-id="84118-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="84118-108">Type</span></span>                 | <span data-ttu-id="84118-109">Chiave</span><span class="sxs-lookup"><span data-stu-id="84118-109">Key</span></span> | <span data-ttu-id="84118-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="84118-110">Nullable</span></span> |
|--------|----------------------|-----|----------|
| <span data-ttu-id="84118-111">Nome</span><span class="sxs-lookup"><span data-stu-id="84118-111">Name</span></span>   | [<span data-ttu-id="84118-112">Text</span><span class="sxs-lookup"><span data-stu-id="84118-112">Text</span></span>](text.md)     | <span data-ttu-id="84118-113">S</span><span class="sxs-lookup"><span data-stu-id="84118-113">Y</span></span>   | <span data-ttu-id="84118-114">N</span><span class="sxs-lookup"><span data-stu-id="84118-114">N</span></span>        |
| <span data-ttu-id="84118-115">Data</span><span class="sxs-lookup"><span data-stu-id="84118-115">Data</span></span>   | [<span data-ttu-id="84118-116">Binario</span><span class="sxs-lookup"><span data-stu-id="84118-116">Binary</span></span>](binary.md) | <span data-ttu-id="84118-117">N</span><span class="sxs-lookup"><span data-stu-id="84118-117">N</span></span>   | <span data-ttu-id="84118-118">S</span><span class="sxs-lookup"><span data-stu-id="84118-118">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="84118-119">Colonne</span><span class="sxs-lookup"><span data-stu-id="84118-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="84118-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome</span><span class="sxs-lookup"><span data-stu-id="84118-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="84118-121">Chiave univoca che identifica l'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="84118-121">A unique key that identifies the storage.</span></span> <span data-ttu-id="84118-122">La lunghezza massima del nome è 31 caratteri.</span><span class="sxs-lookup"><span data-stu-id="84118-122">The maximum length of Name is 31 characters.</span></span>

</dd> <dt>

<span data-ttu-id="84118-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Dati</span><span class="sxs-lookup"><span data-stu-id="84118-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="84118-124">Dati binari non formattati.</span><span class="sxs-lookup"><span data-stu-id="84118-124">The unformatted binary data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84118-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="84118-125">Remarks</span></span>

<span data-ttu-id="84118-126">Per aggiungere una risorsa di archiviazione OLE a un database, creare un nuovo record nella \_ tabella Storages e immettere il nome della risorsa di archiviazione nella colonna nome.</span><span class="sxs-lookup"><span data-stu-id="84118-126">To add an OLE storage to a database, create a new record in the \_Storages table and enter the name of the storage into the Name column.</span></span> <span data-ttu-id="84118-127">Usare [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) per copiare i dati nella colonna di dati del record.</span><span class="sxs-lookup"><span data-stu-id="84118-127">Use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) to copy data into the Data column of this record.</span></span> <span data-ttu-id="84118-128">Infine, usare [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) per inserire il record nella \_ tabella storages.</span><span class="sxs-lookup"><span data-stu-id="84118-128">Finally, use [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the \_Storages table.</span></span>

<span data-ttu-id="84118-129">Non è possibile leggere i dati dalla \_ tabella storages.</span><span class="sxs-lookup"><span data-stu-id="84118-129">Data cannot be read from the \_Storages table.</span></span> <span data-ttu-id="84118-130">\_È tuttavia possibile eseguire una query sulla tabella Storages per verificare l'esistenza di una risorsa di archiviazione specifica.</span><span class="sxs-lookup"><span data-stu-id="84118-130">However, the \_Storages table can be queried to check for the existence of a specific storage.</span></span> <span data-ttu-id="84118-131">Ciò significa che non è possibile spostare una risorsa di archiviazione OLE da un database a un altro.</span><span class="sxs-lookup"><span data-stu-id="84118-131">This means that it is not possible to move an OLE storage from one database to another.</span></span> <span data-ttu-id="84118-132">È invece necessario importare il file di archiviazione originale nel nuovo database. Per eliminare una risorsa di archiviazione OLE, recuperare il record contenente i dati binari, impostare la colonna di dati nella \_ tabella Storages su null, quindi aggiornare il record.</span><span class="sxs-lookup"><span data-stu-id="84118-132">You must instead import the original storage file into the new database.To delete an OLE storage, fetch the record containing the binary data, set the Data column in the \_Storages table to null, and then update the record.</span></span> <span data-ttu-id="84118-133">Un metodo alternativo consiste nel semplicemente eliminare il record utilizzando [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) o una query SQL semplice.</span><span class="sxs-lookup"><span data-stu-id="84118-133">An alternative method is to simply delete the record using either [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) or a plain SQL query.</span></span>

<span data-ttu-id="84118-134">Per rinominare una risorsa di archiviazione OLE, aggiornare la colonna Name del record.</span><span class="sxs-lookup"><span data-stu-id="84118-134">To rename an OLE storage, update the Name column of the record.</span></span>

<span data-ttu-id="84118-135">Se in questa tabella viene posizionata un'attesa utilizzando SQL (ALTER TABLE</span><span class="sxs-lookup"><span data-stu-id="84118-135">If a hold is placed on this table using SQL (ALTER TABLE</span></span> <table> <span data-ttu-id="84118-136">In attesa) o viene aggiunta una colonna con l'ESENZIONe, la tabella deve essere rilasciata usando FREE.</span><span class="sxs-lookup"><span data-stu-id="84118-136">HOLD) or a column is added with HOLD, the table must be released using FREE.</span></span> <span data-ttu-id="84118-137">Le archiviazioni non vengono scritte finché la tabella non viene rilasciata o sottoposta a commit.</span><span class="sxs-lookup"><span data-stu-id="84118-137">Storages are not written until the table has been released or committed.</span></span>

 

 



