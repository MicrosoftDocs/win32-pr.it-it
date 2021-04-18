---
description: Ottiene la proprietà del file di collegamento logico specificato nel percorso dell'oggetto. Questo metodo è una versione estesa del metodo TakeOwnerShip.
ms.assetid: 1345562c-343e-4e3a-b6ed-3b64a7260c89
ms.tgt_platform: multiple
title: Metodo TakeOwnerShipEx della classe Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 69988c7995ee295297c92bbabf0ee83059304a94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304473"
---
# <a name="takeownershipex-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="22507-104">Metodo TakeOwnerShipEx della \_ classe ShortcutFile Win32</span><span class="sxs-lookup"><span data-stu-id="22507-104">TakeOwnerShipEx method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="22507-105">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShipEx** ottiene la proprietà del file di collegamento logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="22507-105">The **TakeOwnerShipEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical shortcut file specified in the object path.</span></span> <span data-ttu-id="22507-106">Questo metodo è una versione estesa del metodo [**TakeOwnership**](takeownership-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="22507-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="22507-107">Se il file logico è in realtà una directory, questo metodo agisce in modo ricorsivo, assumendo la proprietà di tutti i file e le sottodirectory contenuti nella directory.</span><span class="sxs-lookup"><span data-stu-id="22507-107">If the logical file is actually a directory, then this method acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="22507-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="22507-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="22507-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="22507-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="22507-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="22507-110">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="22507-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="22507-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22507-112">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="22507-112">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22507-113">Nome del file o della directory in cui il metodo **TakeOwnerShipEx** non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="22507-113">Name of the file or directory where the **TakeOwnerShipEx** method failed.</span></span> <span data-ttu-id="22507-114">Questo parametro sarà **null** se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="22507-114">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="22507-115">*StartFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="22507-115">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="22507-116">Denomina il file o la directory figlio da utilizzare come punto di partenza per **TakeOwnerShipEx**.</span><span class="sxs-lookup"><span data-stu-id="22507-116">Names the child file or directory to use as a starting point for **TakeOwnerShipEx**.</span></span> <span data-ttu-id="22507-117">Il parametro *StartFileName* è in genere il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="22507-117">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="22507-118">Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificata nella chiamata ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="22507-118">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> <dt>

<span data-ttu-id="22507-119">*Ricorsivo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="22507-119">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="22507-120">Se **true**, la modifica della proprietà verrà applicata in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="22507-120">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="22507-121">Per le istanze di file, il parametro *ricorsivo* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="22507-121">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22507-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="22507-122">Return value</span></span>

<span data-ttu-id="22507-123">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="22507-123">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="22507-124">**0**</span><span class="sxs-lookup"><span data-stu-id="22507-124">**0**</span></span>
</dt> <dd>

<span data-ttu-id="22507-125">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="22507-125">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="22507-126">**2**</span><span class="sxs-lookup"><span data-stu-id="22507-126">**2**</span></span>
</dt> <dd>

<span data-ttu-id="22507-127">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="22507-127">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="22507-128">**8**</span><span class="sxs-lookup"><span data-stu-id="22507-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="22507-129">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="22507-129">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="22507-130">**9**</span><span class="sxs-lookup"><span data-stu-id="22507-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="22507-131">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="22507-131">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="22507-132">**10**</span><span class="sxs-lookup"><span data-stu-id="22507-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="22507-133">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="22507-133">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="22507-134">**11**</span><span class="sxs-lookup"><span data-stu-id="22507-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="22507-135">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="22507-135">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="22507-136">**12**</span><span class="sxs-lookup"><span data-stu-id="22507-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="22507-137">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="22507-137">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="22507-138">**13**</span><span class="sxs-lookup"><span data-stu-id="22507-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="22507-139">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="22507-139">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="22507-140">**14**</span><span class="sxs-lookup"><span data-stu-id="22507-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="22507-141">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="22507-141">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="22507-142">**15**</span><span class="sxs-lookup"><span data-stu-id="22507-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="22507-143">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="22507-143">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="22507-144">**16**</span><span class="sxs-lookup"><span data-stu-id="22507-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="22507-145">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="22507-145">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="22507-146">**17**</span><span class="sxs-lookup"><span data-stu-id="22507-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="22507-147">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="22507-147">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="22507-148">**21**</span><span class="sxs-lookup"><span data-stu-id="22507-148">**21**</span></span>
</dt> <dd>

<span data-ttu-id="22507-149">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="22507-149">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="22507-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22507-150">Requirements</span></span>



| <span data-ttu-id="22507-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="22507-151">Requirement</span></span> | <span data-ttu-id="22507-152">Valore</span><span class="sxs-lookup"><span data-stu-id="22507-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22507-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22507-153">Minimum supported client</span></span><br/> | <span data-ttu-id="22507-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="22507-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="22507-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22507-155">Minimum supported server</span></span><br/> | <span data-ttu-id="22507-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22507-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="22507-157">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="22507-157">Namespace</span></span><br/>                | <span data-ttu-id="22507-158">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="22507-158">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="22507-159">MOF</span><span class="sxs-lookup"><span data-stu-id="22507-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22507-160"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="22507-160"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="22507-161">DLL</span><span class="sxs-lookup"><span data-stu-id="22507-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22507-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22507-162"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22507-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="22507-163">See also</span></span>

<dl> <dt>

<span data-ttu-id="22507-164">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="22507-164">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="22507-165">**\_ShortcutFile Win32**</span><span class="sxs-lookup"><span data-stu-id="22507-165">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

