---
description: Il metodo della classe WMI DeleteEx eliminerà il file logico o la directory specificata nel percorso dell'oggetto. DeleteEx è una versione estesa del metodo Delete.
ms.assetid: 6e5447c1-4d71-4a51-a1e0-b5785c13dfd2
ms.tgt_platform: multiple
title: Metodo DeleteEx della classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ac23a4013053d252aec49b8b7be4aae62c41c8e1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966068"
---
# <a name="deleteex-method-of-the-win32_directory-class"></a><span data-ttu-id="f8b28-104">Metodo DeleteEx della classe di \_ directory Win32</span><span class="sxs-lookup"><span data-stu-id="f8b28-104">DeleteEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="f8b28-105">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **DeleteEx** eliminerà il file logico o la directory specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f8b28-105">The **DeleteEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method will delete the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="f8b28-106">**DeleteEx** è una versione estesa del metodo [**Delete**](delete-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="f8b28-106">**DeleteEx** is an extended version of the [**Delete**](delete-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="f8b28-107">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="f8b28-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f8b28-108">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f8b28-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f8b28-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8b28-109">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out]          string StopFileName,
  [in, optional] string StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="f8b28-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8b28-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8b28-111">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f8b28-111">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8b28-112">Nome del file o della directory in cui il metodo **DeleteEx** non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="f8b28-112">Name of the file or directory where the **DeleteEx** method failed.</span></span> <span data-ttu-id="f8b28-113">Questo parametro sarà **null** se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="f8b28-113">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="f8b28-114">*StartFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="f8b28-114">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f8b28-115">Denomina il file o la directory figlio da utilizzare come punto di partenza per **DeleteEx**.</span><span class="sxs-lookup"><span data-stu-id="f8b28-115">Names the child file or directory to use as a starting point for **DeleteEx**.</span></span> <span data-ttu-id="f8b28-116">Il parametro *StartFileName* è in genere il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="f8b28-116">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="f8b28-117">Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificata nella chiamata ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="f8b28-117">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8b28-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f8b28-118">Return value</span></span>

<span data-ttu-id="f8b28-119">Restituisce un valore pari a 0 (zero) se il file è stato eliminato correttamente e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="f8b28-119">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="f8b28-120">**0**</span><span class="sxs-lookup"><span data-stu-id="f8b28-120">**0**</span></span>
</dt> <dd>

<span data-ttu-id="f8b28-121">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="f8b28-121">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="f8b28-122">**2**</span><span class="sxs-lookup"><span data-stu-id="f8b28-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="f8b28-123">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="f8b28-123">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="f8b28-124">**8**</span><span class="sxs-lookup"><span data-stu-id="f8b28-124">**8**</span></span>
</dt> <dd>

<span data-ttu-id="f8b28-125">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="f8b28-125">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="f8b28-126">**9**</span><span class="sxs-lookup"><span data-stu-id="f8b28-126">**9**</span></span>
</dt> <dd>

<span data-ttu-id="f8b28-127">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="f8b28-127">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f8b28-128">**10**</span><span class="sxs-lookup"><span data-stu-id="f8b28-128">**10**</span></span>
</dt> <dd>

<span data-ttu-id="f8b28-129">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="f8b28-129">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f8b28-130">**11**</span><span class="sxs-lookup"><span data-stu-id="f8b28-130">**11**</span></span>
</dt> <dd>

<span data-ttu-id="f8b28-131">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="f8b28-131">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="f8b28-132">**12**</span><span class="sxs-lookup"><span data-stu-id="f8b28-132">**12**</span></span>
</dt> <dd>

<span data-ttu-id="f8b28-133">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="f8b28-133">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="f8b28-134">**13**</span><span class="sxs-lookup"><span data-stu-id="f8b28-134">**13**</span></span>
</dt> <dd>

<span data-ttu-id="f8b28-135">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="f8b28-135">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="f8b28-136">**14**</span><span class="sxs-lookup"><span data-stu-id="f8b28-136">**14**</span></span>
</dt> <dd>

<span data-ttu-id="f8b28-137">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="f8b28-137">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="f8b28-138">**15**</span><span class="sxs-lookup"><span data-stu-id="f8b28-138">**15**</span></span>
</dt> <dd>

<span data-ttu-id="f8b28-139">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="f8b28-139">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="f8b28-140">**16**</span><span class="sxs-lookup"><span data-stu-id="f8b28-140">**16**</span></span>
</dt> <dd>

<span data-ttu-id="f8b28-141">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="f8b28-141">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f8b28-142">**17**</span><span class="sxs-lookup"><span data-stu-id="f8b28-142">**17**</span></span>
</dt> <dd>

<span data-ttu-id="f8b28-143">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="f8b28-143">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="f8b28-144">**21**</span><span class="sxs-lookup"><span data-stu-id="f8b28-144">**21**</span></span>
</dt> <dd>

<span data-ttu-id="f8b28-145">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="f8b28-145">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f8b28-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8b28-146">Requirements</span></span>



| <span data-ttu-id="f8b28-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8b28-147">Requirement</span></span> | <span data-ttu-id="f8b28-148">Valore</span><span class="sxs-lookup"><span data-stu-id="f8b28-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8b28-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8b28-149">Minimum supported client</span></span><br/> | <span data-ttu-id="f8b28-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8b28-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f8b28-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8b28-151">Minimum supported server</span></span><br/> | <span data-ttu-id="f8b28-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8b28-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f8b28-153">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f8b28-153">Namespace</span></span><br/>                | <span data-ttu-id="f8b28-154">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f8b28-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f8b28-155">MOF</span><span class="sxs-lookup"><span data-stu-id="f8b28-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8b28-156"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8b28-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8b28-157">DLL</span><span class="sxs-lookup"><span data-stu-id="f8b28-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8b28-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8b28-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8b28-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8b28-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="f8b28-160">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f8b28-160">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f8b28-161">**\_Directory Win32**</span><span class="sxs-lookup"><span data-stu-id="f8b28-161">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

