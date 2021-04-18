---
description: Il metodo OpenDatabase dell'oggetto Installer apre un database esistente o ne crea uno nuovo, restituendo un oggetto di database. Se non è possibile creare e aprire correttamente l'oggetto di database, viene generato un errore.
ms.assetid: a77b3954-db27-41a0-8f8b-2654766bde6a
title: Installer. OpenDatabase, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenDatabase
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 13256f0bbe2d5adad61c46ea091e8207f1a9351b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324610"
---
# <a name="installeropendatabase-method"></a><span data-ttu-id="e733b-104">Installer. OpenDatabase, metodo</span><span class="sxs-lookup"><span data-stu-id="e733b-104">Installer.OpenDatabase method</span></span>

<span data-ttu-id="e733b-105">Il metodo **OpenDatabase** dell'oggetto [**Installer**](installer-object.md) apre un database esistente o ne crea uno nuovo, restituendo un oggetto di [**database**](database-object.md) .</span><span class="sxs-lookup"><span data-stu-id="e733b-105">The **OpenDatabase** method of the [**Installer**](installer-object.md) object opens an existing database or creates a new one, returning a [**Database**](database-object.md) object.</span></span> <span data-ttu-id="e733b-106">Se non è possibile creare e aprire correttamente l'oggetto di **database** , viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="e733b-106">It generates an error if the **Database** object cannot be successfully created and opened.</span></span>

## <a name="syntax"></a><span data-ttu-id="e733b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e733b-107">Syntax</span></span>


```JScript
Installer.OpenDatabase(
  name,
  openMode
)
```



## <a name="parameters"></a><span data-ttu-id="e733b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e733b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e733b-109">*nome*</span><span class="sxs-lookup"><span data-stu-id="e733b-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="e733b-110">Stringa obbligatoria che contiene il nome del percorso del database.</span><span class="sxs-lookup"><span data-stu-id="e733b-110">Required string that contains the path name of the database.</span></span> <span data-ttu-id="e733b-111">Se viene fornita una stringa vuota, viene creato un database temporaneo che non viene reso permanente.</span><span class="sxs-lookup"><span data-stu-id="e733b-111">If an empty string is supplied, a temporary database is created that is not persisted.</span></span>

</dd> <dt>

<span data-ttu-id="e733b-112">*openMode*</span><span class="sxs-lookup"><span data-stu-id="e733b-112">*openMode*</span></span> 
</dt> <dd>

<span data-ttu-id="e733b-113">Un parametro dell'elenco seguente o una stringa che contiene il nome del percorso del nuovo file di database di output in cui scrivere al momento del commit.</span><span class="sxs-lookup"><span data-stu-id="e733b-113">A parameter from the following list or a string that contains the path name of the new output database file that is to be written to upon commit.</span></span>



| <span data-ttu-id="e733b-114">Parametro</span><span class="sxs-lookup"><span data-stu-id="e733b-114">Parameter</span></span>                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="e733b-115">Significato</span><span class="sxs-lookup"><span data-stu-id="e733b-115">Meaning</span></span>                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiOpenDatabaseModeReadOnly"></span><span id="msiopendatabasemodereadonly"></span><span id="MSIOPENDATABASEMODEREADONLY"></span><dl> <span data-ttu-id="e733b-116"><dt>**msiOpenDatabaseModeReadOnly**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e733b-116"><dt>**msiOpenDatabaseModeReadOnly**</dt> <dt>0</dt></span></span> </dl>                 | <span data-ttu-id="e733b-117">Apre un database di sola lettura, senza modifiche permanenti.</span><span class="sxs-lookup"><span data-stu-id="e733b-117">Opens a database read-only, no persistent changes.</span></span><br/>                                                                                                           |
| <span id="msiOpenDatabaseModeTransact"></span><span id="msiopendatabasemodetransact"></span><span id="MSIOPENDATABASEMODETRANSACT"></span><dl> <span data-ttu-id="e733b-118"><dt>**msiOpenDatabaseModeTransact**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e733b-118"><dt>**msiOpenDatabaseModeTransact**</dt> <dt>1</dt></span></span> </dl>                 | <span data-ttu-id="e733b-119">Apre un database di lettura/scrittura in modalità transazione.</span><span class="sxs-lookup"><span data-stu-id="e733b-119">Opens a database read/write in transaction mode.</span></span><br/>                                                                                                             |
| <span id="msiOpenDatabaseModeDirect"></span><span id="msiopendatabasemodedirect"></span><span id="MSIOPENDATABASEMODEDIRECT"></span><dl> <span data-ttu-id="e733b-120"><dt>**msiOpenDatabaseModeDirect**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e733b-120"><dt>**msiOpenDatabaseModeDirect**</dt> <dt>2</dt></span></span> </dl>                         | <span data-ttu-id="e733b-121">Apre una lettura/scrittura diretta del database senza transazione.</span><span class="sxs-lookup"><span data-stu-id="e733b-121">Opens a database direct read/write without transaction.</span></span><br/>                                                                                                      |
| <span id="msiOpenDatabaseModeCreate"></span><span id="msiopendatabasemodecreate"></span><span id="MSIOPENDATABASEMODECREATE"></span><dl> <span data-ttu-id="e733b-122"><dt>**msiOpenDatabaseModeCreate**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e733b-122"><dt>**msiOpenDatabaseModeCreate**</dt> <dt>3</dt></span></span> </dl>                         | <span data-ttu-id="e733b-123">Consente di creare un nuovo database, in modalità Transact-lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e733b-123">Creates a new database, transact mode read/write.</span></span><br/>                                                                                                            |
| <span id="msiOpenDatabaseModeCreateDirect"></span><span id="msiopendatabasemodecreatedirect"></span><span id="MSIOPENDATABASEMODECREATEDIRECT"></span><dl> <span data-ttu-id="e733b-124"><dt>**msiOpenDatabaseModeCreateDirect**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e733b-124"><dt>**msiOpenDatabaseModeCreateDirect**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="e733b-125">Crea un nuovo database, modalità diretta di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e733b-125">Creates a new database, direct mode read/write.</span></span><br/>                                                                                                              |
| <span id="msiOpenDatabaseModeListScript"></span><span id="msiopendatabasemodelistscript"></span><span id="MSIOPENDATABASEMODELISTSCRIPT"></span><dl> <span data-ttu-id="e733b-126"><dt>**msiOpenDatabaseModeListScript**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e733b-126"><dt>**msiOpenDatabaseModeListScript**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="e733b-127">Apre un database per visualizzare i file di script di annuncio, ad esempio i file generati dal metodo [**CreateAdvertiseScript**](installer-createadvertisescript.md) .</span><span class="sxs-lookup"><span data-stu-id="e733b-127">Opens a database to view advertise script files, such as the files generated by the [**CreateAdvertiseScript**](installer-createadvertisescript.md) method.</span></span><br/> |
| <span id="msiOpenDatabaseModePatchFile"></span><span id="msiopendatabasemodepatchfile"></span><span id="MSIOPENDATABASEMODEPATCHFILE"></span><dl> <span data-ttu-id="e733b-128"><dt>**msiOpenDatabaseModePatchFile**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="e733b-128"><dt>**msiOpenDatabaseModePatchFile**</dt> <dt>32</dt></span></span> </dl>            | <span data-ttu-id="e733b-129">Aggiunge questo flag per indicare un file di correzione.</span><span class="sxs-lookup"><span data-stu-id="e733b-129">Adds this flag to indicate a patch file.</span></span><br/>                                                                                                                     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e733b-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e733b-130">Return value</span></span>

<span data-ttu-id="e733b-131">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e733b-131">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e733b-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="e733b-132">Remarks</span></span>

<span data-ttu-id="e733b-133">Quando un database viene aperto come output di un altro database, il flusso di informazioni di riepilogo del database di output è effettivamente un mirror di sola lettura del database originale e pertanto non può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="e733b-133">When a database is opened as the output of another database, the summary information stream of the output database is actually a read-only mirror of the original database and thus cannot be changed.</span></span> <span data-ttu-id="e733b-134">Inoltre, non viene reso permanente con il database.</span><span class="sxs-lookup"><span data-stu-id="e733b-134">Additionally, it is not persisted with the database.</span></span> <span data-ttu-id="e733b-135">Per creare o modificare le informazioni di riepilogo per il database di output, è necessario chiuderlo e riaprirlo.</span><span class="sxs-lookup"><span data-stu-id="e733b-135">To create or modify the summary information for the output database it must be closed and reopened.</span></span>

<span data-ttu-id="e733b-136">Per creare e salvare le modifiche apportate a un database, aprire innanzitutto il database nella modalità transazione (msiOpenDatabaseModeTransact), create (msiOpenDatabaseModeCreate o msiOpenDatabaseModeCreateDirect) o Direct (msiOpenDatabaseModeDirect).</span><span class="sxs-lookup"><span data-stu-id="e733b-136">To make and save changes to a database first open the database in transaction (msiOpenDatabaseModeTransact), create (msiOpenDatabaseModeCreate or msiOpenDatabaseModeCreateDirect), or direct (msiOpenDatabaseModeDirect) mode.</span></span> <span data-ttu-id="e733b-137">Dopo avere apportato le modifiche, chiamare sempre il metodo [**commit**](database-commit.md) prima di chiudere l'handle di database.</span><span class="sxs-lookup"><span data-stu-id="e733b-137">After making the changes, always call the [**Commit**](database-commit.md) method before closing the database handle.</span></span> <span data-ttu-id="e733b-138">Il metodo **commit** Scarica tutti i buffer.</span><span class="sxs-lookup"><span data-stu-id="e733b-138">The **Commit** method flushes all buffers.</span></span>

<span data-ttu-id="e733b-139">Chiamare sempre il metodo [**commit**](database-commit.md) su un database aperto in modalità diretta (MsiOpenDatabaseModeDirect o msiOpenDatabaseModeCreateDirect) prima di chiudere il database.</span><span class="sxs-lookup"><span data-stu-id="e733b-139">Always call the [**Commit**](database-commit.md) method on a database that has been opened in direct mode (msiOpenDatabaseModeDirect or msiOpenDatabaseModeCreateDirect) before closing the database.</span></span> <span data-ttu-id="e733b-140">In caso contrario, è possibile che il database sia danneggiato.</span><span class="sxs-lookup"><span data-stu-id="e733b-140">Failure to do this may corrupt the database.</span></span>

<span data-ttu-id="e733b-141">Poiché il metodo **OpenDatabase** avvia l'accesso al database, non può essere utilizzato con un'installazione in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e733b-141">Because the **OpenDatabase** method initiates database access, it cannot be used with a running installation.</span></span>

<span data-ttu-id="e733b-142">Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="e733b-142">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e733b-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e733b-143">Requirements</span></span>



| <span data-ttu-id="e733b-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="e733b-144">Requirement</span></span> | <span data-ttu-id="e733b-145">Valore</span><span class="sxs-lookup"><span data-stu-id="e733b-145">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e733b-146">Versione</span><span class="sxs-lookup"><span data-stu-id="e733b-146">Version</span></span><br/> | <span data-ttu-id="e733b-147">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e733b-147">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e733b-148">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e733b-148">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e733b-149">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="e733b-149">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e733b-150">DLL</span><span class="sxs-lookup"><span data-stu-id="e733b-150">DLL</span></span><br/>     | <dl> <span data-ttu-id="e733b-151"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e733b-151"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e733b-152">IID</span><span class="sxs-lookup"><span data-stu-id="e733b-152">IID</span></span><br/>     | <span data-ttu-id="e733b-153">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e733b-153">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




