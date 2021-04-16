---
description: TakeOwnerShip&\# 8194; Il metodo della classe WMI ottiene la proprietà del file logico specificato nel percorso dell'oggetto.
ms.assetid: c4f42d54-562c-4163-a5ec-e94f76932631
ms.tgt_platform: multiple
title: Metodo TakeOwnerShip della classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3265e0acc065f63daca2ed6485269ac8c006ad8d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524297"
---
# <a name="takeownership-method-of-the-win32_pagefile-class"></a><span data-ttu-id="0bdea-103">Metodo TakeOwnerShip della classe di \_ paging Win32</span><span class="sxs-lookup"><span data-stu-id="0bdea-103">TakeOwnerShip method of the Win32\_PageFile class</span></span>

<span data-ttu-id="0bdea-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnership** ottiene la proprietà del file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0bdea-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="0bdea-105">Se il file logico è effettivamente una directory, **TakeOwnership** agisce in modo ricorsivo, assumendo la proprietà di tutti i file e le sottodirectory contenute nella directory.</span><span class="sxs-lookup"><span data-stu-id="0bdea-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="0bdea-106">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="0bdea-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0bdea-107">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0bdea-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0bdea-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0bdea-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="0bdea-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0bdea-109">Parameters</span></span>

<span data-ttu-id="0bdea-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0bdea-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0bdea-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0bdea-111">Return value</span></span>

<span data-ttu-id="0bdea-112">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="0bdea-112">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="0bdea-113">**0**</span><span class="sxs-lookup"><span data-stu-id="0bdea-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="0bdea-114">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="0bdea-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="0bdea-115">**2**</span><span class="sxs-lookup"><span data-stu-id="0bdea-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="0bdea-116">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="0bdea-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="0bdea-117">**8**</span><span class="sxs-lookup"><span data-stu-id="0bdea-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="0bdea-118">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="0bdea-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="0bdea-119">**9**</span><span class="sxs-lookup"><span data-stu-id="0bdea-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="0bdea-120">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="0bdea-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0bdea-121">**10**</span><span class="sxs-lookup"><span data-stu-id="0bdea-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="0bdea-122">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="0bdea-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="0bdea-123">**11**</span><span class="sxs-lookup"><span data-stu-id="0bdea-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="0bdea-124">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="0bdea-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="0bdea-125">**12**</span><span class="sxs-lookup"><span data-stu-id="0bdea-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="0bdea-126">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="0bdea-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="0bdea-127">**13**</span><span class="sxs-lookup"><span data-stu-id="0bdea-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="0bdea-128">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="0bdea-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="0bdea-129">**14**</span><span class="sxs-lookup"><span data-stu-id="0bdea-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="0bdea-130">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="0bdea-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="0bdea-131">**15**</span><span class="sxs-lookup"><span data-stu-id="0bdea-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="0bdea-132">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="0bdea-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="0bdea-133">**16**</span><span class="sxs-lookup"><span data-stu-id="0bdea-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="0bdea-134">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="0bdea-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0bdea-135">**17**</span><span class="sxs-lookup"><span data-stu-id="0bdea-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="0bdea-136">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="0bdea-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="0bdea-137">**21**</span><span class="sxs-lookup"><span data-stu-id="0bdea-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="0bdea-138">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="0bdea-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0bdea-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0bdea-139">Requirements</span></span>



| <span data-ttu-id="0bdea-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bdea-140">Requirement</span></span> | <span data-ttu-id="0bdea-141">Valore</span><span class="sxs-lookup"><span data-stu-id="0bdea-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bdea-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0bdea-142">Minimum supported client</span></span><br/> | <span data-ttu-id="0bdea-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0bdea-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0bdea-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0bdea-144">Minimum supported server</span></span><br/> | <span data-ttu-id="0bdea-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0bdea-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0bdea-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0bdea-146">Namespace</span></span><br/>                | <span data-ttu-id="0bdea-147">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="0bdea-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0bdea-148">MOF</span><span class="sxs-lookup"><span data-stu-id="0bdea-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0bdea-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0bdea-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0bdea-150">DLL</span><span class="sxs-lookup"><span data-stu-id="0bdea-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0bdea-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bdea-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bdea-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0bdea-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="0bdea-153">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0bdea-153">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0bdea-154">**\_Pagefile Win32**</span><span class="sxs-lookup"><span data-stu-id="0bdea-154">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

