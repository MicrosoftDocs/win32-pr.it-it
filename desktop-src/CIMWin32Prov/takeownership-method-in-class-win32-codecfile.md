---
description: Il metodo della classe WMI TakeOwnerShip ottiene la proprietà del file logico specificato nel percorso dell'oggetto.
ms.assetid: c8fa0706-1f7e-4e68-aea6-694ba24c16c3
ms.tgt_platform: multiple
title: Metodo TakeOwnerShip della classe Win32_CodecFile
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
ms.openlocfilehash: 1de05f444e99be9a1ebcb5d32fa0ba754cf34254
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126006"
---
# <a name="takeownership-method-of-the-win32_codecfile-class"></a><span data-ttu-id="c9fe7-103">Metodo TakeOwnerShip della \_ classe Sqlcfile Win32</span><span class="sxs-lookup"><span data-stu-id="c9fe7-103">TakeOwnerShip method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="c9fe7-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnership** ottiene la proprietà del file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c9fe7-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="c9fe7-105">Se il file logico è effettivamente una directory, **TakeOwnership** agisce in modo ricorsivo, assumendo la proprietà di tutti i file e le sottodirectory contenute nella directory.</span><span class="sxs-lookup"><span data-stu-id="c9fe7-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="c9fe7-106">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="c9fe7-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c9fe7-107">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c9fe7-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c9fe7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c9fe7-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="c9fe7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9fe7-109">Parameters</span></span>

<span data-ttu-id="c9fe7-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c9fe7-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c9fe7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c9fe7-111">Return value</span></span>

<span data-ttu-id="c9fe7-112">Restituisce uno dei valori interi seguenti.</span><span class="sxs-lookup"><span data-stu-id="c9fe7-112">Returns one of the following integer values.</span></span>

<dl> <dt>

<span data-ttu-id="c9fe7-113">**0**</span><span class="sxs-lookup"><span data-stu-id="c9fe7-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c9fe7-114">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="c9fe7-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="c9fe7-115">**2**</span><span class="sxs-lookup"><span data-stu-id="c9fe7-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="c9fe7-116">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="c9fe7-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="c9fe7-117">**8**</span><span class="sxs-lookup"><span data-stu-id="c9fe7-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="c9fe7-118">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="c9fe7-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="c9fe7-119">**9**</span><span class="sxs-lookup"><span data-stu-id="c9fe7-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="c9fe7-120">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="c9fe7-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c9fe7-121">**10**</span><span class="sxs-lookup"><span data-stu-id="c9fe7-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="c9fe7-122">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="c9fe7-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="c9fe7-123">**11**</span><span class="sxs-lookup"><span data-stu-id="c9fe7-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="c9fe7-124">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="c9fe7-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="c9fe7-125">**12**</span><span class="sxs-lookup"><span data-stu-id="c9fe7-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="c9fe7-126">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="c9fe7-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="c9fe7-127">**13**</span><span class="sxs-lookup"><span data-stu-id="c9fe7-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="c9fe7-128">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="c9fe7-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="c9fe7-129">**14**</span><span class="sxs-lookup"><span data-stu-id="c9fe7-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="c9fe7-130">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="c9fe7-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="c9fe7-131">**15**</span><span class="sxs-lookup"><span data-stu-id="c9fe7-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="c9fe7-132">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="c9fe7-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="c9fe7-133">**16**</span><span class="sxs-lookup"><span data-stu-id="c9fe7-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="c9fe7-134">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="c9fe7-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c9fe7-135">**17**</span><span class="sxs-lookup"><span data-stu-id="c9fe7-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="c9fe7-136">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="c9fe7-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="c9fe7-137">**21**</span><span class="sxs-lookup"><span data-stu-id="c9fe7-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="c9fe7-138">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="c9fe7-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9fe7-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9fe7-139">Requirements</span></span>



| <span data-ttu-id="c9fe7-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9fe7-140">Requirement</span></span> | <span data-ttu-id="c9fe7-141">Valore</span><span class="sxs-lookup"><span data-stu-id="c9fe7-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9fe7-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9fe7-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c9fe7-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c9fe7-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c9fe7-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9fe7-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c9fe7-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9fe7-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c9fe7-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c9fe7-146">Namespace</span></span><br/>                | <span data-ttu-id="c9fe7-147">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="c9fe7-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c9fe7-148">MOF</span><span class="sxs-lookup"><span data-stu-id="c9fe7-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9fe7-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9fe7-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9fe7-150">DLL</span><span class="sxs-lookup"><span data-stu-id="c9fe7-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9fe7-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9fe7-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9fe7-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9fe7-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="c9fe7-153">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c9fe7-153">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c9fe7-154">**Codecfile Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="c9fe7-154">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

