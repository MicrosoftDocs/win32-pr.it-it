---
description: Decomprime il file di collegamento logico (o directory) specificato nel percorso dell'oggetto. Questo metodo è una versione estesa del metodo Decompress.
ms.assetid: aa1c04d1-4cce-4096-bce3-b9c61b9a4eb7
ms.tgt_platform: multiple
title: Metodo UncompressEx della classe Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e07e86be3666b06063ef81c896eab6ee7a918657
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127499"
---
# <a name="uncompressex-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="28fa9-104">Metodo UncompressEx della \_ classe ShortcutFile Win32</span><span class="sxs-lookup"><span data-stu-id="28fa9-104">UncompressEx method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="28fa9-105">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UncompressEx** decomprime il file di collegamento logico o la directory specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="28fa9-105">The **UncompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical shortcut file (or directory) specified in the object path.</span></span> <span data-ttu-id="28fa9-106">Questo metodo è una versione estesa del metodo [**Decompress**](uncompress-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="28fa9-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="28fa9-107">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="28fa9-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="28fa9-108">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="28fa9-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="28fa9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="28fa9-109">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="28fa9-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="28fa9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28fa9-111">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="28fa9-111">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28fa9-112">Nome del file o della directory in cui il metodo **UncompressEx** non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="28fa9-112">Name of the file or directory where the **UncompressEx** method failed.</span></span> <span data-ttu-id="28fa9-113">Questo parametro sarà **null** se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="28fa9-113">This parameter will be **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="28fa9-114">*StartFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="28fa9-114">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="28fa9-115">Denomina il file o la directory figlio da utilizzare come punto di partenza per **UncompressEx**.</span><span class="sxs-lookup"><span data-stu-id="28fa9-115">Names the child file or directory to use as a starting point for **UncompressEx**.</span></span> <span data-ttu-id="28fa9-116">Il parametro *StartFileName* è in genere il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="28fa9-116">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="28fa9-117">Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificata nella chiamata ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="28fa9-117">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> <dt>

<span data-ttu-id="28fa9-118">*Ricorsivo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="28fa9-118">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="28fa9-119">Se **true**, la modifica della proprietà verrà applicata in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="28fa9-119">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="28fa9-120">Per le istanze di file, il parametro *ricorsivo* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="28fa9-120">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28fa9-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="28fa9-121">Return value</span></span>

<span data-ttu-id="28fa9-122">Restituisce un valore pari a 0 (zero) se il file è stato decompresso correttamente e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="28fa9-122">Returns a value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="28fa9-123">**0**</span><span class="sxs-lookup"><span data-stu-id="28fa9-123">**0**</span></span>
</dt> <dd>

<span data-ttu-id="28fa9-124">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="28fa9-124">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="28fa9-125">**2**</span><span class="sxs-lookup"><span data-stu-id="28fa9-125">**2**</span></span>
</dt> <dd>

<span data-ttu-id="28fa9-126">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="28fa9-126">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="28fa9-127">**8**</span><span class="sxs-lookup"><span data-stu-id="28fa9-127">**8**</span></span>
</dt> <dd>

<span data-ttu-id="28fa9-128">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="28fa9-128">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="28fa9-129">**9**</span><span class="sxs-lookup"><span data-stu-id="28fa9-129">**9**</span></span>
</dt> <dd>

<span data-ttu-id="28fa9-130">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="28fa9-130">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="28fa9-131">**10**</span><span class="sxs-lookup"><span data-stu-id="28fa9-131">**10**</span></span>
</dt> <dd>

<span data-ttu-id="28fa9-132">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="28fa9-132">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="28fa9-133">**11**</span><span class="sxs-lookup"><span data-stu-id="28fa9-133">**11**</span></span>
</dt> <dd>

<span data-ttu-id="28fa9-134">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="28fa9-134">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="28fa9-135">**12**</span><span class="sxs-lookup"><span data-stu-id="28fa9-135">**12**</span></span>
</dt> <dd>

<span data-ttu-id="28fa9-136">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="28fa9-136">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="28fa9-137">**13**</span><span class="sxs-lookup"><span data-stu-id="28fa9-137">**13**</span></span>
</dt> <dd>

<span data-ttu-id="28fa9-138">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="28fa9-138">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="28fa9-139">**14**</span><span class="sxs-lookup"><span data-stu-id="28fa9-139">**14**</span></span>
</dt> <dd>

<span data-ttu-id="28fa9-140">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="28fa9-140">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="28fa9-141">**15**</span><span class="sxs-lookup"><span data-stu-id="28fa9-141">**15**</span></span>
</dt> <dd>

<span data-ttu-id="28fa9-142">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="28fa9-142">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="28fa9-143">**16**</span><span class="sxs-lookup"><span data-stu-id="28fa9-143">**16**</span></span>
</dt> <dd>

<span data-ttu-id="28fa9-144">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="28fa9-144">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="28fa9-145">**17**</span><span class="sxs-lookup"><span data-stu-id="28fa9-145">**17**</span></span>
</dt> <dd>

<span data-ttu-id="28fa9-146">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="28fa9-146">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="28fa9-147">**21**</span><span class="sxs-lookup"><span data-stu-id="28fa9-147">**21**</span></span>
</dt> <dd>

<span data-ttu-id="28fa9-148">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="28fa9-148">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="28fa9-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28fa9-149">Requirements</span></span>



| <span data-ttu-id="28fa9-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="28fa9-150">Requirement</span></span> | <span data-ttu-id="28fa9-151">Valore</span><span class="sxs-lookup"><span data-stu-id="28fa9-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28fa9-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28fa9-152">Minimum supported client</span></span><br/> | <span data-ttu-id="28fa9-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="28fa9-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="28fa9-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28fa9-154">Minimum supported server</span></span><br/> | <span data-ttu-id="28fa9-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28fa9-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="28fa9-156">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="28fa9-156">Namespace</span></span><br/>                | <span data-ttu-id="28fa9-157">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="28fa9-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="28fa9-158">MOF</span><span class="sxs-lookup"><span data-stu-id="28fa9-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28fa9-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="28fa9-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="28fa9-160">DLL</span><span class="sxs-lookup"><span data-stu-id="28fa9-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28fa9-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28fa9-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28fa9-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28fa9-162">See also</span></span>

<dl> <dt>

<span data-ttu-id="28fa9-163">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="28fa9-163">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="28fa9-164">**\_ShortcutFile Win32**</span><span class="sxs-lookup"><span data-stu-id="28fa9-164">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

