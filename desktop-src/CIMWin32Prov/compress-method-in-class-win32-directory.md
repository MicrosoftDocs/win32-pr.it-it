---
description: Comprime il file di voce o la directory della directory logica specificata nel percorso dell'oggetto.
ms.assetid: 4db13622-75c5-45db-8536-451059c0e477
ms.tgt_platform: multiple
title: Metodo Compress della classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea694c09e11e5801016a4ea85b9774448c542991
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126117"
---
# <a name="compress-method-of-the-win32_directory-class"></a><span data-ttu-id="a087c-103">Metodo Compress della classe di \_ directory Win32</span><span class="sxs-lookup"><span data-stu-id="a087c-103">Compress method of the Win32\_Directory class</span></span>

<span data-ttu-id="a087c-104">Il metodo **Comprimi** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) comprime il file di voce o la directory della directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a087c-104">The **Compress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical directory entry file (or directory) specified in the object path.</span></span>

<span data-ttu-id="a087c-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="a087c-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a087c-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a087c-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a087c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a087c-107">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="a087c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a087c-108">Parameters</span></span>

<span data-ttu-id="a087c-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a087c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a087c-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a087c-110">Return value</span></span>

<span data-ttu-id="a087c-111">Restituisce un valore pari a 0 (zero) se il file è stato compresso correttamente e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="a087c-111">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="a087c-112">**0**</span><span class="sxs-lookup"><span data-stu-id="a087c-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="a087c-113">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="a087c-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="a087c-114">**2**</span><span class="sxs-lookup"><span data-stu-id="a087c-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="a087c-115">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="a087c-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="a087c-116">**8**</span><span class="sxs-lookup"><span data-stu-id="a087c-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="a087c-117">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="a087c-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="a087c-118">**9**</span><span class="sxs-lookup"><span data-stu-id="a087c-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="a087c-119">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="a087c-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a087c-120">**10**</span><span class="sxs-lookup"><span data-stu-id="a087c-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="a087c-121">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="a087c-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="a087c-122">**11**</span><span class="sxs-lookup"><span data-stu-id="a087c-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="a087c-123">Il file system non è un NTFS.</span><span class="sxs-lookup"><span data-stu-id="a087c-123">The file system is not an NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="a087c-124">**12**</span><span class="sxs-lookup"><span data-stu-id="a087c-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="a087c-125">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="a087c-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="a087c-126">**13**</span><span class="sxs-lookup"><span data-stu-id="a087c-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="a087c-127">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="a087c-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="a087c-128">**14**</span><span class="sxs-lookup"><span data-stu-id="a087c-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="a087c-129">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="a087c-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="a087c-130">**15**</span><span class="sxs-lookup"><span data-stu-id="a087c-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="a087c-131">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="a087c-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="a087c-132">**16**</span><span class="sxs-lookup"><span data-stu-id="a087c-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="a087c-133">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="a087c-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a087c-134">**17**</span><span class="sxs-lookup"><span data-stu-id="a087c-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="a087c-135">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="a087c-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="a087c-136">**21**</span><span class="sxs-lookup"><span data-stu-id="a087c-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="a087c-137">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="a087c-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a087c-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="a087c-138">Remarks</span></span>

<span data-ttu-id="a087c-139">La compressione consente di liberare spazio di archiviazione aggiuntivo su un'unità disco senza acquistare nuovo hardware e senza rimuovere file o cartelle.</span><span class="sxs-lookup"><span data-stu-id="a087c-139">Compression provides a way to free additional storage space on a disk drive without purchasing new hardware and without removing files or folders.</span></span> <span data-ttu-id="a087c-140">A seconda delle dimensioni del disco rigido e del tipo di file archiviati sul disco, è possibile che si riesca a recuperare centinaia di megabyte di spazio su disco, evitando così di dover acquistare un nuovo disco rigido e portare il computer offline fino a quando non viene installata la nuova unità.</span><span class="sxs-lookup"><span data-stu-id="a087c-140">Depending on the size of your hard disk and the type of files stored on that disk, you might be able to recover hundreds of megabytes of disk space and thus preclude the need to purchase a new hard drive and to take the computer offline until the new drive is installed.</span></span>

<span data-ttu-id="a087c-141">Il metodo Compress comprime tutti i file e le sottocartelle all'interno di una cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="a087c-141">The Compress method compresses all the files and subfolders within a specified folder.</span></span> <span data-ttu-id="a087c-142">Inoltre, la classe include anche un metodo uncompress che rimuove la compressione da tutti i file e le sottocartelle in una cartella.</span><span class="sxs-lookup"><span data-stu-id="a087c-142">In addition, the class also includes an Uncompress method that removes compression from all the files and subfolders in a folder.</span></span> <span data-ttu-id="a087c-143">Vengono inoltre forniti metodi simili con la \_ classe CIM DataFile.</span><span class="sxs-lookup"><span data-stu-id="a087c-143">Similar methods are also provided with the CIM\_Datafile class.</span></span> <span data-ttu-id="a087c-144">In questo modo è possibile comprimere o decomprimere selettivamente file specifici all'interno di una cartella.</span><span class="sxs-lookup"><span data-stu-id="a087c-144">This allows you to selectively compress or uncompress specific files within a folder.</span></span>

<span data-ttu-id="a087c-145">Poiché la compressione comporta una lieve riduzione delle prestazioni, non è consigliabile per i file o le cartelle a cui viene eseguito l'accesso in base a una routine. ad esempio, è probabile che non si desideri comprimere i file di database, i file di log o le cartelle dei profili utente.</span><span class="sxs-lookup"><span data-stu-id="a087c-145">Because compression imparts a slight performance penalty, it is not recommended for files or folders that are accessed on a routine basis; for example, you probably do not want to compress database files, log files, or user profile folders.</span></span> <span data-ttu-id="a087c-146">I candidati migliori per la compressione sono file e cartelle a cui non si accede molto spesso.</span><span class="sxs-lookup"><span data-stu-id="a087c-146">Better candidates for compression are files and folders that are not accessed very often.</span></span> <span data-ttu-id="a087c-147">Ad esempio, è possibile scrivere uno script per restituire una raccolta di cartelle in un'unità a cui non è stato eseguito l'accesso per un mese o più, quindi comprimere ognuna di queste cartelle.</span><span class="sxs-lookup"><span data-stu-id="a087c-147">For example, you might write a script to return a collection of folders on a drive that have not been accessed for a month or more and then compress each of those folders.</span></span>

<span data-ttu-id="a087c-148">La quantità di spazio su disco liberata dalle cartelle di compressione varia a seconda del tipo di file archiviati in tale cartella.</span><span class="sxs-lookup"><span data-stu-id="a087c-148">The amount of disk space freed by compressing folders varies depending on the type of files stored in that folder.</span></span> <span data-ttu-id="a087c-149">Ad esempio, i file con estensione jpg sono già compressi e l'ulteriore compressione ha un effetto minimo sulle dimensioni del file.</span><span class="sxs-lookup"><span data-stu-id="a087c-149">For example, .jpg files are already compressed, and further compression has little effect on the size of the file.</span></span> <span data-ttu-id="a087c-150">Con altri tipi di file, tuttavia, il risparmio può essere considerevole.</span><span class="sxs-lookup"><span data-stu-id="a087c-150">With other file types, however, the savings can be considerable.</span></span> <span data-ttu-id="a087c-151">Ad esempio, una nuova cartella è stata creata in un computer di test basato su Windows 2000 e 33 i documenti di Microsoft Word, che occupano un totale di 15 megabyte (MB) di spazio su disco, sono stati copiati in tale cartella.</span><span class="sxs-lookup"><span data-stu-id="a087c-151">For example, a new folder was created on a Windows 2000-based test computer, and 33 Microsoft Word documents, taking up a total of 15 megabytes (MB) of disk space, were copied into that folder.</span></span> <span data-ttu-id="a087c-152">Quando i documenti sono stati compressi, la cartella ha occupato solo 7 MB di spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="a087c-152">When the documents were compressed, the folder took up only 7 MB of disk space.</span></span>

## <a name="examples"></a><span data-ttu-id="a087c-153">Esempio</span><span class="sxs-lookup"><span data-stu-id="a087c-153">Examples</span></span>

<span data-ttu-id="a087c-154">L'esempio VBScript seguente comprime la cartella C: \\ Scripts.</span><span class="sxs-lookup"><span data-stu-id="a087c-154">The following VBScript sample compresses the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Compress
 Wscript.Echo errResults
Next
```



## <a name="requirements"></a><span data-ttu-id="a087c-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a087c-155">Requirements</span></span>



| <span data-ttu-id="a087c-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="a087c-156">Requirement</span></span> | <span data-ttu-id="a087c-157">Valore</span><span class="sxs-lookup"><span data-stu-id="a087c-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a087c-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a087c-158">Minimum supported client</span></span><br/> | <span data-ttu-id="a087c-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a087c-159">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a087c-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a087c-160">Minimum supported server</span></span><br/> | <span data-ttu-id="a087c-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a087c-161">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a087c-162">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a087c-162">Namespace</span></span><br/>                | <span data-ttu-id="a087c-163">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a087c-163">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a087c-164">MOF</span><span class="sxs-lookup"><span data-stu-id="a087c-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a087c-165"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a087c-165"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a087c-166">DLL</span><span class="sxs-lookup"><span data-stu-id="a087c-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a087c-167"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a087c-167"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a087c-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a087c-168">See also</span></span>

<dl> <dt>

<span data-ttu-id="a087c-169">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a087c-169">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a087c-170">**\_Directory Win32**</span><span class="sxs-lookup"><span data-stu-id="a087c-170">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> <dt>

[<span data-ttu-id="a087c-171">**Decomprimere**</span><span class="sxs-lookup"><span data-stu-id="a087c-171">**Uncompress**</span></span>](uncompress-method-in-class-win32-directory.md)
</dt> </dl>

 

