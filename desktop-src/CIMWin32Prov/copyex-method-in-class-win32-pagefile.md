---
description: Copia il file o la directory di paging logica specificata nel percorso dell'oggetto nel percorso specificato dal parametro FileName. Questo metodo è una versione estesa del metodo Copy.
ms.assetid: a8376dc8-eb73-4097-b84c-839432ac3a25
ms.tgt_platform: multiple
title: Metodo CopyEx della classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 810f1d3bcf878d33756930f6bd3b6799c3513dc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878398"
---
# <a name="copyex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="01483-104">Metodo CopyEx della classe di \_ paging Win32</span><span class="sxs-lookup"><span data-stu-id="01483-104">CopyEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="01483-105">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CopyEx** copia il file di paging logico o la directory specificata nel percorso dell'oggetto nel percorso specificato dal parametro *filename* .</span><span class="sxs-lookup"><span data-stu-id="01483-105">The **CopyEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical paging file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="01483-106">Questo metodo è una versione estesa del metodo [**Copy**](copy-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="01483-106">This method is an extended version of the [**Copy**](copy-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="01483-107">Una copia non è supportata se è necessario sovrascrivere un file logico esistente.</span><span class="sxs-lookup"><span data-stu-id="01483-107">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="01483-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="01483-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="01483-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="01483-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="01483-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01483-110">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="01483-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="01483-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01483-112">*Nome file* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01483-112">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01483-113">Nome completo della copia del file (o directory).</span><span class="sxs-lookup"><span data-stu-id="01483-113">Fully qualified name of the copy of the file (or directory).</span></span>

<span data-ttu-id="01483-114">Esempio: c: \\ temp \\ NewDirectory</span><span class="sxs-lookup"><span data-stu-id="01483-114">Example: c:\\temp\\newdirectory</span></span>

</dd> <dt>

<span data-ttu-id="01483-115">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="01483-115">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01483-116">Nome del file o della directory in cui il metodo **CopyEx** non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="01483-116">Name of the file or directory where the **CopyEx** method failed.</span></span> <span data-ttu-id="01483-117">Questo parametro è **null** se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="01483-117">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="01483-118">*StartFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="01483-118">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="01483-119">Denomina il file o la directory figlio da utilizzare come punto di partenza per **CopyEx**.</span><span class="sxs-lookup"><span data-stu-id="01483-119">Names the child file or directory to use as a starting point for **CopyEx**.</span></span> <span data-ttu-id="01483-120">Il parametro *StartFileName* è in genere il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="01483-120">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="01483-121">Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificata nella chiamata ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="01483-121">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> <dt>

<span data-ttu-id="01483-122">*Ricorsivo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="01483-122">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="01483-123">Se è **true**, la modifica della proprietà verrà applicata in modo ricorsivo ai file e alle directory nella directory specificata dall'istanza [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="01483-123">If **true**, the change of ownership will be applied recursively to the files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="01483-124">Per le istanze di file, il parametro *ricorsivo* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="01483-124">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01483-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="01483-125">Return value</span></span>

<span data-ttu-id="01483-126">Restituisce un valore pari a 0 (zero) se il file è stato copiato correttamente e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="01483-126">Returns a value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="01483-127">**0**</span><span class="sxs-lookup"><span data-stu-id="01483-127">**0**</span></span>
</dt> <dd>

<span data-ttu-id="01483-128">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="01483-128">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="01483-129">**2**</span><span class="sxs-lookup"><span data-stu-id="01483-129">**2**</span></span>
</dt> <dd>

<span data-ttu-id="01483-130">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="01483-130">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="01483-131">**8**</span><span class="sxs-lookup"><span data-stu-id="01483-131">**8**</span></span>
</dt> <dd>

<span data-ttu-id="01483-132">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="01483-132">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="01483-133">**9**</span><span class="sxs-lookup"><span data-stu-id="01483-133">**9**</span></span>
</dt> <dd>

<span data-ttu-id="01483-134">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="01483-134">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="01483-135">**10**</span><span class="sxs-lookup"><span data-stu-id="01483-135">**10**</span></span>
</dt> <dd>

<span data-ttu-id="01483-136">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="01483-136">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="01483-137">**11**</span><span class="sxs-lookup"><span data-stu-id="01483-137">**11**</span></span>
</dt> <dd>

<span data-ttu-id="01483-138">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="01483-138">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="01483-139">**12**</span><span class="sxs-lookup"><span data-stu-id="01483-139">**12**</span></span>
</dt> <dd>

<span data-ttu-id="01483-140">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="01483-140">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="01483-141">**13**</span><span class="sxs-lookup"><span data-stu-id="01483-141">**13**</span></span>
</dt> <dd>

<span data-ttu-id="01483-142">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="01483-142">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="01483-143">**14**</span><span class="sxs-lookup"><span data-stu-id="01483-143">**14**</span></span>
</dt> <dd>

<span data-ttu-id="01483-144">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="01483-144">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="01483-145">**15**</span><span class="sxs-lookup"><span data-stu-id="01483-145">**15**</span></span>
</dt> <dd>

<span data-ttu-id="01483-146">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="01483-146">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="01483-147">**16**</span><span class="sxs-lookup"><span data-stu-id="01483-147">**16**</span></span>
</dt> <dd>

<span data-ttu-id="01483-148">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="01483-148">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="01483-149">**17**</span><span class="sxs-lookup"><span data-stu-id="01483-149">**17**</span></span>
</dt> <dd>

<span data-ttu-id="01483-150">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="01483-150">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="01483-151">**21**</span><span class="sxs-lookup"><span data-stu-id="01483-151">**21**</span></span>
</dt> <dd>

<span data-ttu-id="01483-152">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="01483-152">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="01483-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01483-153">Requirements</span></span>



| <span data-ttu-id="01483-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="01483-154">Requirement</span></span> | <span data-ttu-id="01483-155">Valore</span><span class="sxs-lookup"><span data-stu-id="01483-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01483-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01483-156">Minimum supported client</span></span><br/> | <span data-ttu-id="01483-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01483-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="01483-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01483-158">Minimum supported server</span></span><br/> | <span data-ttu-id="01483-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01483-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="01483-160">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="01483-160">Namespace</span></span><br/>                | <span data-ttu-id="01483-161">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="01483-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="01483-162">MOF</span><span class="sxs-lookup"><span data-stu-id="01483-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01483-163"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01483-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="01483-164">DLL</span><span class="sxs-lookup"><span data-stu-id="01483-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01483-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01483-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01483-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01483-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="01483-167">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="01483-167">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="01483-168">**\_Pagefile Win32**</span><span class="sxs-lookup"><span data-stu-id="01483-168">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

