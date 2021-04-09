---
description: Ottiene la proprietà del file di codec logico specificato nel percorso dell'oggetto. Questo metodo è una versione estesa del metodo TakeOwnerShip.
ms.assetid: 8f3b495a-f654-4818-b0ea-dc88819d72af
ms.tgt_platform: multiple
title: Metodo TakeOwnerShipEx della classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 36512d48fe724da42c39c0d3d0686a706f54472d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877273"
---
# <a name="takeownershipex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="ffce4-104">Metodo TakeOwnerShipEx della \_ classe Sqlcfile Win32</span><span class="sxs-lookup"><span data-stu-id="ffce4-104">TakeOwnerShipEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="ffce4-105">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShipEx** ottiene la proprietà del file di codec logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ffce4-105">The **TakeOwnerShipEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical codec file specified in the object path.</span></span> <span data-ttu-id="ffce4-106">Questo metodo è una versione estesa del metodo [**TakeOwnership**](takeownership-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="ffce4-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="ffce4-107">Se il file logico è in realtà una directory, questo metodo agisce in modo ricorsivo, assumendo la proprietà di tutti i file e le sottodirectory contenuti nella directory.</span><span class="sxs-lookup"><span data-stu-id="ffce4-107">If the logical file is actually a directory, then this method acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="ffce4-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="ffce4-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ffce4-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ffce4-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ffce4-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ffce4-110">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="ffce4-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="ffce4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffce4-112">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ffce4-112">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ffce4-113">Nome del file o della directory in cui il metodo **TakeOwnerShipEx** non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="ffce4-113">Name of the file or directory where the **TakeOwnerShipEx** method failed.</span></span> <span data-ttu-id="ffce4-114">Questo parametro sarà **null** se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ffce4-114">This parameter will be **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="ffce4-115">*StartFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ffce4-115">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ffce4-116">Denomina il file o la directory figlio da utilizzare come punto di partenza per **TakeOwnerShipEx**. Il parametro *StartFileName* è in genere il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="ffce4-116">Names the child file or directory to use as a starting point for **TakeOwnerShipEx**.The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="ffce4-117">Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificata nella chiamata **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="ffce4-117">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="ffce4-118">*Ricorsivo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ffce4-118">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ffce4-119">Se **true**, la modifica della proprietà verrà applicata in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="ffce4-119">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="ffce4-120">Nota: per le istanze di file, il parametro di input *ricorsivo* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="ffce4-120">Note: for file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffce4-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ffce4-121">Return value</span></span>

<span data-ttu-id="ffce4-122">Restituisce un valore intero pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="ffce4-122">Returns an integer value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="ffce4-123">**0**</span><span class="sxs-lookup"><span data-stu-id="ffce4-123">**0**</span></span>
</dt> <dd>

<span data-ttu-id="ffce4-124">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="ffce4-124">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="ffce4-125">**2**</span><span class="sxs-lookup"><span data-stu-id="ffce4-125">**2**</span></span>
</dt> <dd>

<span data-ttu-id="ffce4-126">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="ffce4-126">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="ffce4-127">**8**</span><span class="sxs-lookup"><span data-stu-id="ffce4-127">**8**</span></span>
</dt> <dd>

<span data-ttu-id="ffce4-128">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="ffce4-128">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="ffce4-129">**9**</span><span class="sxs-lookup"><span data-stu-id="ffce4-129">**9**</span></span>
</dt> <dd>

<span data-ttu-id="ffce4-130">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="ffce4-130">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ffce4-131">**10**</span><span class="sxs-lookup"><span data-stu-id="ffce4-131">**10**</span></span>
</dt> <dd>

<span data-ttu-id="ffce4-132">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="ffce4-132">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="ffce4-133">**11**</span><span class="sxs-lookup"><span data-stu-id="ffce4-133">**11**</span></span>
</dt> <dd>

<span data-ttu-id="ffce4-134">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="ffce4-134">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="ffce4-135">**12**</span><span class="sxs-lookup"><span data-stu-id="ffce4-135">**12**</span></span>
</dt> <dd>

<span data-ttu-id="ffce4-136">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="ffce4-136">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="ffce4-137">**13**</span><span class="sxs-lookup"><span data-stu-id="ffce4-137">**13**</span></span>
</dt> <dd>

<span data-ttu-id="ffce4-138">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="ffce4-138">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="ffce4-139">**14**</span><span class="sxs-lookup"><span data-stu-id="ffce4-139">**14**</span></span>
</dt> <dd>

<span data-ttu-id="ffce4-140">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="ffce4-140">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="ffce4-141">**15**</span><span class="sxs-lookup"><span data-stu-id="ffce4-141">**15**</span></span>
</dt> <dd>

<span data-ttu-id="ffce4-142">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="ffce4-142">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="ffce4-143">**16**</span><span class="sxs-lookup"><span data-stu-id="ffce4-143">**16**</span></span>
</dt> <dd>

<span data-ttu-id="ffce4-144">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="ffce4-144">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ffce4-145">**17**</span><span class="sxs-lookup"><span data-stu-id="ffce4-145">**17**</span></span>
</dt> <dd>

<span data-ttu-id="ffce4-146">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="ffce4-146">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="ffce4-147">**21**</span><span class="sxs-lookup"><span data-stu-id="ffce4-147">**21**</span></span>
</dt> <dd>

<span data-ttu-id="ffce4-148">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="ffce4-148">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ffce4-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ffce4-149">Requirements</span></span>



| <span data-ttu-id="ffce4-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffce4-150">Requirement</span></span> | <span data-ttu-id="ffce4-151">Valore</span><span class="sxs-lookup"><span data-stu-id="ffce4-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffce4-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffce4-152">Minimum supported client</span></span><br/> | <span data-ttu-id="ffce4-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ffce4-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ffce4-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffce4-154">Minimum supported server</span></span><br/> | <span data-ttu-id="ffce4-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ffce4-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ffce4-156">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ffce4-156">Namespace</span></span><br/>                | <span data-ttu-id="ffce4-157">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ffce4-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ffce4-158">MOF</span><span class="sxs-lookup"><span data-stu-id="ffce4-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffce4-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ffce4-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ffce4-160">DLL</span><span class="sxs-lookup"><span data-stu-id="ffce4-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffce4-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffce4-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffce4-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ffce4-162">See also</span></span>

<dl> <dt>

<span data-ttu-id="ffce4-163">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ffce4-163">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ffce4-164">**Codecfile Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="ffce4-164">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

