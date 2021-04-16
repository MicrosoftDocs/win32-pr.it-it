---
description: Decomprime il file di codec logico (o directory) specificato nel percorso dell'oggetto. Questo metodo è una versione estesa del metodo Decompress.
ms.assetid: 257c69fa-c4f7-48be-8317-55db4b01601b
ms.tgt_platform: multiple
title: Metodo UncompressEx della classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 547062a85336681b78a6081646801e78e4713e3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524121"
---
# <a name="uncompressex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="d5fed-104">Metodo UncompressEx della \_ classe Sqlcfile Win32</span><span class="sxs-lookup"><span data-stu-id="d5fed-104">UncompressEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="d5fed-105">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UncompressEx** decomprime il file di codec logico o la directory specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d5fed-105">The **UncompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical codec file (or directory) specified in the object path.</span></span> <span data-ttu-id="d5fed-106">Questo metodo è una versione estesa del metodo [**Decompress**](uncompress-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="d5fed-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="d5fed-107">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="d5fed-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d5fed-108">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d5fed-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d5fed-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d5fed-109">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="d5fed-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5fed-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5fed-111">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d5fed-111">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5fed-112">Nome del file o della directory in cui il metodo **UncompressEx** non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="d5fed-112">Name of the file or directory where the **UncompressEx** method failed.</span></span> <span data-ttu-id="d5fed-113">Questo parametro sarà **null** se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="d5fed-113">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="d5fed-114">*StartFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="d5fed-114">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d5fed-115">Denomina il file o la directory figlio da utilizzare come punto di partenza per **UncompressEx**. Il parametro *StartFileName* è in genere il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="d5fed-115">Names the child file or directory to use as a starting point for **UncompressEx**.The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="d5fed-116">Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificata nella chiamata **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="d5fed-116">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="d5fed-117">*Ricorsivo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="d5fed-117">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d5fed-118">Se **true**, la modifica della proprietà verrà applicata in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="d5fed-118">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="d5fed-119">Nota: per le istanze di file, il parametro di input *ricorsivo* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="d5fed-119">Note: for file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5fed-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5fed-120">Return value</span></span>

<span data-ttu-id="d5fed-121">Restituisce un valore intero pari a 0 (zero) se il file è stato decompresso correttamente e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="d5fed-121">Returns an integer value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="d5fed-122">**0**</span><span class="sxs-lookup"><span data-stu-id="d5fed-122">**0**</span></span>
</dt> <dd>

<span data-ttu-id="d5fed-123">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="d5fed-123">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="d5fed-124">**2**</span><span class="sxs-lookup"><span data-stu-id="d5fed-124">**2**</span></span>
</dt> <dd>

<span data-ttu-id="d5fed-125">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="d5fed-125">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="d5fed-126">**8**</span><span class="sxs-lookup"><span data-stu-id="d5fed-126">**8**</span></span>
</dt> <dd>

<span data-ttu-id="d5fed-127">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="d5fed-127">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d5fed-128">**9**</span><span class="sxs-lookup"><span data-stu-id="d5fed-128">**9**</span></span>
</dt> <dd>

<span data-ttu-id="d5fed-129">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="d5fed-129">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d5fed-130">**10**</span><span class="sxs-lookup"><span data-stu-id="d5fed-130">**10**</span></span>
</dt> <dd>

<span data-ttu-id="d5fed-131">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="d5fed-131">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d5fed-132">**11**</span><span class="sxs-lookup"><span data-stu-id="d5fed-132">**11**</span></span>
</dt> <dd>

<span data-ttu-id="d5fed-133">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="d5fed-133">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="d5fed-134">**12**</span><span class="sxs-lookup"><span data-stu-id="d5fed-134">**12**</span></span>
</dt> <dd>

<span data-ttu-id="d5fed-135">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="d5fed-135">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="d5fed-136">**13**</span><span class="sxs-lookup"><span data-stu-id="d5fed-136">**13**</span></span>
</dt> <dd>

<span data-ttu-id="d5fed-137">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="d5fed-137">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="d5fed-138">**14**</span><span class="sxs-lookup"><span data-stu-id="d5fed-138">**14**</span></span>
</dt> <dd>

<span data-ttu-id="d5fed-139">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="d5fed-139">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="d5fed-140">**15**</span><span class="sxs-lookup"><span data-stu-id="d5fed-140">**15**</span></span>
</dt> <dd>

<span data-ttu-id="d5fed-141">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="d5fed-141">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="d5fed-142">**16**</span><span class="sxs-lookup"><span data-stu-id="d5fed-142">**16**</span></span>
</dt> <dd>

<span data-ttu-id="d5fed-143">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="d5fed-143">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d5fed-144">**17**</span><span class="sxs-lookup"><span data-stu-id="d5fed-144">**17**</span></span>
</dt> <dd>

<span data-ttu-id="d5fed-145">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="d5fed-145">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="d5fed-146">**21**</span><span class="sxs-lookup"><span data-stu-id="d5fed-146">**21**</span></span>
</dt> <dd>

<span data-ttu-id="d5fed-147">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="d5fed-147">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5fed-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5fed-148">Requirements</span></span>



| <span data-ttu-id="d5fed-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5fed-149">Requirement</span></span> | <span data-ttu-id="d5fed-150">Valore</span><span class="sxs-lookup"><span data-stu-id="d5fed-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5fed-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5fed-151">Minimum supported client</span></span><br/> | <span data-ttu-id="d5fed-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5fed-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d5fed-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5fed-153">Minimum supported server</span></span><br/> | <span data-ttu-id="d5fed-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5fed-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d5fed-155">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d5fed-155">Namespace</span></span><br/>                | <span data-ttu-id="d5fed-156">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="d5fed-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d5fed-157">MOF</span><span class="sxs-lookup"><span data-stu-id="d5fed-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5fed-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5fed-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5fed-159">DLL</span><span class="sxs-lookup"><span data-stu-id="d5fed-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5fed-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5fed-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5fed-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5fed-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="d5fed-162">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d5fed-162">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d5fed-163">**Codecfile Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="d5fed-163">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

