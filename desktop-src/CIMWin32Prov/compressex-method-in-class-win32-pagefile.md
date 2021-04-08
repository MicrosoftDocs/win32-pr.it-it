---
description: Comprime il file di paging logico (o directory) specificato nel percorso dell'oggetto (questo metodo è una versione estesa del metodo Compress).
ms.assetid: ea99367b-4d5e-4cd2-aa89-d250d1161f8f
ms.tgt_platform: multiple
title: Metodo CompressEx della classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2823d12fc474b5a5023890596a116062d94a045f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877357"
---
# <a name="compressex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="313c4-103">Metodo CompressEx della classe di \_ paging Win32</span><span class="sxs-lookup"><span data-stu-id="313c4-103">CompressEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="313c4-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CompressEx** comprime il file di paging logico o la directory specificata nel percorso dell'oggetto (questo metodo è una versione estesa del metodo [**Compress**](compress-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="313c4-104">The **CompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical paging file (or directory) specified in the object path (this method is an extended version of the [**Compress**](compress-method-in-class-win32-directory.md) method).</span></span>

<span data-ttu-id="313c4-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="313c4-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="313c4-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="313c4-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="313c4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="313c4-107">Syntax</span></span>


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="313c4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="313c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="313c4-109">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="313c4-109">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="313c4-110">Nome del file o della directory in cui il metodo **CompressEx** non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="313c4-110">Name of the file or directory where the **CompressEx** method failed.</span></span> <span data-ttu-id="313c4-111">Questo parametro è **null** se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="313c4-111">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="313c4-112">*StartFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="313c4-112">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="313c4-113">Denomina il file o la directory figlio da utilizzare come punto di partenza per **CompressEx**.</span><span class="sxs-lookup"><span data-stu-id="313c4-113">Names the child file or directory to use as a starting point for **CompressEx**.</span></span> <span data-ttu-id="313c4-114">Il parametro *StartFileName* è in genere il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="313c4-114">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="313c4-115">Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificata nella chiamata **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="313c4-115">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="313c4-116">*Ricorsivo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="313c4-116">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="313c4-117">Se è **true**, la modifica della proprietà verrà applicata in modo ricorsivo ai file e alle directory nella directory specificata dall'istanza [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="313c4-117">If **true**, the change of ownership will be applied recursively to the files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="313c4-118">Per le istanze di file, il parametro *ricorsivo* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="313c4-118">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="313c4-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="313c4-119">Return value</span></span>

<span data-ttu-id="313c4-120">Restituisce un valore pari a 0 (zero) se il file è stato compresso correttamente e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="313c4-120">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="313c4-121">**0**</span><span class="sxs-lookup"><span data-stu-id="313c4-121">**0**</span></span>
</dt> <dd>

<span data-ttu-id="313c4-122">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="313c4-122">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="313c4-123">**2**</span><span class="sxs-lookup"><span data-stu-id="313c4-123">**2**</span></span>
</dt> <dd>

<span data-ttu-id="313c4-124">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="313c4-124">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="313c4-125">**8**</span><span class="sxs-lookup"><span data-stu-id="313c4-125">**8**</span></span>
</dt> <dd>

<span data-ttu-id="313c4-126">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="313c4-126">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="313c4-127">**9**</span><span class="sxs-lookup"><span data-stu-id="313c4-127">**9**</span></span>
</dt> <dd>

<span data-ttu-id="313c4-128">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="313c4-128">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="313c4-129">**10**</span><span class="sxs-lookup"><span data-stu-id="313c4-129">**10**</span></span>
</dt> <dd>

<span data-ttu-id="313c4-130">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="313c4-130">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="313c4-131">**11**</span><span class="sxs-lookup"><span data-stu-id="313c4-131">**11**</span></span>
</dt> <dd>

<span data-ttu-id="313c4-132">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="313c4-132">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="313c4-133">**12**</span><span class="sxs-lookup"><span data-stu-id="313c4-133">**12**</span></span>
</dt> <dd>

<span data-ttu-id="313c4-134">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="313c4-134">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="313c4-135">**13**</span><span class="sxs-lookup"><span data-stu-id="313c4-135">**13**</span></span>
</dt> <dd>

<span data-ttu-id="313c4-136">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="313c4-136">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="313c4-137">**14**</span><span class="sxs-lookup"><span data-stu-id="313c4-137">**14**</span></span>
</dt> <dd>

<span data-ttu-id="313c4-138">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="313c4-138">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="313c4-139">**15**</span><span class="sxs-lookup"><span data-stu-id="313c4-139">**15**</span></span>
</dt> <dd>

<span data-ttu-id="313c4-140">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="313c4-140">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="313c4-141">**16**</span><span class="sxs-lookup"><span data-stu-id="313c4-141">**16**</span></span>
</dt> <dd>

<span data-ttu-id="313c4-142">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="313c4-142">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="313c4-143">**17**</span><span class="sxs-lookup"><span data-stu-id="313c4-143">**17**</span></span>
</dt> <dd>

<span data-ttu-id="313c4-144">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="313c4-144">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="313c4-145">**21**</span><span class="sxs-lookup"><span data-stu-id="313c4-145">**21**</span></span>
</dt> <dd>

<span data-ttu-id="313c4-146">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="313c4-146">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="313c4-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="313c4-147">Requirements</span></span>



| <span data-ttu-id="313c4-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="313c4-148">Requirement</span></span> | <span data-ttu-id="313c4-149">Valore</span><span class="sxs-lookup"><span data-stu-id="313c4-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="313c4-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="313c4-150">Minimum supported client</span></span><br/> | <span data-ttu-id="313c4-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="313c4-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="313c4-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="313c4-152">Minimum supported server</span></span><br/> | <span data-ttu-id="313c4-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="313c4-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="313c4-154">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="313c4-154">Namespace</span></span><br/>                | <span data-ttu-id="313c4-155">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="313c4-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="313c4-156">MOF</span><span class="sxs-lookup"><span data-stu-id="313c4-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="313c4-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="313c4-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="313c4-158">DLL</span><span class="sxs-lookup"><span data-stu-id="313c4-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="313c4-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="313c4-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="313c4-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="313c4-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="313c4-161">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="313c4-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="313c4-162">**\_Pagefile Win32**</span><span class="sxs-lookup"><span data-stu-id="313c4-162">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

