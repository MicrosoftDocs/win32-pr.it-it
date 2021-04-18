---
description: L'oggetto View rappresenta un set di risultati ottenuto durante l'elaborazione di una query utilizzando il metodo OpenView dell'oggetto di database.
ms.assetid: d9d6583a-1cf3-4c33-a851-83e862e2338e
title: Oggetto View
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c26cfa3c4873913d70fca63537f1d25532648a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329231"
---
# <a name="view-object"></a><span data-ttu-id="db3df-103">Oggetto View</span><span class="sxs-lookup"><span data-stu-id="db3df-103">View object</span></span>

<span data-ttu-id="db3df-104">L'oggetto **View** rappresenta un set di risultati ottenuto durante l'elaborazione di una query utilizzando il metodo [**OpenView**](database-openview.md) dell'oggetto di [**database**](database-object.md) .</span><span class="sxs-lookup"><span data-stu-id="db3df-104">The **View** object represents a result set obtained when processing a query using the [**OpenView**](database-openview.md) method of the [**Database**](database-object.md) object.</span></span> <span data-ttu-id="db3df-105">Prima di poter trasferire i dati, la query deve essere eseguita utilizzando il metodo [**Execute**](view-execute.md) , passandogli tutti i parametri sostituibili designati all'interno della stringa di query SQL.</span><span class="sxs-lookup"><span data-stu-id="db3df-105">Before any data can be transferred, the query must be executed using the [**Execute**](view-execute.md) method, passing to it all replaceable parameters designated within the SQL query string.</span></span> <span data-ttu-id="db3df-106">La query può essere eseguita di nuovo, con parametri diversi, se necessario, ma solo dopo avere liberato il set di risultati recuperando tutti i record o chiamando il metodo [**Close**](view-close.md) .</span><span class="sxs-lookup"><span data-stu-id="db3df-106">The query may be executed again, with different parameters if needed, but only after freeing the result set either by fetching all the records or by calling the [**Close**](view-close.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="db3df-107">Membri</span><span class="sxs-lookup"><span data-stu-id="db3df-107">Members</span></span>

<span data-ttu-id="db3df-108">L'oggetto **View** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="db3df-108">The **View** object has these types of members:</span></span>

-   [<span data-ttu-id="db3df-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="db3df-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="db3df-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="db3df-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="db3df-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="db3df-111">Methods</span></span>

<span data-ttu-id="db3df-112">L'oggetto **View** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="db3df-112">The **View** object has these methods.</span></span>



| <span data-ttu-id="db3df-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="db3df-113">Method</span></span>                            | <span data-ttu-id="db3df-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db3df-114">Description</span></span>                                                                                                                                                                     |
|:----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="db3df-115">**Chiudi**</span><span class="sxs-lookup"><span data-stu-id="db3df-115">**Close**</span></span>](view-close.md)       | <span data-ttu-id="db3df-116">Termina l'esecuzione della query e rilascia le risorse di database.</span><span class="sxs-lookup"><span data-stu-id="db3df-116">Terminates query execution and releases database resources.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="db3df-117">**Execute**</span><span class="sxs-lookup"><span data-stu-id="db3df-117">**Execute**</span></span>](view-execute.md)   | <span data-ttu-id="db3df-118">Usa il token punto interrogativo per rappresentare i parametri in una query SQL.</span><span class="sxs-lookup"><span data-stu-id="db3df-118">Uses the question mark token to represent parameters in a SQL query.</span></span> <span data-ttu-id="db3df-119">I valori di questi parametri vengono passati come campi corrispondenti di un record di parametri.</span><span class="sxs-lookup"><span data-stu-id="db3df-119">The values of these parameters are passed in as the corresponding fields of a parameter record.</span></span><br/> |
| [<span data-ttu-id="db3df-120">**Prendere**</span><span class="sxs-lookup"><span data-stu-id="db3df-120">**Fetch**</span></span>](view-fetch.md)       | <span data-ttu-id="db3df-121">Restituisce un oggetto [**record**](record-object.md) contenente i dati della colonna richiesta se nel set di risultati sono disponibili più righe. in caso contrario, restituisce null.</span><span class="sxs-lookup"><span data-stu-id="db3df-121">Returns a [**Record**](record-object.md) object containing the requested column data if more rows are available in the result set, otherwise, it returns null.</span></span><br/>      |
| [<span data-ttu-id="db3df-122">**GetError**</span><span class="sxs-lookup"><span data-stu-id="db3df-122">**GetError**</span></span>](view-geterror.md) | <span data-ttu-id="db3df-123">Restituisce l'errore di convalida e il nome della colonna per cui si è verificato l'errore.</span><span class="sxs-lookup"><span data-stu-id="db3df-123">Returns the Validation error and column name for which the error occurred.</span></span><br/>                                                                                           |
| [<span data-ttu-id="db3df-124">**Modificare**</span><span class="sxs-lookup"><span data-stu-id="db3df-124">**Modify**</span></span>](view-modify.md)     | <span data-ttu-id="db3df-125">Modifica una riga di database con un oggetto [**record**](record-object.md) modificato ottenuto dal metodo [**Fetch**](view-fetch.md) .</span><span class="sxs-lookup"><span data-stu-id="db3df-125">Modifies a database row with a modified [**Record**](record-object.md) object obtained by the [**Fetch**](view-fetch.md) method.</span></span><br/>                                   |



 

### <a name="properties"></a><span data-ttu-id="db3df-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="db3df-126">Properties</span></span>

<span data-ttu-id="db3df-127">L'oggetto **View** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="db3df-127">The **View** object has these properties.</span></span>



| <span data-ttu-id="db3df-128">Proprietà</span><span class="sxs-lookup"><span data-stu-id="db3df-128">Property</span></span>                                         | <span data-ttu-id="db3df-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db3df-129">Description</span></span>                                                                                                                           |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="db3df-130">**ColumnInfo**</span><span class="sxs-lookup"><span data-stu-id="db3df-130">**ColumnInfo**</span></span>](view-columninfo.md)<br/> | <span data-ttu-id="db3df-131">Restituisce un oggetto [**record**](record-object.md) contenente le informazioni richieste su ogni colonna nel set di risultati.</span><span class="sxs-lookup"><span data-stu-id="db3df-131">Returns a [**Record**](record-object.md) object containing the requested information about each column in the result set.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="db3df-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db3df-132">Requirements</span></span>



| <span data-ttu-id="db3df-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="db3df-133">Requirement</span></span> | <span data-ttu-id="db3df-134">Valore</span><span class="sxs-lookup"><span data-stu-id="db3df-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db3df-135">Versione</span><span class="sxs-lookup"><span data-stu-id="db3df-135">Version</span></span><br/> | <span data-ttu-id="db3df-136">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="db3df-136">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="db3df-137">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="db3df-137">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="db3df-138">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="db3df-138">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="db3df-139">DLL</span><span class="sxs-lookup"><span data-stu-id="db3df-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="db3df-140"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db3df-140"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="db3df-141">IID</span><span class="sxs-lookup"><span data-stu-id="db3df-141">IID</span></span><br/>     | <span data-ttu-id="db3df-142">IID \_ iView è definito come 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="db3df-142">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="db3df-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db3df-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db3df-144">Esempi di script di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="db3df-144">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




