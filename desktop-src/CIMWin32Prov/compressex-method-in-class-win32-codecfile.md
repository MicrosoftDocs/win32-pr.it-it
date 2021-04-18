---
description: Comprime il file di codec logico (o directory) specificato nel percorso dell'oggetto (questo metodo è una versione estesa del metodo Compress).
ms.assetid: e1ecf0de-3b81-443e-9936-326d7d2d9210
ms.tgt_platform: multiple
title: Metodo CompressEx della classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4ab2915a4f550c799fed8a58e5573e8264b92f1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482925"
---
# <a name="compressex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="0e410-103">Metodo CompressEx della \_ classe Sqlcfile Win32</span><span class="sxs-lookup"><span data-stu-id="0e410-103">CompressEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="0e410-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CompressEx** comprime il file di codec logico o la directory specificata nel percorso dell'oggetto (questo metodo è una versione estesa del metodo [**Compress**](compress-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="0e410-104">The **CompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical codec file (or directory) specified in the object path (this method is an extended version of the [**Compress**](compress-method-in-class-win32-directory.md) method).</span></span>

<span data-ttu-id="0e410-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="0e410-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0e410-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0e410-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0e410-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e410-107">Syntax</span></span>


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="0e410-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0e410-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e410-109">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0e410-109">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e410-110">Nome del file o della directory in cui il metodo **CompressEx** non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="0e410-110">Name of the file or directory where the **CompressEx** method failed.</span></span> <span data-ttu-id="0e410-111">Questo parametro sarà **null** se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0e410-111">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="0e410-112">*StartFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="0e410-112">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0e410-113">Denomina il file o la directory figlio da utilizzare come punto di partenza per **CompressEx** . Il parametro *StartFileName* è in genere il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="0e410-113">Names the child file or directory to use as a starting point for **CompressEx** .The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="0e410-114">Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificata nella chiamata **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="0e410-114">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="0e410-115">*Ricorsivo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="0e410-115">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0e410-116">Se **true**, la modifica della proprietà verrà applicata in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="0e410-116">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="0e410-117">Nota: per le istanze di file, il parametro di input *ricorsivo* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="0e410-117">Note: for file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e410-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0e410-118">Return value</span></span>

<span data-ttu-id="0e410-119">Restituisce un valore pari a 0 (zero) se il file è stato compresso correttamente e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="0e410-119">Returns an value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="0e410-120">**0**</span><span class="sxs-lookup"><span data-stu-id="0e410-120">**0**</span></span>
</dt> <dd>

<span data-ttu-id="0e410-121">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="0e410-121">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="0e410-122">**2**</span><span class="sxs-lookup"><span data-stu-id="0e410-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="0e410-123">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="0e410-123">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="0e410-124">**8**</span><span class="sxs-lookup"><span data-stu-id="0e410-124">**8**</span></span>
</dt> <dd>

<span data-ttu-id="0e410-125">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="0e410-125">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="0e410-126">**9**</span><span class="sxs-lookup"><span data-stu-id="0e410-126">**9**</span></span>
</dt> <dd>

<span data-ttu-id="0e410-127">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="0e410-127">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0e410-128">**10**</span><span class="sxs-lookup"><span data-stu-id="0e410-128">**10**</span></span>
</dt> <dd>

<span data-ttu-id="0e410-129">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="0e410-129">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="0e410-130">**11**</span><span class="sxs-lookup"><span data-stu-id="0e410-130">**11**</span></span>
</dt> <dd>

<span data-ttu-id="0e410-131">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="0e410-131">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="0e410-132">**12**</span><span class="sxs-lookup"><span data-stu-id="0e410-132">**12**</span></span>
</dt> <dd>

<span data-ttu-id="0e410-133">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="0e410-133">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="0e410-134">**13**</span><span class="sxs-lookup"><span data-stu-id="0e410-134">**13**</span></span>
</dt> <dd>

<span data-ttu-id="0e410-135">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="0e410-135">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="0e410-136">**14**</span><span class="sxs-lookup"><span data-stu-id="0e410-136">**14**</span></span>
</dt> <dd>

<span data-ttu-id="0e410-137">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="0e410-137">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="0e410-138">**15**</span><span class="sxs-lookup"><span data-stu-id="0e410-138">**15**</span></span>
</dt> <dd>

<span data-ttu-id="0e410-139">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="0e410-139">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="0e410-140">**16**</span><span class="sxs-lookup"><span data-stu-id="0e410-140">**16**</span></span>
</dt> <dd>

<span data-ttu-id="0e410-141">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="0e410-141">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0e410-142">**17**</span><span class="sxs-lookup"><span data-stu-id="0e410-142">**17**</span></span>
</dt> <dd>

<span data-ttu-id="0e410-143">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="0e410-143">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="0e410-144">**21**</span><span class="sxs-lookup"><span data-stu-id="0e410-144">**21**</span></span>
</dt> <dd>

<span data-ttu-id="0e410-145">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="0e410-145">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0e410-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e410-146">Requirements</span></span>



| <span data-ttu-id="0e410-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e410-147">Requirement</span></span> | <span data-ttu-id="0e410-148">Valore</span><span class="sxs-lookup"><span data-stu-id="0e410-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e410-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e410-149">Minimum supported client</span></span><br/> | <span data-ttu-id="0e410-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e410-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0e410-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e410-151">Minimum supported server</span></span><br/> | <span data-ttu-id="0e410-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e410-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0e410-153">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0e410-153">Namespace</span></span><br/>                | <span data-ttu-id="0e410-154">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="0e410-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0e410-155">MOF</span><span class="sxs-lookup"><span data-stu-id="0e410-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e410-156"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e410-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e410-157">DLL</span><span class="sxs-lookup"><span data-stu-id="0e410-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e410-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e410-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e410-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e410-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="0e410-160">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0e410-160">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0e410-161">**Codecfile Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="0e410-161">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

