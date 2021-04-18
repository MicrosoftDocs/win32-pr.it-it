---
description: Ottiene la proprietà del file di voce della directory logica specificato nel percorso dell'oggetto. Questo metodo è una versione estesa del metodo TakeOwnerShip.
ms.assetid: 73726207-e885-4957-bff8-6903c4b99278
ms.tgt_platform: multiple
title: Metodo TakeOwnerShipEx della classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2e391e942e581d0f80d46b0f59b9b273d7bff499
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304475"
---
# <a name="takeownershipex-method-of-the-win32_directory-class"></a><span data-ttu-id="f11f3-104">Metodo TakeOwnerShipEx della classe di \_ directory Win32</span><span class="sxs-lookup"><span data-stu-id="f11f3-104">TakeOwnerShipEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="f11f3-105">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShipEx** ottiene la proprietà del file di voce della directory logica specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f11f3-105">The **TakeOwnerShipEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical directory entry file specified in the object path.</span></span> <span data-ttu-id="f11f3-106">Questo metodo è una versione estesa del metodo [**TakeOwnership**](takeownership-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="f11f3-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="f11f3-107">Se il file logico è in realtà una directory, questo metodo agisce in modo ricorsivo, assumendo la proprietà di tutti i file e le sottodirectory contenuti nella directory.</span><span class="sxs-lookup"><span data-stu-id="f11f3-107">If the logical file is actually a directory, then this method acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="f11f3-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="f11f3-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f11f3-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f11f3-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f11f3-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f11f3-110">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="f11f3-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="f11f3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f11f3-112">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f11f3-112">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f11f3-113">Nome del file o della directory in cui il metodo **TakeOwnerShipEx** non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="f11f3-113">Name of the file or directory where the **TakeOwnerShipEx** method failed.</span></span> <span data-ttu-id="f11f3-114">Questo parametro è **null** se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="f11f3-114">This parameter is **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="f11f3-115">*StartFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="f11f3-115">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f11f3-116">Denomina il file o la directory figlio da utilizzare come punto di partenza per **TakeOwnerShipEx**.</span><span class="sxs-lookup"><span data-stu-id="f11f3-116">Names the child file or directory to use as a starting point for **TakeOwnerShipEx**.</span></span> <span data-ttu-id="f11f3-117">Il parametro *StartFileName* è in genere il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="f11f3-117">The *StartFileName* parameter is typically the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="f11f3-118">Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificata nella chiamata [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="f11f3-118">If this parameter is **NULL**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) call.</span></span>

<span data-ttu-id="f11f3-119">Se si usa *StartFileName* , è necessario impostare *ricorsivo* su true.</span><span class="sxs-lookup"><span data-stu-id="f11f3-119">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="f11f3-120">*Ricorsivo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="f11f3-120">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f11f3-121">Se **true**, la modifica della proprietà viene applicata in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="f11f3-121">If **True**, the change of ownership is applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="f11f3-122">Per le istanze di file, il parametro di input *ricorsivo* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="f11f3-122">For file instances, the *Recursive* input parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f11f3-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f11f3-123">Return value</span></span>

<span data-ttu-id="f11f3-124">Restituisce un valore intero pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="f11f3-124">Returns an integer value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="f11f3-125">**0**</span><span class="sxs-lookup"><span data-stu-id="f11f3-125">**0**</span></span>
</dt> <dd>

<span data-ttu-id="f11f3-126">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="f11f3-126">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="f11f3-127">**2**</span><span class="sxs-lookup"><span data-stu-id="f11f3-127">**2**</span></span>
</dt> <dd>

<span data-ttu-id="f11f3-128">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="f11f3-128">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="f11f3-129">**8**</span><span class="sxs-lookup"><span data-stu-id="f11f3-129">**8**</span></span>
</dt> <dd>

<span data-ttu-id="f11f3-130">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="f11f3-130">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="f11f3-131">**9**</span><span class="sxs-lookup"><span data-stu-id="f11f3-131">**9**</span></span>
</dt> <dd>

<span data-ttu-id="f11f3-132">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="f11f3-132">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f11f3-133">**10**</span><span class="sxs-lookup"><span data-stu-id="f11f3-133">**10**</span></span>
</dt> <dd>

<span data-ttu-id="f11f3-134">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="f11f3-134">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f11f3-135">**11**</span><span class="sxs-lookup"><span data-stu-id="f11f3-135">**11**</span></span>
</dt> <dd>

<span data-ttu-id="f11f3-136">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="f11f3-136">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="f11f3-137">**12**</span><span class="sxs-lookup"><span data-stu-id="f11f3-137">**12**</span></span>
</dt> <dd>

<span data-ttu-id="f11f3-138">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="f11f3-138">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="f11f3-139">**13**</span><span class="sxs-lookup"><span data-stu-id="f11f3-139">**13**</span></span>
</dt> <dd>

<span data-ttu-id="f11f3-140">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="f11f3-140">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="f11f3-141">**14**</span><span class="sxs-lookup"><span data-stu-id="f11f3-141">**14**</span></span>
</dt> <dd>

<span data-ttu-id="f11f3-142">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="f11f3-142">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="f11f3-143">**15**</span><span class="sxs-lookup"><span data-stu-id="f11f3-143">**15**</span></span>
</dt> <dd>

<span data-ttu-id="f11f3-144">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="f11f3-144">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="f11f3-145">**16**</span><span class="sxs-lookup"><span data-stu-id="f11f3-145">**16**</span></span>
</dt> <dd>

<span data-ttu-id="f11f3-146">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="f11f3-146">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f11f3-147">**17**</span><span class="sxs-lookup"><span data-stu-id="f11f3-147">**17**</span></span>
</dt> <dd>

<span data-ttu-id="f11f3-148">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="f11f3-148">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="f11f3-149">**21**</span><span class="sxs-lookup"><span data-stu-id="f11f3-149">**21**</span></span>
</dt> <dd>

<span data-ttu-id="f11f3-150">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="f11f3-150">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="f11f3-151">Esempio</span><span class="sxs-lookup"><span data-stu-id="f11f3-151">Examples</span></span>

<span data-ttu-id="f11f3-152">Il codice di script seguente Visual Basic chiama il metodo [**TakeOwnerShipEx**](takeownershipex-method-in-class-cim-directory.md) per assumere la proprietà della cartella C: \\ Temp.</span><span class="sxs-lookup"><span data-stu-id="f11f3-152">The following Visual Basic Script code calls the [**TakeOwnerShipEx**](takeownershipex-method-in-class-cim-directory.md) method to take ownership of the C:\\temp folder.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")
' Obtain an InParameters object specific
' to the method.
Set objInParam = objShare.Methods_("TakeOwnerShipEx").inParameters.SpawnInstance_()

' Add the input parameters.
objInParam.Properties_.Item("Recursive") =  true

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod("Win32_Directory.Name='C:\Temp'", "TakeOwnerShipEx", objInParam)
wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a><span data-ttu-id="f11f3-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f11f3-153">Requirements</span></span>



| <span data-ttu-id="f11f3-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="f11f3-154">Requirement</span></span> | <span data-ttu-id="f11f3-155">Valore</span><span class="sxs-lookup"><span data-stu-id="f11f3-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f11f3-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f11f3-156">Minimum supported client</span></span><br/> | <span data-ttu-id="f11f3-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f11f3-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f11f3-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f11f3-158">Minimum supported server</span></span><br/> | <span data-ttu-id="f11f3-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f11f3-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f11f3-160">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f11f3-160">Namespace</span></span><br/>                | <span data-ttu-id="f11f3-161">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f11f3-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f11f3-162">MOF</span><span class="sxs-lookup"><span data-stu-id="f11f3-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f11f3-163"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f11f3-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f11f3-164">DLL</span><span class="sxs-lookup"><span data-stu-id="f11f3-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f11f3-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f11f3-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f11f3-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f11f3-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="f11f3-167">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f11f3-167">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f11f3-168">**\_Directory Win32**</span><span class="sxs-lookup"><span data-stu-id="f11f3-168">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

