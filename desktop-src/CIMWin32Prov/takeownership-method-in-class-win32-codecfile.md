---
description: "Metodo TakeOwnerShip della Win32_CodecFile: il metodo della classe WMI TakeOwnerShip ottiene la proprietà del file logico specificato nel percorso dell'oggetto."
ms.assetid: c8fa0706-1f7e-4e68-aea6-694ba24c16c3
ms.tgt_platform: multiple
title: Metodo TakeOwnerShip della Win32_CodecFile classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e52e5dafe5f0453861ddcddadf9f7115d17ee404
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086039"
---
# <a name="takeownership-method-of-the-win32_codecfile-class"></a><span data-ttu-id="3ea1f-103">Metodo TakeOwnerShip della classe CodecFile Win32 \_</span><span class="sxs-lookup"><span data-stu-id="3ea1f-103">TakeOwnerShip method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="3ea1f-104">Il metodo della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShip** ottiene la proprietà del file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3ea1f-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="3ea1f-105">Se il file logico è effettivamente una directory, **TakeOwnerShip** agisce in modo ricorsivo, assumendo la proprietà di tutti i file e le sottodirectory contenuti nella directory.</span><span class="sxs-lookup"><span data-stu-id="3ea1f-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="3ea1f-106">Questo argomento usa Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="3ea1f-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3ea1f-107">Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3ea1f-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3ea1f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ea1f-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="3ea1f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3ea1f-109">Parameters</span></span>

<span data-ttu-id="3ea1f-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="3ea1f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3ea1f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3ea1f-111">Return value</span></span>

<span data-ttu-id="3ea1f-112">Restituisce uno dei seguenti valori interi.</span><span class="sxs-lookup"><span data-stu-id="3ea1f-112">Returns one of the following integer values.</span></span>

<dl> <dt>

<span data-ttu-id="3ea1f-113">**0**</span><span class="sxs-lookup"><span data-stu-id="3ea1f-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="3ea1f-114">La richiesta ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="3ea1f-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="3ea1f-115">**2**</span><span class="sxs-lookup"><span data-stu-id="3ea1f-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="3ea1f-116">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="3ea1f-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="3ea1f-117">**8**</span><span class="sxs-lookup"><span data-stu-id="3ea1f-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="3ea1f-118">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="3ea1f-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="3ea1f-119">**9**</span><span class="sxs-lookup"><span data-stu-id="3ea1f-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="3ea1f-120">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="3ea1f-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3ea1f-121">**10**</span><span class="sxs-lookup"><span data-stu-id="3ea1f-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="3ea1f-122">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="3ea1f-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3ea1f-123">**11**</span><span class="sxs-lookup"><span data-stu-id="3ea1f-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="3ea1f-124">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="3ea1f-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="3ea1f-125">**12**</span><span class="sxs-lookup"><span data-stu-id="3ea1f-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="3ea1f-126">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="3ea1f-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="3ea1f-127">**13**</span><span class="sxs-lookup"><span data-stu-id="3ea1f-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="3ea1f-128">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="3ea1f-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="3ea1f-129">**14**</span><span class="sxs-lookup"><span data-stu-id="3ea1f-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="3ea1f-130">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="3ea1f-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="3ea1f-131">**15**</span><span class="sxs-lookup"><span data-stu-id="3ea1f-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="3ea1f-132">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="3ea1f-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="3ea1f-133">**16**</span><span class="sxs-lookup"><span data-stu-id="3ea1f-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="3ea1f-134">Il file iniziale specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="3ea1f-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3ea1f-135">**17**</span><span class="sxs-lookup"><span data-stu-id="3ea1f-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="3ea1f-136">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="3ea1f-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="3ea1f-137">**21**</span><span class="sxs-lookup"><span data-stu-id="3ea1f-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="3ea1f-138">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="3ea1f-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3ea1f-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ea1f-139">Requirements</span></span>



| <span data-ttu-id="3ea1f-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ea1f-140">Requirement</span></span> | <span data-ttu-id="3ea1f-141">Valore</span><span class="sxs-lookup"><span data-stu-id="3ea1f-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ea1f-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ea1f-142">Minimum supported client</span></span><br/> | <span data-ttu-id="3ea1f-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ea1f-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3ea1f-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ea1f-144">Minimum supported server</span></span><br/> | <span data-ttu-id="3ea1f-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ea1f-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3ea1f-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3ea1f-146">Namespace</span></span><br/>                | <span data-ttu-id="3ea1f-147">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="3ea1f-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3ea1f-148">MOF</span><span class="sxs-lookup"><span data-stu-id="3ea1f-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ea1f-149"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ea1f-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ea1f-150">DLL</span><span class="sxs-lookup"><span data-stu-id="3ea1f-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ea1f-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ea1f-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ea1f-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ea1f-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="3ea1f-153">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3ea1f-153">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3ea1f-154">**Win32 \_ CodecFile**</span><span class="sxs-lookup"><span data-stu-id="3ea1f-154">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

