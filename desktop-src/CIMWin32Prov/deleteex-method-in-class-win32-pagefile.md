---
description: Elimina il file di paging logico (o directory) specificato nel percorso dell'oggetto.
ms.assetid: ea31f92a-94b9-4d4d-abd9-6c304ac5caee
ms.tgt_platform: multiple
title: Metodo DeleteEx della classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2f62875313f6be432ab191fc91bbac381627de3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126525"
---
# <a name="deleteex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="3a07c-103">Metodo DeleteEx della classe di \_ paging Win32</span><span class="sxs-lookup"><span data-stu-id="3a07c-103">DeleteEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="3a07c-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **DeleteEx** Elimina il file di paging logico o la directory specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3a07c-104">The **DeleteEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes the logical paging file (or directory) specified in the object path.</span></span> <span data-ttu-id="3a07c-105">**DeleteEx** è una versione estesa del metodo [**Delete**](delete-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="3a07c-105">**DeleteEx** is an extended version of the [**Delete**](delete-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="3a07c-106">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="3a07c-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3a07c-107">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3a07c-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3a07c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3a07c-108">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out]          string StopFileName,
  [in, optional] string StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="3a07c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a07c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a07c-110">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3a07c-110">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a07c-111">Nome del file o della directory in cui il metodo **DeleteEx** non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="3a07c-111">Name of the file or directory where the **DeleteEx** method failed.</span></span> <span data-ttu-id="3a07c-112">Questo parametro è **null** se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="3a07c-112">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="3a07c-113">*StartFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3a07c-113">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3a07c-114">Denomina il file o la directory figlio da utilizzare come punto di partenza per **DeleteEx**.</span><span class="sxs-lookup"><span data-stu-id="3a07c-114">Names the child file or directory to use as a starting point for **DeleteEx**.</span></span> <span data-ttu-id="3a07c-115">Il parametro *StartFileName* è in genere il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="3a07c-115">The *StartFileName* parameter is typically the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="3a07c-116">Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificata nella chiamata ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="3a07c-116">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a07c-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a07c-117">Return value</span></span>

<span data-ttu-id="3a07c-118">Restituisce un valore pari a 0 (zero) se il file è stato eliminato correttamente e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="3a07c-118">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="3a07c-119">**0**</span><span class="sxs-lookup"><span data-stu-id="3a07c-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="3a07c-120">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="3a07c-120">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="3a07c-121">**2**</span><span class="sxs-lookup"><span data-stu-id="3a07c-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="3a07c-122">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="3a07c-122">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="3a07c-123">**8**</span><span class="sxs-lookup"><span data-stu-id="3a07c-123">**8**</span></span>
</dt> <dd>

<span data-ttu-id="3a07c-124">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="3a07c-124">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="3a07c-125">**9**</span><span class="sxs-lookup"><span data-stu-id="3a07c-125">**9**</span></span>
</dt> <dd>

<span data-ttu-id="3a07c-126">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="3a07c-126">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3a07c-127">**10**</span><span class="sxs-lookup"><span data-stu-id="3a07c-127">**10**</span></span>
</dt> <dd>

<span data-ttu-id="3a07c-128">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="3a07c-128">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3a07c-129">**11**</span><span class="sxs-lookup"><span data-stu-id="3a07c-129">**11**</span></span>
</dt> <dd>

<span data-ttu-id="3a07c-130">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="3a07c-130">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="3a07c-131">**12**</span><span class="sxs-lookup"><span data-stu-id="3a07c-131">**12**</span></span>
</dt> <dd>

<span data-ttu-id="3a07c-132">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="3a07c-132">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="3a07c-133">**13**</span><span class="sxs-lookup"><span data-stu-id="3a07c-133">**13**</span></span>
</dt> <dd>

<span data-ttu-id="3a07c-134">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="3a07c-134">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="3a07c-135">**14**</span><span class="sxs-lookup"><span data-stu-id="3a07c-135">**14**</span></span>
</dt> <dd>

<span data-ttu-id="3a07c-136">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="3a07c-136">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="3a07c-137">**15**</span><span class="sxs-lookup"><span data-stu-id="3a07c-137">**15**</span></span>
</dt> <dd>

<span data-ttu-id="3a07c-138">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="3a07c-138">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="3a07c-139">**16**</span><span class="sxs-lookup"><span data-stu-id="3a07c-139">**16**</span></span>
</dt> <dd>

<span data-ttu-id="3a07c-140">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="3a07c-140">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3a07c-141">**17**</span><span class="sxs-lookup"><span data-stu-id="3a07c-141">**17**</span></span>
</dt> <dd>

<span data-ttu-id="3a07c-142">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="3a07c-142">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="3a07c-143">**21**</span><span class="sxs-lookup"><span data-stu-id="3a07c-143">**21**</span></span>
</dt> <dd>

<span data-ttu-id="3a07c-144">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="3a07c-144">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a07c-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a07c-145">Requirements</span></span>



| <span data-ttu-id="3a07c-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a07c-146">Requirement</span></span> | <span data-ttu-id="3a07c-147">Valore</span><span class="sxs-lookup"><span data-stu-id="3a07c-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a07c-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a07c-148">Minimum supported client</span></span><br/> | <span data-ttu-id="3a07c-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a07c-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3a07c-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a07c-150">Minimum supported server</span></span><br/> | <span data-ttu-id="3a07c-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a07c-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3a07c-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3a07c-152">Namespace</span></span><br/>                | <span data-ttu-id="3a07c-153">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="3a07c-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3a07c-154">MOF</span><span class="sxs-lookup"><span data-stu-id="3a07c-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a07c-155"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a07c-155"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a07c-156">DLL</span><span class="sxs-lookup"><span data-stu-id="3a07c-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a07c-157"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a07c-157"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a07c-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a07c-158">See also</span></span>

<dl> <dt>

<span data-ttu-id="3a07c-159">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3a07c-159">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3a07c-160">**\_Pagefile Win32**</span><span class="sxs-lookup"><span data-stu-id="3a07c-160">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

