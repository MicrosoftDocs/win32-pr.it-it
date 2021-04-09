---
description: Eliminare il file o la directory del codec audio o video (o directory) logica specificata nel percorso dell'oggetto.
ms.assetid: df85c8a4-3be3-4bde-b36e-6bc8af6495a9
ms.tgt_platform: multiple
title: Metodo DeleteEx della classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: df5527be497176f167ac368b872253fa3254a404
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877609"
---
# <a name="deleteex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="5523e-103">Metodo DeleteEx della \_ classe Sqlcfile Win32</span><span class="sxs-lookup"><span data-stu-id="5523e-103">DeleteEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="5523e-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **DeleteEx** eliminerà il file (o la directory) del codec audio o video di un codec logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5523e-104">The **DeleteEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method will delete the logical audio or video codec file (or directory) specified in the object path.</span></span> <span data-ttu-id="5523e-105">**DeleteEx** è una versione estesa del metodo [**Delete**](delete-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="5523e-105">**DeleteEx** is an extended version of the [**Delete**](delete-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="5523e-106">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="5523e-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5523e-107">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5523e-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5523e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5523e-108">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out] string StopFileName,
  [in]  String StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="5523e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5523e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5523e-110">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5523e-110">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5523e-111">Nome del file o della directory in cui il metodo **DeleteEx** non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="5523e-111">Name of the file or directory where the **DeleteEx** method failed.</span></span> <span data-ttu-id="5523e-112">Questo parametro sarà **null** se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5523e-112">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="5523e-113">*StartFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5523e-113">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5523e-114">Denomina il file o la directory figlio da utilizzare come punto di partenza per **DeleteEx**.</span><span class="sxs-lookup"><span data-stu-id="5523e-114">Names the child file or directory to use as a starting point for **DeleteEx**.</span></span> <span data-ttu-id="5523e-115">Il parametro *StartFileName* è in genere il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="5523e-115">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="5523e-116">Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificata nella chiamata **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="5523e-116">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span> <span data-ttu-id="5523e-117">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5523e-117">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5523e-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5523e-118">Return value</span></span>

<span data-ttu-id="5523e-119">Restituisce un valore intero pari a 0 (zero) se il file è stato eliminato correttamente e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="5523e-119">Returns an integer value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="5523e-120">**0**</span><span class="sxs-lookup"><span data-stu-id="5523e-120">**0**</span></span>
</dt> <dd>

<span data-ttu-id="5523e-121">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="5523e-121">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="5523e-122">**2**</span><span class="sxs-lookup"><span data-stu-id="5523e-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="5523e-123">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="5523e-123">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="5523e-124">**8**</span><span class="sxs-lookup"><span data-stu-id="5523e-124">**8**</span></span>
</dt> <dd>

<span data-ttu-id="5523e-125">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="5523e-125">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="5523e-126">**9**</span><span class="sxs-lookup"><span data-stu-id="5523e-126">**9**</span></span>
</dt> <dd>

<span data-ttu-id="5523e-127">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="5523e-127">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5523e-128">**10**</span><span class="sxs-lookup"><span data-stu-id="5523e-128">**10**</span></span>
</dt> <dd>

<span data-ttu-id="5523e-129">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="5523e-129">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="5523e-130">**11**</span><span class="sxs-lookup"><span data-stu-id="5523e-130">**11**</span></span>
</dt> <dd>

<span data-ttu-id="5523e-131">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="5523e-131">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="5523e-132">**12**</span><span class="sxs-lookup"><span data-stu-id="5523e-132">**12**</span></span>
</dt> <dd>

<span data-ttu-id="5523e-133">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="5523e-133">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="5523e-134">**13**</span><span class="sxs-lookup"><span data-stu-id="5523e-134">**13**</span></span>
</dt> <dd>

<span data-ttu-id="5523e-135">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="5523e-135">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="5523e-136">**14**</span><span class="sxs-lookup"><span data-stu-id="5523e-136">**14**</span></span>
</dt> <dd>

<span data-ttu-id="5523e-137">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="5523e-137">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="5523e-138">**15**</span><span class="sxs-lookup"><span data-stu-id="5523e-138">**15**</span></span>
</dt> <dd>

<span data-ttu-id="5523e-139">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="5523e-139">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="5523e-140">**16**</span><span class="sxs-lookup"><span data-stu-id="5523e-140">**16**</span></span>
</dt> <dd>

<span data-ttu-id="5523e-141">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="5523e-141">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5523e-142">**17**</span><span class="sxs-lookup"><span data-stu-id="5523e-142">**17**</span></span>
</dt> <dd>

<span data-ttu-id="5523e-143">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="5523e-143">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="5523e-144">**21**</span><span class="sxs-lookup"><span data-stu-id="5523e-144">**21**</span></span>
</dt> <dd>

<span data-ttu-id="5523e-145">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="5523e-145">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5523e-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5523e-146">Requirements</span></span>



| <span data-ttu-id="5523e-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="5523e-147">Requirement</span></span> | <span data-ttu-id="5523e-148">Valore</span><span class="sxs-lookup"><span data-stu-id="5523e-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5523e-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5523e-149">Minimum supported client</span></span><br/> | <span data-ttu-id="5523e-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5523e-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5523e-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5523e-151">Minimum supported server</span></span><br/> | <span data-ttu-id="5523e-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5523e-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5523e-153">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5523e-153">Namespace</span></span><br/>                | <span data-ttu-id="5523e-154">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="5523e-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5523e-155">MOF</span><span class="sxs-lookup"><span data-stu-id="5523e-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5523e-156"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5523e-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5523e-157">DLL</span><span class="sxs-lookup"><span data-stu-id="5523e-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5523e-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5523e-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5523e-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5523e-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="5523e-160">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5523e-160">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5523e-161">**Codecfile Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="5523e-161">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

