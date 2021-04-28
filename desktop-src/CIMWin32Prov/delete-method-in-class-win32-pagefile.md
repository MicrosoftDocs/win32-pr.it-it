---
description: "Metodo Delete della classe Win32_PageFile: elimina il file di paging logico (o la directory) specificato nel percorso dell'oggetto."
ms.assetid: cc36d621-597e-4343-8bf6-bfca7fa29276
ms.tgt_platform: multiple
title: Metodo Delete della classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b35751633387f3db1d7dccbf13694f56717a1d3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089589"
---
# <a name="delete-method-of-the-win32_pagefile-class"></a><span data-ttu-id="770ac-103">Metodo Delete della classe PageFile Win32 \_</span><span class="sxs-lookup"><span data-stu-id="770ac-103">Delete method of the Win32\_PageFile class</span></span>

<span data-ttu-id="770ac-104">Il **metodo delete** della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) elimina il file di paging logico (o la directory) specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="770ac-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes the logical paging file (or directory) specified in the object path.</span></span>

<span data-ttu-id="770ac-105">Questo argomento usa Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="770ac-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="770ac-106">Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="770ac-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="770ac-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="770ac-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="770ac-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="770ac-108">Parameters</span></span>

<span data-ttu-id="770ac-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="770ac-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="770ac-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="770ac-110">Return value</span></span>

<span data-ttu-id="770ac-111">Restituisce il valore 0 (zero) se il file è stato eliminato correttamente e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="770ac-111">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="770ac-112">**0**</span><span class="sxs-lookup"><span data-stu-id="770ac-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="770ac-113">La richiesta ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="770ac-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="770ac-114">**2**</span><span class="sxs-lookup"><span data-stu-id="770ac-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="770ac-115">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="770ac-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="770ac-116">**8**</span><span class="sxs-lookup"><span data-stu-id="770ac-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="770ac-117">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="770ac-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="770ac-118">**9**</span><span class="sxs-lookup"><span data-stu-id="770ac-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="770ac-119">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="770ac-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="770ac-120">**10**</span><span class="sxs-lookup"><span data-stu-id="770ac-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="770ac-121">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="770ac-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="770ac-122">**11**</span><span class="sxs-lookup"><span data-stu-id="770ac-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="770ac-123">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="770ac-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="770ac-124">**12**</span><span class="sxs-lookup"><span data-stu-id="770ac-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="770ac-125">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="770ac-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="770ac-126">**13**</span><span class="sxs-lookup"><span data-stu-id="770ac-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="770ac-127">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="770ac-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="770ac-128">**14**</span><span class="sxs-lookup"><span data-stu-id="770ac-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="770ac-129">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="770ac-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="770ac-130">**15**</span><span class="sxs-lookup"><span data-stu-id="770ac-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="770ac-131">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="770ac-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="770ac-132">**16**</span><span class="sxs-lookup"><span data-stu-id="770ac-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="770ac-133">Il file iniziale specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="770ac-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="770ac-134">**17**</span><span class="sxs-lookup"><span data-stu-id="770ac-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="770ac-135">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="770ac-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="770ac-136">**21**</span><span class="sxs-lookup"><span data-stu-id="770ac-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="770ac-137">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="770ac-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="770ac-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="770ac-138">Requirements</span></span>



| <span data-ttu-id="770ac-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="770ac-139">Requirement</span></span> | <span data-ttu-id="770ac-140">Valore</span><span class="sxs-lookup"><span data-stu-id="770ac-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="770ac-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="770ac-141">Minimum supported client</span></span><br/> | <span data-ttu-id="770ac-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="770ac-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="770ac-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="770ac-143">Minimum supported server</span></span><br/> | <span data-ttu-id="770ac-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="770ac-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="770ac-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="770ac-145">Namespace</span></span><br/>                | <span data-ttu-id="770ac-146">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="770ac-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="770ac-147">MOF</span><span class="sxs-lookup"><span data-stu-id="770ac-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="770ac-148"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="770ac-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="770ac-149">DLL</span><span class="sxs-lookup"><span data-stu-id="770ac-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="770ac-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="770ac-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="770ac-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="770ac-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="770ac-152">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="770ac-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="770ac-153">**File di paging Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="770ac-153">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

