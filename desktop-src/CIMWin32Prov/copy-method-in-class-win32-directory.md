---
description: Copia il file o la directory della voce di directory logica specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.
ms.assetid: 038e23d7-71db-4db6-8fb1-e84e972510c9
ms.tgt_platform: multiple
title: Metodo Copy della classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 25568167d9532303a7cbee794757bc674a378b39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126923"
---
# <a name="copy-method-of-the-win32_directory-class"></a><span data-ttu-id="7f696-103">Metodo Copy della classe di \_ directory Win32</span><span class="sxs-lookup"><span data-stu-id="7f696-103">Copy method of the Win32\_Directory class</span></span>

<span data-ttu-id="7f696-104">Il metodo **Copy** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) copia il file di voce della directory logica o la directory specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.</span><span class="sxs-lookup"><span data-stu-id="7f696-104">The **Copy** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical directory entry file or directory specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="7f696-105">Una copia non è supportata se è necessario sovrascrivere un file logico esistente.</span><span class="sxs-lookup"><span data-stu-id="7f696-105">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="7f696-106">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="7f696-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7f696-107">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7f696-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7f696-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f696-108">Syntax</span></span>


```mof
uint32 Copy(
   string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="7f696-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7f696-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f696-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="7f696-110">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="7f696-111">Nome completo della copia del file (o directory).</span><span class="sxs-lookup"><span data-stu-id="7f696-111">Fully qualified name of the copy of the file (or directory).</span></span> <span data-ttu-id="7f696-112">Esempio: c: \\ temp \\ NewDirectory</span><span class="sxs-lookup"><span data-stu-id="7f696-112">Example: c:\\temp\\newdirectory</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f696-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7f696-113">Return value</span></span>

<span data-ttu-id="7f696-114">Restituisce un valore pari a 0 (zero) se il file è stato copiato correttamente e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="7f696-114">Returns a value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="7f696-115">**0**</span><span class="sxs-lookup"><span data-stu-id="7f696-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="7f696-116">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="7f696-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="7f696-117">**2**</span><span class="sxs-lookup"><span data-stu-id="7f696-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="7f696-118">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="7f696-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="7f696-119">**8**</span><span class="sxs-lookup"><span data-stu-id="7f696-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="7f696-120">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="7f696-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="7f696-121">**9**</span><span class="sxs-lookup"><span data-stu-id="7f696-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="7f696-122">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="7f696-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="7f696-123">**10**</span><span class="sxs-lookup"><span data-stu-id="7f696-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="7f696-124">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="7f696-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="7f696-125">**11**</span><span class="sxs-lookup"><span data-stu-id="7f696-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="7f696-126">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="7f696-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="7f696-127">**12**</span><span class="sxs-lookup"><span data-stu-id="7f696-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="7f696-128">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="7f696-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="7f696-129">**13**</span><span class="sxs-lookup"><span data-stu-id="7f696-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="7f696-130">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="7f696-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="7f696-131">**14**</span><span class="sxs-lookup"><span data-stu-id="7f696-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="7f696-132">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="7f696-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="7f696-133">**15**</span><span class="sxs-lookup"><span data-stu-id="7f696-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="7f696-134">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="7f696-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="7f696-135">**16**</span><span class="sxs-lookup"><span data-stu-id="7f696-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="7f696-136">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="7f696-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="7f696-137">**17**</span><span class="sxs-lookup"><span data-stu-id="7f696-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="7f696-138">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="7f696-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="7f696-139">**21**</span><span class="sxs-lookup"><span data-stu-id="7f696-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="7f696-140">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="7f696-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f696-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f696-141">Remarks</span></span>

<span data-ttu-id="7f696-142">Spesso è necessario copiare le cartelle da una posizione a un'altra.</span><span class="sxs-lookup"><span data-stu-id="7f696-142">Folders often need to be copied from one location to another.</span></span> <span data-ttu-id="7f696-143">Ad esempio, è possibile copiare una cartella da un server a un altro per creare una copia di backup della cartella.</span><span class="sxs-lookup"><span data-stu-id="7f696-143">For example, you might copy a folder from one server to another to create a backup copy of that folder.</span></span> <span data-ttu-id="7f696-144">In alternativa, è possibile che sia presente una cartella templates che deve essere copiata nelle workstation utente o una cartella Scripts che deve essere copiata in tutti i server DNS.</span><span class="sxs-lookup"><span data-stu-id="7f696-144">Or you might have a templates folder that needs to be copied to user workstations, or a scripts folder that should be copied to all of your DNS servers.</span></span>

<span data-ttu-id="7f696-145">Il \_ metodo di copia della directory Win32 consente di copiare una cartella da un percorso a un altro nello stesso computer (ad esempio, copiando una cartella dall'unità C all'unità D) o in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="7f696-145">The Win32\_Directory Copy method enables you to copy a folder from one location to another, either on the same computer (for example, copying a folder from drive C to drive D) or on a remote computer.</span></span> <span data-ttu-id="7f696-146">Per copiare una cartella, viene restituita un'istanza della cartella da copiare e quindi viene chiamato il metodo Copy, passando come parametro il percorso di destinazione per la nuova copia della cartella.</span><span class="sxs-lookup"><span data-stu-id="7f696-146">To copy a folder, you return an instance of the folder to be copied and then call the Copy method, passing as a parameter the target location for the new copy of the folder.</span></span> <span data-ttu-id="7f696-147">Questa riga di codice, ad esempio, copia una cartella nella cartella script nell'unità F:</span><span class="sxs-lookup"><span data-stu-id="7f696-147">For example, this line of code copies a folder to the Scripts folder on drive F:</span></span>

`objFolder.Copy("F:\Scripts")`

<span data-ttu-id="7f696-148">Quando si esegue il metodo di copia, WMI non sovrascriverà una cartella esistente.</span><span class="sxs-lookup"><span data-stu-id="7f696-148">WMI will not overwrite an existing folder when executing the Copy method.</span></span> <span data-ttu-id="7f696-149">Ciò significa che l'operazione di copia ha esito negativo se la cartella di destinazione esiste.</span><span class="sxs-lookup"><span data-stu-id="7f696-149">This means that the copy operation fails if the destination folder exists.</span></span> <span data-ttu-id="7f696-150">Si supponga, ad esempio, di disporre di una cartella denominata scripts e di copiare la cartella in una condivisione remota denominata \\ \\ Archivio ATL-FS-01 \\ .</span><span class="sxs-lookup"><span data-stu-id="7f696-150">For example, suppose you have a folder named Scripts and you attempt to copy that folder to a remote share named \\\\atl-fs-01\\archive.</span></span> <span data-ttu-id="7f696-151">Se nella condivisione è già presente una cartella denominata scripts, l'operazione di copia ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="7f696-151">If a folder named Scripts already exists on that share, the copy operation fails.</span></span>

## <a name="examples"></a><span data-ttu-id="7f696-152">Esempio</span><span class="sxs-lookup"><span data-stu-id="7f696-152">Examples</span></span>

<span data-ttu-id="7f696-153">L'esempio di codice followng, tratto da [copy a folder using WMI](https://Gallery.TechNet.Microsoft.Com/71b8f517-0240-42a2-be5c-e5a3921604d2), usa il metodo Copy per copiare la cartella C: \\ Scripts in D: \\ Archive.</span><span class="sxs-lookup"><span data-stu-id="7f696-153">The followng code sample, taken from the [Copy a Folder Using WMI](https://Gallery.TechNet.Microsoft.Com/71b8f517-0240-42a2-be5c-e5a3921604d2), uses the Copy method to copy the folder C:\\Scripts to D:\\Archive.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colFolders = objWMIService.ExecQuery( _ 
    "Select * from Win32_Directory where Name = 'c:\\Scripts'") 
 
For Each objFolder in colFolders 
    errResults  = objFolder.Copy("D:\Archive") 
Next
```



## <a name="requirements"></a><span data-ttu-id="7f696-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f696-154">Requirements</span></span>



| <span data-ttu-id="7f696-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f696-155">Requirement</span></span> | <span data-ttu-id="7f696-156">Valore</span><span class="sxs-lookup"><span data-stu-id="7f696-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f696-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f696-157">Minimum supported client</span></span><br/> | <span data-ttu-id="7f696-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7f696-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7f696-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f696-159">Minimum supported server</span></span><br/> | <span data-ttu-id="7f696-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f696-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7f696-161">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7f696-161">Namespace</span></span><br/>                | <span data-ttu-id="7f696-162">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="7f696-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7f696-163">MOF</span><span class="sxs-lookup"><span data-stu-id="7f696-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f696-164"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7f696-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f696-165">DLL</span><span class="sxs-lookup"><span data-stu-id="7f696-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f696-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f696-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f696-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f696-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="7f696-168">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7f696-168">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7f696-169">**\_Directory Win32**</span><span class="sxs-lookup"><span data-stu-id="7f696-169">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

