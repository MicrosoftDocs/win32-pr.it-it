---
description: Decomprime il file di voce o directory della directory logica specificato nel percorso dell'oggetto. Questo metodo è una versione estesa del metodo Decompress.
ms.assetid: cd18d8b7-ab63-475c-a3a6-79611c9e032d
ms.tgt_platform: multiple
title: Metodo UncompressEx della classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a0fd02d0757745199249d64fa08d73f8b5ec65a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127502"
---
# <a name="uncompressex-method-of-the-win32_directory-class"></a><span data-ttu-id="0aff5-104">Metodo UncompressEx della classe di \_ directory Win32</span><span class="sxs-lookup"><span data-stu-id="0aff5-104">UncompressEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="0aff5-105">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UncompressEx** decomprime il file di voce o la directory della directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0aff5-105">The **UncompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical directory entry file (or directory) specified in the object path.</span></span> <span data-ttu-id="0aff5-106">Questo metodo è una versione estesa del metodo [**Decompress**](uncompress-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="0aff5-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="0aff5-107">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="0aff5-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0aff5-108">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0aff5-108">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0aff5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0aff5-109">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="0aff5-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="0aff5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0aff5-111">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0aff5-111">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0aff5-112">Nome del file o della directory in cui il metodo **UncompressEx** non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="0aff5-112">Name of the file/directory where the **UncompressEx** method failed.</span></span> <span data-ttu-id="0aff5-113">Questo parametro sarà **null** se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0aff5-113">This parameter will be **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="0aff5-114">*StartFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="0aff5-114">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0aff5-115">Denomina la directory o il file figlio da utilizzare come punto di partenza per **UncompressEx**.</span><span class="sxs-lookup"><span data-stu-id="0aff5-115">Names the child file/directory to use as a starting point for **UncompressEx**.</span></span> <span data-ttu-id="0aff5-116">Il parametro *StartFileName* è in genere il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="0aff5-116">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="0aff5-117">Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificata nella chiamata ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="0aff5-117">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

<span data-ttu-id="0aff5-118">Se si usa *StartFileName* , è necessario impostare *ricorsivo* su true.</span><span class="sxs-lookup"><span data-stu-id="0aff5-118">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="0aff5-119">*Ricorsivo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="0aff5-119">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0aff5-120">Se **true**, la modifica della proprietà verrà applicata in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="0aff5-120">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="0aff5-121">Nota: per le istanze di file, il parametro di input *ricorsivo* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="0aff5-121">Note: for file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0aff5-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0aff5-122">Return value</span></span>

<span data-ttu-id="0aff5-123">Restituisce un valore pari a 0 (zero) se il file è stato decompresso correttamente e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="0aff5-123">Returns an value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="0aff5-124">**0**</span><span class="sxs-lookup"><span data-stu-id="0aff5-124">**0**</span></span>
</dt> <dd>

<span data-ttu-id="0aff5-125">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="0aff5-125">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="0aff5-126">**2**</span><span class="sxs-lookup"><span data-stu-id="0aff5-126">**2**</span></span>
</dt> <dd>

<span data-ttu-id="0aff5-127">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="0aff5-127">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="0aff5-128">**8**</span><span class="sxs-lookup"><span data-stu-id="0aff5-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="0aff5-129">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="0aff5-129">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="0aff5-130">**9**</span><span class="sxs-lookup"><span data-stu-id="0aff5-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="0aff5-131">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="0aff5-131">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0aff5-132">**10**</span><span class="sxs-lookup"><span data-stu-id="0aff5-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="0aff5-133">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="0aff5-133">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="0aff5-134">**11**</span><span class="sxs-lookup"><span data-stu-id="0aff5-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="0aff5-135">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="0aff5-135">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="0aff5-136">**12**</span><span class="sxs-lookup"><span data-stu-id="0aff5-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="0aff5-137">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="0aff5-137">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="0aff5-138">**13**</span><span class="sxs-lookup"><span data-stu-id="0aff5-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="0aff5-139">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="0aff5-139">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="0aff5-140">**14**</span><span class="sxs-lookup"><span data-stu-id="0aff5-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="0aff5-141">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="0aff5-141">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="0aff5-142">**15**</span><span class="sxs-lookup"><span data-stu-id="0aff5-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="0aff5-143">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="0aff5-143">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="0aff5-144">**16**</span><span class="sxs-lookup"><span data-stu-id="0aff5-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="0aff5-145">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="0aff5-145">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0aff5-146">**17**</span><span class="sxs-lookup"><span data-stu-id="0aff5-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="0aff5-147">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="0aff5-147">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="0aff5-148">**21**</span><span class="sxs-lookup"><span data-stu-id="0aff5-148">**21**</span></span>
</dt> <dd>

<span data-ttu-id="0aff5-149">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="0aff5-149">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0aff5-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0aff5-150">Requirements</span></span>



| <span data-ttu-id="0aff5-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="0aff5-151">Requirement</span></span> | <span data-ttu-id="0aff5-152">Valore</span><span class="sxs-lookup"><span data-stu-id="0aff5-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0aff5-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0aff5-153">Minimum supported client</span></span><br/> | <span data-ttu-id="0aff5-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0aff5-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0aff5-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0aff5-155">Minimum supported server</span></span><br/> | <span data-ttu-id="0aff5-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0aff5-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0aff5-157">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0aff5-157">Namespace</span></span><br/>                | <span data-ttu-id="0aff5-158">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="0aff5-158">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0aff5-159">MOF</span><span class="sxs-lookup"><span data-stu-id="0aff5-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0aff5-160"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0aff5-160"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0aff5-161">DLL</span><span class="sxs-lookup"><span data-stu-id="0aff5-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0aff5-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0aff5-162"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0aff5-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0aff5-163">See also</span></span>

<dl> <dt>

<span data-ttu-id="0aff5-164">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0aff5-164">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0aff5-165">**\_Directory Win32**</span><span class="sxs-lookup"><span data-stu-id="0aff5-165">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

