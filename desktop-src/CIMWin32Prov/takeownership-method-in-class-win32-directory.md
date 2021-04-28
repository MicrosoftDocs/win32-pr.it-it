---
description: "Metodo TakeOwnerShip della classe Win32_Directory: il metodo della classe WMI TakeOwnerShip ottiene la proprietà del file logico specificato nel percorso dell'oggetto."
ms.assetid: 1112823b-0bb6-4dc0-a5c4-8d3839a47a3a
ms.tgt_platform: multiple
title: Metodo TakeOwnerShip della Win32_Directory classe
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
ms.openlocfilehash: 178f1bf523d939883a7fc18b5bdbd7142cc4f824
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086029"
---
# <a name="takeownership-method-of-the-win32_directory-class"></a><span data-ttu-id="a224d-103">Metodo TakeOwnerShip della classe Directory Win32 \_</span><span class="sxs-lookup"><span data-stu-id="a224d-103">TakeOwnerShip method of the Win32\_Directory class</span></span>

<span data-ttu-id="a224d-104">Il metodo della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShip** ottiene la proprietà del file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a224d-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="a224d-105">Se il file logico è effettivamente una directory, **TakeOwnerShip** agisce in modo ricorsivo, assumendo la proprietà di tutti i file e le sottodirectory contenuti nella directory.</span><span class="sxs-lookup"><span data-stu-id="a224d-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="a224d-106">Questo argomento usa Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="a224d-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a224d-107">Per altre informazioni sull'uso di questo metodo, [vedere Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a224d-107">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a224d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a224d-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="a224d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a224d-109">Parameters</span></span>

<span data-ttu-id="a224d-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a224d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a224d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a224d-111">Return value</span></span>

<span data-ttu-id="a224d-112">Restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="a224d-112">Returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a224d-113">**0**</span><span class="sxs-lookup"><span data-stu-id="a224d-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="a224d-114">La richiesta ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a224d-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="a224d-115">**2**</span><span class="sxs-lookup"><span data-stu-id="a224d-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="a224d-116">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="a224d-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="a224d-117">**8**</span><span class="sxs-lookup"><span data-stu-id="a224d-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="a224d-118">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="a224d-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="a224d-119">**9**</span><span class="sxs-lookup"><span data-stu-id="a224d-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="a224d-120">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="a224d-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a224d-121">**10**</span><span class="sxs-lookup"><span data-stu-id="a224d-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="a224d-122">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="a224d-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="a224d-123">**11**</span><span class="sxs-lookup"><span data-stu-id="a224d-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="a224d-124">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="a224d-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="a224d-125">**12**</span><span class="sxs-lookup"><span data-stu-id="a224d-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="a224d-126">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="a224d-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="a224d-127">**13**</span><span class="sxs-lookup"><span data-stu-id="a224d-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="a224d-128">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="a224d-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="a224d-129">**14**</span><span class="sxs-lookup"><span data-stu-id="a224d-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="a224d-130">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="a224d-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="a224d-131">**15**</span><span class="sxs-lookup"><span data-stu-id="a224d-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="a224d-132">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="a224d-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="a224d-133">**16**</span><span class="sxs-lookup"><span data-stu-id="a224d-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="a224d-134">Il file iniziale specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="a224d-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a224d-135">**17**</span><span class="sxs-lookup"><span data-stu-id="a224d-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="a224d-136">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="a224d-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="a224d-137">**21**</span><span class="sxs-lookup"><span data-stu-id="a224d-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="a224d-138">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="a224d-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="a224d-139">Esempio</span><span class="sxs-lookup"><span data-stu-id="a224d-139">Examples</span></span>

<span data-ttu-id="a224d-140">Il codice Visual Basic script seguente chiama il [**metodo TakeOwnerShip**](takeownership-method-in-class-cim-directory.md) per assumere la proprietà della cartella \\ C: temp.</span><span class="sxs-lookup"><span data-stu-id="a224d-140">The following Visual Basic Script code calls the [**TakeOwnerShip**](takeownership-method-in-class-cim-directory.md) method to take ownership of the C:\\temp folder.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="a224d-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a224d-141">Requirements</span></span>



| <span data-ttu-id="a224d-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="a224d-142">Requirement</span></span> | <span data-ttu-id="a224d-143">Valore</span><span class="sxs-lookup"><span data-stu-id="a224d-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a224d-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a224d-144">Minimum supported client</span></span><br/> | <span data-ttu-id="a224d-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a224d-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a224d-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a224d-146">Minimum supported server</span></span><br/> | <span data-ttu-id="a224d-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a224d-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a224d-148">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a224d-148">Namespace</span></span><br/>                | <span data-ttu-id="a224d-149">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a224d-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a224d-150">MOF</span><span class="sxs-lookup"><span data-stu-id="a224d-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a224d-151"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="a224d-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a224d-152">DLL</span><span class="sxs-lookup"><span data-stu-id="a224d-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a224d-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a224d-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a224d-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a224d-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="a224d-155">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a224d-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a224d-156">**Win32 \_ Directory**</span><span class="sxs-lookup"><span data-stu-id="a224d-156">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

