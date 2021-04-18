---
description: Il metodo Delete WMI class eliminerà il file o la directory logica specificata nel percorso dell'oggetto.
ms.assetid: 5663b8a8-3089-475b-8a36-454a7315bfca
ms.tgt_platform: multiple
title: Metodo Delete della classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 843583698c11c1b9ad8f08e83aa6e4b894b55db8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305292"
---
# <a name="delete-method-of-the-win32_directory-class"></a><span data-ttu-id="9f5bb-103">Metodo Delete della classe di \_ directory Win32</span><span class="sxs-lookup"><span data-stu-id="9f5bb-103">Delete method of the Win32\_Directory class</span></span>

<span data-ttu-id="9f5bb-104">Il metodo **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) eliminerà il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9f5bb-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method will delete the logical file (or directory) specified in the object path.</span></span>

<span data-ttu-id="9f5bb-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="9f5bb-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9f5bb-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9f5bb-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9f5bb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f5bb-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="9f5bb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f5bb-108">Parameters</span></span>

<span data-ttu-id="9f5bb-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="9f5bb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9f5bb-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9f5bb-110">Return value</span></span>

<span data-ttu-id="9f5bb-111">Restituisce un valore pari a 0 (zero) se il file è stato eliminato correttamente e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="9f5bb-111">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="9f5bb-112">**0**</span><span class="sxs-lookup"><span data-stu-id="9f5bb-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="9f5bb-113">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="9f5bb-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="9f5bb-114">**2**</span><span class="sxs-lookup"><span data-stu-id="9f5bb-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="9f5bb-115">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="9f5bb-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="9f5bb-116">**8**</span><span class="sxs-lookup"><span data-stu-id="9f5bb-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="9f5bb-117">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="9f5bb-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="9f5bb-118">**9**</span><span class="sxs-lookup"><span data-stu-id="9f5bb-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="9f5bb-119">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="9f5bb-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="9f5bb-120">**10**</span><span class="sxs-lookup"><span data-stu-id="9f5bb-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="9f5bb-121">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="9f5bb-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="9f5bb-122">**11**</span><span class="sxs-lookup"><span data-stu-id="9f5bb-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="9f5bb-123">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="9f5bb-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="9f5bb-124">**12**</span><span class="sxs-lookup"><span data-stu-id="9f5bb-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="9f5bb-125">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="9f5bb-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="9f5bb-126">**13**</span><span class="sxs-lookup"><span data-stu-id="9f5bb-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="9f5bb-127">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="9f5bb-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="9f5bb-128">**14**</span><span class="sxs-lookup"><span data-stu-id="9f5bb-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="9f5bb-129">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="9f5bb-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="9f5bb-130">**15**</span><span class="sxs-lookup"><span data-stu-id="9f5bb-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="9f5bb-131">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="9f5bb-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="9f5bb-132">**16**</span><span class="sxs-lookup"><span data-stu-id="9f5bb-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="9f5bb-133">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="9f5bb-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="9f5bb-134">**17**</span><span class="sxs-lookup"><span data-stu-id="9f5bb-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="9f5bb-135">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="9f5bb-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="9f5bb-136">**21**</span><span class="sxs-lookup"><span data-stu-id="9f5bb-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="9f5bb-137">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="9f5bb-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f5bb-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f5bb-138">Remarks</span></span>

<span data-ttu-id="9f5bb-139">Le cartelle non sono necessariamente aggiunte permanenti a una file system.</span><span class="sxs-lookup"><span data-stu-id="9f5bb-139">Folders are not necessarily permanent additions to a file system.</span></span> <span data-ttu-id="9f5bb-140">A un certo punto, potrebbe essere necessario eliminare le cartelle, probabilmente perché non sono più necessarie, perché il ruolo del computer è stato modificato o perché le cartelle sono state create per errore.</span><span class="sxs-lookup"><span data-stu-id="9f5bb-140">At some point, folders might need to be deleted, perhaps because they are no longer required, because the role of the computer has changed, or because the folders were created by mistake.</span></span>

<span data-ttu-id="9f5bb-141">Elimina consente di eliminare le cartelle: è sufficiente associare la cartella in questione e quindi chiamare il metodo Delete.</span><span class="sxs-lookup"><span data-stu-id="9f5bb-141">Delete allows you to delete folders: you simply bind to the folder in question and then call the Delete method.</span></span> <span data-ttu-id="9f5bb-142">Una volta chiamato il metodo Delete, la cartella viene rimossa definitivamente dalla file system; non viene inviato al Cestino.</span><span class="sxs-lookup"><span data-stu-id="9f5bb-142">After the Delete method is called, the folder is permanently removed from the file system; it is not sent to the Recycle Bin.</span></span> <span data-ttu-id="9f5bb-143">Inoltre, non viene inviata alcuna notifica di conferma ("eliminare la cartella?").</span><span class="sxs-lookup"><span data-stu-id="9f5bb-143">In addition, no confirmation notice ("Are you sure you want to delete this folder?") is issued.</span></span> <span data-ttu-id="9f5bb-144">Al contrario, la cartella viene immediatamente rimossa.</span><span class="sxs-lookup"><span data-stu-id="9f5bb-144">Instead, the folder is immediately removed.</span></span>

<span data-ttu-id="9f5bb-145">Non è possibile eliminare le cartelle di sola lettura usando FileSystemObject; Tuttavia, questa operazione può essere eseguita tramite WMI.</span><span class="sxs-lookup"><span data-stu-id="9f5bb-145">You cannot delete read-only folders using the FileSystemObject; however, this can be done using WMI.</span></span> <span data-ttu-id="9f5bb-146">Se lo script utilizza WMI e non si desidera rimuovere una cartella di sola lettura, è necessario utilizzare la proprietà leggibile per verificare lo stato della cartella prima di eliminarla.</span><span class="sxs-lookup"><span data-stu-id="9f5bb-146">If your script uses WMI and you do not want to remove a read-only folder, you must use the Readable property to check the folder status before deleting it.</span></span>

## <a name="examples"></a><span data-ttu-id="9f5bb-147">Esempio</span><span class="sxs-lookup"><span data-stu-id="9f5bb-147">Examples</span></span>

<span data-ttu-id="9f5bb-148">L'esempio di codice VBScript seguente elimina la cartella C: \\ Scripts.</span><span class="sxs-lookup"><span data-stu-id="9f5bb-148">The following VBScript code sample deletes the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Delete
 Wscript.Echo errResults
Next
```



## <a name="requirements"></a><span data-ttu-id="9f5bb-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f5bb-149">Requirements</span></span>



| <span data-ttu-id="9f5bb-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f5bb-150">Requirement</span></span> | <span data-ttu-id="9f5bb-151">Valore</span><span class="sxs-lookup"><span data-stu-id="9f5bb-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f5bb-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f5bb-152">Minimum supported client</span></span><br/> | <span data-ttu-id="9f5bb-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f5bb-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9f5bb-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f5bb-154">Minimum supported server</span></span><br/> | <span data-ttu-id="9f5bb-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f5bb-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9f5bb-156">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9f5bb-156">Namespace</span></span><br/>                | <span data-ttu-id="9f5bb-157">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="9f5bb-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9f5bb-158">MOF</span><span class="sxs-lookup"><span data-stu-id="9f5bb-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f5bb-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f5bb-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f5bb-160">DLL</span><span class="sxs-lookup"><span data-stu-id="9f5bb-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f5bb-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f5bb-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f5bb-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f5bb-162">See also</span></span>

<dl> <dt>

<span data-ttu-id="9f5bb-163">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9f5bb-163">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9f5bb-164">**\_Directory Win32**</span><span class="sxs-lookup"><span data-stu-id="9f5bb-164">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

