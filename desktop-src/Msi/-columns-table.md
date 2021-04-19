---
description: La \_ tabella Columns è una tabella di sistema di sola lettura che contiene il catalogo delle colonne. Vengono elencate le colonne per tutte le tabelle. È possibile eseguire una query su questa tabella per determinare se esiste una determinata colonna.
ms.assetid: 1ddde4e2-90a9-4dd8-a4f9-b6802d0b11cf
title: Tabella _Columns
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d896f330e5fc2e13b5f172581341eb11a09617d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311119"
---
# <a name="_columns-table"></a><span data-ttu-id="86f0d-105">\_Tabella colonne</span><span class="sxs-lookup"><span data-stu-id="86f0d-105">\_Columns Table</span></span>

<span data-ttu-id="86f0d-106">La \_ tabella Columns è una tabella di sistema di sola lettura che contiene il catalogo delle colonne.</span><span class="sxs-lookup"><span data-stu-id="86f0d-106">The \_Columns table is a read-only system table that contains the column catalog.</span></span> <span data-ttu-id="86f0d-107">Vengono elencate le colonne per tutte le tabelle.</span><span class="sxs-lookup"><span data-stu-id="86f0d-107">It lists the columns for all the tables.</span></span> <span data-ttu-id="86f0d-108">È possibile eseguire una query su questa tabella per determinare se esiste una determinata colonna.</span><span class="sxs-lookup"><span data-stu-id="86f0d-108">You can query this table to find out if a given column exists.</span></span>

<span data-ttu-id="86f0d-109">La \_ tabella Columns contiene le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="86f0d-109">The \_Columns table has the following columns.</span></span>



| <span data-ttu-id="86f0d-110">Colonna</span><span class="sxs-lookup"><span data-stu-id="86f0d-110">Column</span></span> | <span data-ttu-id="86f0d-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="86f0d-111">Type</span></span>                   | <span data-ttu-id="86f0d-112">Chiave</span><span class="sxs-lookup"><span data-stu-id="86f0d-112">Key</span></span> | <span data-ttu-id="86f0d-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="86f0d-113">Nullable</span></span> |
|--------|------------------------|-----|----------|
| <span data-ttu-id="86f0d-114">Tabella</span><span class="sxs-lookup"><span data-stu-id="86f0d-114">Table</span></span>  | [<span data-ttu-id="86f0d-115">Text</span><span class="sxs-lookup"><span data-stu-id="86f0d-115">Text</span></span>](text.md)       | <span data-ttu-id="86f0d-116">S</span><span class="sxs-lookup"><span data-stu-id="86f0d-116">Y</span></span>   | <span data-ttu-id="86f0d-117">N</span><span class="sxs-lookup"><span data-stu-id="86f0d-117">N</span></span>        |
| <span data-ttu-id="86f0d-118">Number</span><span class="sxs-lookup"><span data-stu-id="86f0d-118">Number</span></span> | [<span data-ttu-id="86f0d-119">Integer</span><span class="sxs-lookup"><span data-stu-id="86f0d-119">Integer</span></span>](integer.md) | <span data-ttu-id="86f0d-120">S</span><span class="sxs-lookup"><span data-stu-id="86f0d-120">Y</span></span>   | <span data-ttu-id="86f0d-121">N</span><span class="sxs-lookup"><span data-stu-id="86f0d-121">N</span></span>        |
| <span data-ttu-id="86f0d-122">Nome</span><span class="sxs-lookup"><span data-stu-id="86f0d-122">Name</span></span>   | [<span data-ttu-id="86f0d-123">Text</span><span class="sxs-lookup"><span data-stu-id="86f0d-123">Text</span></span>](text.md)       | <span data-ttu-id="86f0d-124">N</span><span class="sxs-lookup"><span data-stu-id="86f0d-124">N</span></span>   | <span data-ttu-id="86f0d-125">N</span><span class="sxs-lookup"><span data-stu-id="86f0d-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="86f0d-126">Colonne</span><span class="sxs-lookup"><span data-stu-id="86f0d-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="86f0d-127"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>tavolo</span><span class="sxs-lookup"><span data-stu-id="86f0d-127"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="86f0d-128">Nome della tabella che contiene la colonna.</span><span class="sxs-lookup"><span data-stu-id="86f0d-128">The name of the table that contains the column.</span></span>

</dd> <dt>

<span data-ttu-id="86f0d-129"><span id="Number"></span><span id="number"></span><span id="NUMBER"></span>Numero</span><span class="sxs-lookup"><span data-stu-id="86f0d-129"><span id="Number"></span><span id="number"></span><span id="NUMBER"></span>Number</span></span>
</dt> <dd>

<span data-ttu-id="86f0d-130">Ordine della colonna all'interno della tabella.</span><span class="sxs-lookup"><span data-stu-id="86f0d-130">The order of the column within the table.</span></span>

</dd> <dt>

<span data-ttu-id="86f0d-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome</span><span class="sxs-lookup"><span data-stu-id="86f0d-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="86f0d-132">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="86f0d-132">The name of the column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86f0d-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="86f0d-133">Remarks</span></span>

<span data-ttu-id="86f0d-134">Poiché la \_ tabella Columns è una tabella di sistema che non può essere modificata tramite query SQL, non è possibile ottenere le chiavi primarie con la funzione [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) o la [**Proprietà PrimaryKeys**](database-primarykeys.md).</span><span class="sxs-lookup"><span data-stu-id="86f0d-134">Because the \_Columns table is a system table that cannot be modified through SQL queries, you cannot obtain the primary keys with the [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) function or the [**PrimaryKeys property**](database-primarykeys.md).</span></span>

<span data-ttu-id="86f0d-135">Nella tabella Columns sono archiviate solo le colonne permanenti \_ .</span><span class="sxs-lookup"><span data-stu-id="86f0d-135">Only persistent columns are stored in the \_Columns table.</span></span> <span data-ttu-id="86f0d-136">Per determinare se esiste una colonna temporanea, è necessario creare una vista usando un'istruzione SELECT sulla \* tabella, quindi eseguire il ciclo di tutti i campi di un record restituito dalla funzione [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) con l' \_ opzione MSICOLINFO names.</span><span class="sxs-lookup"><span data-stu-id="86f0d-136">To determine if a temporary column exists one would need to create a view using a SELECT \* statement against the table, then loop through all fields in a record returned by the [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) function with the MSICOLINFO\_NAMES option.</span></span>

 

 



