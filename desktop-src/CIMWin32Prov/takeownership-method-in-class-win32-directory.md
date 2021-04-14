---
description: Il metodo della classe WMI TakeOwnerShip ottiene la proprietà del file logico specificato nel percorso dell'oggetto.
ms.assetid: 1112823b-0bb6-4dc0-a5c4-8d3839a47a3a
ms.tgt_platform: multiple
title: Metodo TakeOwnerShip della classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c06441b7728ed8b9178e889cbd60c047f0f3a497
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523010"
---
# <a name="takeownership-method-of-the-win32_directory-class"></a><span data-ttu-id="ef39a-103">Metodo TakeOwnerShip della classe di \_ directory Win32</span><span class="sxs-lookup"><span data-stu-id="ef39a-103">TakeOwnerShip method of the Win32\_Directory class</span></span>

<span data-ttu-id="ef39a-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnership** ottiene la proprietà del file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ef39a-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="ef39a-105">Se il file logico è effettivamente una directory, **TakeOwnership** agisce in modo ricorsivo, assumendo la proprietà di tutti i file e le sottodirectory contenute nella directory.</span><span class="sxs-lookup"><span data-stu-id="ef39a-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="ef39a-106">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="ef39a-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ef39a-107">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ef39a-107">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ef39a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ef39a-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="ef39a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ef39a-109">Parameters</span></span>

<span data-ttu-id="ef39a-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ef39a-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ef39a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ef39a-111">Return value</span></span>

<span data-ttu-id="ef39a-112">Restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ef39a-112">Returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ef39a-113">**0**</span><span class="sxs-lookup"><span data-stu-id="ef39a-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="ef39a-114">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="ef39a-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="ef39a-115">**2**</span><span class="sxs-lookup"><span data-stu-id="ef39a-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="ef39a-116">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="ef39a-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="ef39a-117">**8**</span><span class="sxs-lookup"><span data-stu-id="ef39a-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="ef39a-118">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="ef39a-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="ef39a-119">**9**</span><span class="sxs-lookup"><span data-stu-id="ef39a-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="ef39a-120">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="ef39a-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ef39a-121">**10**</span><span class="sxs-lookup"><span data-stu-id="ef39a-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="ef39a-122">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="ef39a-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="ef39a-123">**11**</span><span class="sxs-lookup"><span data-stu-id="ef39a-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="ef39a-124">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="ef39a-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="ef39a-125">**12**</span><span class="sxs-lookup"><span data-stu-id="ef39a-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="ef39a-126">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="ef39a-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="ef39a-127">**13**</span><span class="sxs-lookup"><span data-stu-id="ef39a-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="ef39a-128">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="ef39a-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="ef39a-129">**14**</span><span class="sxs-lookup"><span data-stu-id="ef39a-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="ef39a-130">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="ef39a-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="ef39a-131">**15**</span><span class="sxs-lookup"><span data-stu-id="ef39a-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="ef39a-132">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="ef39a-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="ef39a-133">**16**</span><span class="sxs-lookup"><span data-stu-id="ef39a-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="ef39a-134">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="ef39a-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ef39a-135">**17**</span><span class="sxs-lookup"><span data-stu-id="ef39a-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="ef39a-136">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="ef39a-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="ef39a-137">**21**</span><span class="sxs-lookup"><span data-stu-id="ef39a-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="ef39a-138">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="ef39a-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="ef39a-139">Esempio</span><span class="sxs-lookup"><span data-stu-id="ef39a-139">Examples</span></span>

<span data-ttu-id="ef39a-140">Il codice di script seguente Visual Basic chiama il metodo [**TakeOwnership**](takeownership-method-in-class-cim-directory.md) per assumere la proprietà della cartella C: \\ Temp.</span><span class="sxs-lookup"><span data-stu-id="ef39a-140">The following Visual Basic Script code calls the [**TakeOwnerShip**](takeownership-method-in-class-cim-directory.md) method to take ownership of the C:\\temp folder.</span></span>


```VB
strComputer = "." 

Set objWMIService = _
    GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 

' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\\temp'", "TakeOwnerShip")

wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a><span data-ttu-id="ef39a-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef39a-141">Requirements</span></span>



| <span data-ttu-id="ef39a-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef39a-142">Requirement</span></span> | <span data-ttu-id="ef39a-143">Valore</span><span class="sxs-lookup"><span data-stu-id="ef39a-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef39a-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef39a-144">Minimum supported client</span></span><br/> | <span data-ttu-id="ef39a-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef39a-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ef39a-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef39a-146">Minimum supported server</span></span><br/> | <span data-ttu-id="ef39a-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef39a-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ef39a-148">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ef39a-148">Namespace</span></span><br/>                | <span data-ttu-id="ef39a-149">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ef39a-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ef39a-150">MOF</span><span class="sxs-lookup"><span data-stu-id="ef39a-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef39a-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef39a-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef39a-152">DLL</span><span class="sxs-lookup"><span data-stu-id="ef39a-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef39a-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef39a-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef39a-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef39a-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="ef39a-155">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ef39a-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ef39a-156">**\_Directory Win32**</span><span class="sxs-lookup"><span data-stu-id="ef39a-156">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

