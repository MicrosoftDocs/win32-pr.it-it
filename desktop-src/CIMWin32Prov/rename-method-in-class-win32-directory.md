---
description: Rinomina il file di voce di directory specificato nel percorso dell'oggetto.
ms.assetid: 8bfe1b69-5f93-4408-a742-f03a9cb16bfe
ms.tgt_platform: multiple
title: Rinominare il metodo della classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 874151e1ff8c9feca375df3eb441665863d1070d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304437"
---
# <a name="rename-method-of-the-win32_directory-class"></a><span data-ttu-id="22572-103">Rinominare il metodo della \_ classe di directory Win32</span><span class="sxs-lookup"><span data-stu-id="22572-103">Rename method of the Win32\_Directory class</span></span>

<span data-ttu-id="22572-104">Il metodo **Rinomina** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) Rinomina il file di voce di directory specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="22572-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames the directory entry file specified in the object path.</span></span> <span data-ttu-id="22572-105">Una ridenominazione non è supportata se la destinazione si trova in un'altra unità o se è necessario sovrascrivere un file logico esistente.</span><span class="sxs-lookup"><span data-stu-id="22572-105">A rename is not supported if the destination is on another drive or if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="22572-106">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="22572-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="22572-107">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="22572-107">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="22572-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="22572-108">Syntax</span></span>


```mof
uint32 Rename(
   string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="22572-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="22572-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22572-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="22572-110">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="22572-111">Nome completo del nuovo file (o directory).</span><span class="sxs-lookup"><span data-stu-id="22572-111">Fully qualified new name of the file (or directory).</span></span> <span data-ttu-id="22572-112">Esempio: c: \\ temp \\newfile.txt.</span><span class="sxs-lookup"><span data-stu-id="22572-112">Example: c:\\temp\\newfile.txt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22572-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="22572-113">Return value</span></span>

<span data-ttu-id="22572-114">Restituisce un valore pari a 0 (zero) se il file è stato rinominato correttamente e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="22572-114">Returns a value of 0 (zero) if the file was successfully renamed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="22572-115">**0**</span><span class="sxs-lookup"><span data-stu-id="22572-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="22572-116">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="22572-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="22572-117">**2**</span><span class="sxs-lookup"><span data-stu-id="22572-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="22572-118">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="22572-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="22572-119">**8**</span><span class="sxs-lookup"><span data-stu-id="22572-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="22572-120">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="22572-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="22572-121">**9**</span><span class="sxs-lookup"><span data-stu-id="22572-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="22572-122">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="22572-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="22572-123">**10**</span><span class="sxs-lookup"><span data-stu-id="22572-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="22572-124">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="22572-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="22572-125">**11**</span><span class="sxs-lookup"><span data-stu-id="22572-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="22572-126">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="22572-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="22572-127">**12**</span><span class="sxs-lookup"><span data-stu-id="22572-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="22572-128">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="22572-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="22572-129">**13**</span><span class="sxs-lookup"><span data-stu-id="22572-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="22572-130">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="22572-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="22572-131">**14**</span><span class="sxs-lookup"><span data-stu-id="22572-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="22572-132">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="22572-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="22572-133">**15**</span><span class="sxs-lookup"><span data-stu-id="22572-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="22572-134">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="22572-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="22572-135">**16**</span><span class="sxs-lookup"><span data-stu-id="22572-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="22572-136">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="22572-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="22572-137">**17**</span><span class="sxs-lookup"><span data-stu-id="22572-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="22572-138">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="22572-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="22572-139">**21**</span><span class="sxs-lookup"><span data-stu-id="22572-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="22572-140">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="22572-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="22572-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="22572-141">Remarks</span></span>

<span data-ttu-id="22572-142">Per rinominare una cartella, eseguire prima l'associazione alla cartella in questione, quindi chiamare il metodo Rename.</span><span class="sxs-lookup"><span data-stu-id="22572-142">To rename a folder, first bind to the folder in question and then call the Rename method.</span></span> <span data-ttu-id="22572-143">Come unico parametro del metodo, passare il nuovo nome per la cartella come nome di percorso completo.</span><span class="sxs-lookup"><span data-stu-id="22572-143">As the sole parameter to the method, pass the new name for the folder as a complete path name.</span></span> <span data-ttu-id="22572-144">Se, ad esempio, la cartella del backup dei log di C: \\ Scripts deve \\ \\ essere rinominata c: \\ Scripts \\ Archive, è necessario passare c: \\ Scripts \\ Archive come nome completo della cartella.</span><span class="sxs-lookup"><span data-stu-id="22572-144">For example, if the folder in the C:\\Scripts\\Logs\\Backup is to be renamed C:\\Scripts\\Archive, you must pass C:\\Scripts\\Archive as the complete folder name.</span></span> <span data-ttu-id="22572-145">Passando solo il nome della cartella-Archive-viene restituito un errore di percorso non valido.</span><span class="sxs-lookup"><span data-stu-id="22572-145">Passing only the folder name - Archive - results in an Invalid path error.</span></span>

<span data-ttu-id="22572-146">La \_ classe di directory Win32 non fornisce un metodo in un unico passaggio per lo trasferimento di cartelle.</span><span class="sxs-lookup"><span data-stu-id="22572-146">The Win32\_Directory class does not provide a one-step method for moving folders.</span></span> <span data-ttu-id="22572-147">Il trasferimento di una cartella prevede in genere due passaggi:</span><span class="sxs-lookup"><span data-stu-id="22572-147">Instead, moving a folder generally involves two steps:</span></span>

<dl> 1. <span data-ttu-id="22572-148">Copia della cartella nella nuova posizione</span><span class="sxs-lookup"><span data-stu-id="22572-148">Copying the folder to its new location</span></span>  
2. <span data-ttu-id="22572-149">Eliminazione della cartella originale</span><span class="sxs-lookup"><span data-stu-id="22572-149">Deleting the original folder</span></span>  
</dl>

<span data-ttu-id="22572-150">L'unica eccezione a questo processo in due passaggi prevede lo spostamento di una cartella in una nuova posizione nella stessa unità.</span><span class="sxs-lookup"><span data-stu-id="22572-150">The one exception to this two-step process involves moving a folder to a new location on the same drive.</span></span> <span data-ttu-id="22572-151">Si supponga, ad esempio, di voler spostare l' \\ Archivio c: Temp in c: \\ script per \\ i file temporanei \\ .</span><span class="sxs-lookup"><span data-stu-id="22572-151">For example, suppose you want to move C:\\Temp to C:\\Scripts\\Temporary Files\\Archive.</span></span> <span data-ttu-id="22572-152">Fino a quando la posizione corrente e la nuova posizione si trovano nella stessa unità, è possibile spostare la cartella semplicemente chiamando il metodo Rename e passando la nuova posizione come parametro del metodo.</span><span class="sxs-lookup"><span data-stu-id="22572-152">As long as the current location and the new location are on the same drive, you can move the folder by simply calling the Rename method and passing the new location as the method parameter.</span></span> <span data-ttu-id="22572-153">Questo approccio consente di spostare la cartella in un unico passaggio.</span><span class="sxs-lookup"><span data-stu-id="22572-153">This approach effectively allows you to move the folder in a single step.</span></span> <span data-ttu-id="22572-154">Tuttavia, lo script ha esito negativo se l'unità corrente e la nuova unità sono diverse.</span><span class="sxs-lookup"><span data-stu-id="22572-154">However, the script fails if the current drive and the new drive are different.</span></span> <span data-ttu-id="22572-155">Il tentativo di rinominare C: \\ Temp in D: \\ Temp ha esito negativo con un errore "unità non uguale".</span><span class="sxs-lookup"><span data-stu-id="22572-155">An attempt to rename C:\\Temp to D:\\Temp fails with a "Drive not the same" error.</span></span>

## <a name="examples"></a><span data-ttu-id="22572-156">Esempio</span><span class="sxs-lookup"><span data-stu-id="22572-156">Examples</span></span>

<span data-ttu-id="22572-157">Il codice seguente, dall'esempio [Move a folder using WMI](https://Gallery.TechNet.Microsoft.Com/f4f9643c-d7ed-4f54-b155-c6515396431f) VBScript in TechNet Gallery, usa il metodo Rename per spostare la cartella c: \\ Scripts in c: \\ Admins \\ Documents \\ Archive \\ VBScript.</span><span class="sxs-lookup"><span data-stu-id="22572-157">The following code, from the [Move a Folder Using WMI](https://Gallery.TechNet.Microsoft.Com/f4f9643c-d7ed-4f54-b155-c6515396431f) VBScript sample on TechNet Gallery, uses the Rename method to move the folder C:\\Scripts to C:\\Admins\\Documents\\Archive\\VBScript.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colFolders = objWMIService.ExecQuery _ 
    ("Select * from Win32_Directory where name = 'c:\\Scripts'") 
 
For Each objFolder in colFolders 
    errResults = objFolder.Rename("C:\Admins\Documents\Archive\VBScript") 
Next
```



## <a name="requirements"></a><span data-ttu-id="22572-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22572-158">Requirements</span></span>



| <span data-ttu-id="22572-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="22572-159">Requirement</span></span> | <span data-ttu-id="22572-160">Valore</span><span class="sxs-lookup"><span data-stu-id="22572-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22572-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22572-161">Minimum supported client</span></span><br/> | <span data-ttu-id="22572-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="22572-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="22572-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22572-163">Minimum supported server</span></span><br/> | <span data-ttu-id="22572-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22572-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="22572-165">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="22572-165">Namespace</span></span><br/>                | <span data-ttu-id="22572-166">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="22572-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="22572-167">MOF</span><span class="sxs-lookup"><span data-stu-id="22572-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22572-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="22572-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="22572-169">DLL</span><span class="sxs-lookup"><span data-stu-id="22572-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22572-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22572-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22572-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="22572-171">See also</span></span>

<dl> <dt>

<span data-ttu-id="22572-172">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="22572-172">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="22572-173">**\_Directory Win32**</span><span class="sxs-lookup"><span data-stu-id="22572-173">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

