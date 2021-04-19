---
description: L'oggetto di database accede a un database del programma di installazione.
ms.assetid: 97765884-3e1c-486a-932c-6430b113fac8
title: Oggetto di database
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5b47e4678d9475abe90c4b55d6adb514314dcc0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333059"
---
# <a name="database-object"></a><span data-ttu-id="efcd6-103">Oggetto di database</span><span class="sxs-lookup"><span data-stu-id="efcd6-103">Database object</span></span>

<span data-ttu-id="efcd6-104">L'oggetto di **database** accede a un database del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="efcd6-104">The **Database** object accesses an installer database.</span></span>

<span data-ttu-id="efcd6-105">L'oggetto di **database** viene rilasciato quando viene ricavato dall'ambito o quando la variabile oggetto associata è impostata su null.</span><span class="sxs-lookup"><span data-stu-id="efcd6-105">The **Database** object is released when it is either taken out of scope or when the object variable associated with it is set to null.</span></span> <span data-ttu-id="efcd6-106">È necessario chiamare il metodo [**commit**](database-commit.md) prima che l'oggetto di **database** venga rilasciato per scrivere tutte le modifiche permanenti.</span><span class="sxs-lookup"><span data-stu-id="efcd6-106">The [**Commit**](database-commit.md) method must be called before the **Database** object is released to write out all persistent changes.</span></span> <span data-ttu-id="efcd6-107">Se il metodo **commit** non viene chiamato, il programma di installazione esegue un rollback implicito alla distruzione degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="efcd6-107">If the **Commit** method is not called, the installer performs an implicit rollback upon object destruction.</span></span>

<span data-ttu-id="efcd6-108">Il client può utilizzare la procedura seguente per l'accesso ai dati.</span><span class="sxs-lookup"><span data-stu-id="efcd6-108">The client can use the following procedure for data access.</span></span>

<span data-ttu-id="efcd6-109">**Per eseguire query sulla sequenziazione dell'API**</span><span class="sxs-lookup"><span data-stu-id="efcd6-109">**To Query API Sequencing**</span></span>

1.  <span data-ttu-id="efcd6-110">Ottenere un oggetto di **database** chiamando il [**OpenDatabase**](installer-opendatabase.md) o l'oggetto del [**programma di installazione**](installer-object.md) .</span><span class="sxs-lookup"><span data-stu-id="efcd6-110">Obtain a **Database** object by calling the [**OpenDatabase**](installer-opendatabase.md) or the [**Installer**](installer-object.md) object.</span></span>
2.  <span data-ttu-id="efcd6-111">Avviare una query utilizzando una stringa SQL chiamando il metodo [**OpenView**](database-openview.md) dell'oggetto di **database** .</span><span class="sxs-lookup"><span data-stu-id="efcd6-111">Initiate a query using a SQL string by calling the [**OpenView**](database-openview.md) method of the **Database** object.</span></span>
3.  <span data-ttu-id="efcd6-112">Impostare i parametri di query in un oggetto [**record**](record-object.md) ed eseguire la query di database chiamando il metodo [**Execute**](view-execute.md) dell'oggetto [**View**](view-object.md) .</span><span class="sxs-lookup"><span data-stu-id="efcd6-112">Set query parameters in a [**Record**](record-object.md) object and execute the database query by calling the [**Execute**](view-execute.md) method of the [**View**](view-object.md) object.</span></span> <span data-ttu-id="efcd6-113">Viene generato un risultato che può essere recuperato o aggiornato.</span><span class="sxs-lookup"><span data-stu-id="efcd6-113">This produces a result that can be fetched or updated.</span></span>
4.  <span data-ttu-id="efcd6-114">Chiamare ripetutamente il metodo [**Fetch**](view-fetch.md) dell'oggetto [**View**](view-object.md) per restituire gli oggetti [**record**](record-object.md) .</span><span class="sxs-lookup"><span data-stu-id="efcd6-114">Call the [**Fetch**](view-fetch.md) method of the [**View**](view-object.md) object repeatedly to return [**Record**](record-object.md) objects.</span></span>
5.  <span data-ttu-id="efcd6-115">Aggiornare le righe del database di un oggetto [**record**](record-object.md) ottenuto dal metodo [**Fetch**](view-fetch.md) utilizzando il metodo [**Modify**](view-modify.md) dell'oggetto [**View**](view-object.md) .</span><span class="sxs-lookup"><span data-stu-id="efcd6-115">Update database rows of a [**Record**](record-object.md) object obtained by the [**Fetch**](view-fetch.md) method using the [**Modify**](view-modify.md) method of the [**View**](view-object.md) object.</span></span>
6.  <span data-ttu-id="efcd6-116">Rilasciare la query e tutti i record non recuperati chiamando il metodo [**Close**](view-close.md) dell'oggetto [**View**](view-object.md) .</span><span class="sxs-lookup"><span data-stu-id="efcd6-116">Release the query and any unfetched records by calling the [**Close**](view-close.md) method of the [**View**](view-object.md) object.</span></span>
7.  <span data-ttu-id="efcd6-117">Consente di salvare in modo permanente eventuali aggiornamenti del database chiamando il metodo [**commit**](database-commit.md) dell'oggetto di **database** .</span><span class="sxs-lookup"><span data-stu-id="efcd6-117">Persist any database updates by calling the [**Commit**](database-commit.md) method of the **Database** object.</span></span>

## <a name="members"></a><span data-ttu-id="efcd6-118">Membri</span><span class="sxs-lookup"><span data-stu-id="efcd6-118">Members</span></span>

<span data-ttu-id="efcd6-119">L'oggetto di **database** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="efcd6-119">The **Database** object has these types of members:</span></span>

-   [<span data-ttu-id="efcd6-120">Metodi</span><span class="sxs-lookup"><span data-stu-id="efcd6-120">Methods</span></span>](#methods)
-   [<span data-ttu-id="efcd6-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="efcd6-121">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="efcd6-122">Metodi</span><span class="sxs-lookup"><span data-stu-id="efcd6-122">Methods</span></span>

<span data-ttu-id="efcd6-123">Questi metodi sono disponibili nell'oggetto di **database** .</span><span class="sxs-lookup"><span data-stu-id="efcd6-123">The **Database** object has these methods.</span></span>



| <span data-ttu-id="efcd6-124">Metodo</span><span class="sxs-lookup"><span data-stu-id="efcd6-124">Method</span></span>                                                                    | <span data-ttu-id="efcd6-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="efcd6-125">Description</span></span>                                                                                                                                                               |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="efcd6-126">**ApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="efcd6-126">**ApplyTransform**</span></span>](database-applytransform.md)                         | <span data-ttu-id="efcd6-127">Applica la trasformazione al database.</span><span class="sxs-lookup"><span data-stu-id="efcd6-127">Applies the transform to this database.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="efcd6-128">**Commit**</span><span class="sxs-lookup"><span data-stu-id="efcd6-128">**Commit**</span></span>](database-commit.md)                                         | <span data-ttu-id="efcd6-129">Completa il form persistente del database.</span><span class="sxs-lookup"><span data-stu-id="efcd6-129">Finalizes the persistent form of the database.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="efcd6-130">**CreateTransformSummaryInfo**</span><span class="sxs-lookup"><span data-stu-id="efcd6-130">**CreateTransformSummaryInfo**</span></span>](database-createtransformsummaryinfo.md) | <span data-ttu-id="efcd6-131">Crea e popola il flusso di informazioni di riepilogo di un file di trasformazione esistente.</span><span class="sxs-lookup"><span data-stu-id="efcd6-131">Creates and populates the summary information stream of an existing transform file.</span></span><br/>                                                                            |
| [<span data-ttu-id="efcd6-132">**EnableUIPreview**</span><span class="sxs-lookup"><span data-stu-id="efcd6-132">**EnableUIPreview**</span></span>](database-enableuipreview.md)                       | <span data-ttu-id="efcd6-133">Semplifica la creazione di finestre di dialogo e cartelloni, fornendo il supporto necessario per visualizzare le finestre di dialogo dell'interfaccia utente archiviate nel database del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="efcd6-133">Facilitates the authoring of dialog boxes and billboards by providing the support needed to view user interface dialog boxes stored in the installer database.</span></span><br/> |
| [<span data-ttu-id="efcd6-134">**Esportazione**</span><span class="sxs-lookup"><span data-stu-id="efcd6-134">**Export**</span></span>](database-export.md)                                         | <span data-ttu-id="efcd6-135">Copia la struttura e i dati da una tabella specificata in un file di archivio di testo.</span><span class="sxs-lookup"><span data-stu-id="efcd6-135">Copies the structure and data from a specified table to a text archive file.</span></span><br/>                                                                                   |
| [<span data-ttu-id="efcd6-136">**GenerateTransform**</span><span class="sxs-lookup"><span data-stu-id="efcd6-136">**GenerateTransform**</span></span>](database-generatetransform.md)                   | <span data-ttu-id="efcd6-137">Crea una trasformazione.</span><span class="sxs-lookup"><span data-stu-id="efcd6-137">Creates a transform.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="efcd6-138">**Importa**</span><span class="sxs-lookup"><span data-stu-id="efcd6-138">**Import**</span></span>](database-import.md)                                         | <span data-ttu-id="efcd6-139">Importa una tabella di database da un file di archivio di testo.</span><span class="sxs-lookup"><span data-stu-id="efcd6-139">Imports a database table from a text archive file.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="efcd6-140">**Unione**</span><span class="sxs-lookup"><span data-stu-id="efcd6-140">**Merge**</span></span>](database-merge.md)                                           | <span data-ttu-id="efcd6-141">Unisce il database di riferimento al database di base.</span><span class="sxs-lookup"><span data-stu-id="efcd6-141">Merges the reference database with the base database.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="efcd6-142">**OpenView**</span><span class="sxs-lookup"><span data-stu-id="efcd6-142">**OpenView**</span></span>](database-openview.md)                                     | <span data-ttu-id="efcd6-143">Restituisce un oggetto [**visualizzazione**](view-object.md) che rappresenta la query specificata da una stringa SQL.</span><span class="sxs-lookup"><span data-stu-id="efcd6-143">Returns a [**View**](view-object.md) object representing the query specified by a SQL string.</span></span><br/>                                                                 |



 

### <a name="properties"></a><span data-ttu-id="efcd6-144">Proprietà</span><span class="sxs-lookup"><span data-stu-id="efcd6-144">Properties</span></span>

<span data-ttu-id="efcd6-145">L'oggetto di **database** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="efcd6-145">The **Database** object has these properties.</span></span>



| <span data-ttu-id="efcd6-146">Proprietà</span><span class="sxs-lookup"><span data-stu-id="efcd6-146">Property</span></span>                                                                               | <span data-ttu-id="efcd6-147">Descrizione</span><span class="sxs-lookup"><span data-stu-id="efcd6-147">Description</span></span>                                                                                                                                                      |
|:---------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="efcd6-148">**DatabaseState**</span><span class="sxs-lookup"><span data-stu-id="efcd6-148">**DatabaseState**</span></span>](database-databasestate.md)<br/>                             | <span data-ttu-id="efcd6-149">Restituisce lo stato di persistenza del database.</span><span class="sxs-lookup"><span data-stu-id="efcd6-149">Returns the persistence state of the database.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="efcd6-150">**PrimaryKeys**</span><span class="sxs-lookup"><span data-stu-id="efcd6-150">**PrimaryKeys**</span></span>](database-primarykeys.md)<br/>                                 | <span data-ttu-id="efcd6-151">Restituisce un oggetto [**record**](record-object.md) contenente il nome della tabella e i nomi delle colonne (incluse le chiavi primarie).</span><span class="sxs-lookup"><span data-stu-id="efcd6-151">Returns a [**Record**](record-object.md) object containing the table name and the column names (comprising the primary keys).</span></span><br/>                        |
| [<span data-ttu-id="efcd6-152">**SummaryInformation (oggetto di database)**</span><span class="sxs-lookup"><span data-stu-id="efcd6-152">**SummaryInformation (Database Object)**</span></span>](database-summaryinformation.md)<br/> | <span data-ttu-id="efcd6-153">Restituisce un oggetto [**SummaryInfo**](summaryinfo-object.md) che può essere utilizzato per esaminare, aggiornare e aggiungere proprietà al flusso di informazioni di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="efcd6-153">Returns a [**SummaryInfo**](summaryinfo-object.md) object that can be used to examine, update, and add properties to the summary information stream.</span></span><br/> |
| [<span data-ttu-id="efcd6-154">**TablePersistent**</span><span class="sxs-lookup"><span data-stu-id="efcd6-154">**TablePersistent**</span></span>](database-tablepersistent.md)<br/>                         | <span data-ttu-id="efcd6-155">Restituisce lo stato di persistenza della tabella.</span><span class="sxs-lookup"><span data-stu-id="efcd6-155">Returns the persistence state of the table.</span></span><br/>                                                                                                           |



 

## <a name="requirements"></a><span data-ttu-id="efcd6-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efcd6-156">Requirements</span></span>



| <span data-ttu-id="efcd6-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="efcd6-157">Requirement</span></span> | <span data-ttu-id="efcd6-158">Valore</span><span class="sxs-lookup"><span data-stu-id="efcd6-158">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efcd6-159">Versione</span><span class="sxs-lookup"><span data-stu-id="efcd6-159">Version</span></span><br/> | <span data-ttu-id="efcd6-160">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="efcd6-160">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="efcd6-161">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="efcd6-161">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="efcd6-162">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="efcd6-162">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="efcd6-163">DLL</span><span class="sxs-lookup"><span data-stu-id="efcd6-163">DLL</span></span><br/>     | <dl> <span data-ttu-id="efcd6-164"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efcd6-164"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="efcd6-165">IID</span><span class="sxs-lookup"><span data-stu-id="efcd6-165">IID</span></span><br/>     | <span data-ttu-id="efcd6-166">IID \_ iDatabase è definito come 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="efcd6-166">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="efcd6-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efcd6-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efcd6-168">Esempi di script di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="efcd6-168">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




