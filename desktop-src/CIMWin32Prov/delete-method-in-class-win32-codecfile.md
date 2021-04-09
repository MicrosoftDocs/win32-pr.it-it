---
description: Elimina il file o la directory del codec audio o video, specificato nel percorso dell'oggetto.
ms.assetid: 70233615-8924-4bd4-8a20-279a18b5c807
ms.tgt_platform: multiple
title: Metodo Delete della classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9d9395f5c5ebaf2948043fe43e84685e4c39d4d0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878322"
---
# <a name="delete-method-of-the-win32_codecfile-class"></a><span data-ttu-id="ca023-103">Metodo Delete della \_ classe Sqlcfile Win32</span><span class="sxs-lookup"><span data-stu-id="ca023-103">Delete method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="ca023-104">Il metodo **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) Elimina il file o la directory del codec audio o video, o directory, specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ca023-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes the logical audio or video codec file (or directory) specified in the object path.</span></span>

<span data-ttu-id="ca023-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="ca023-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ca023-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ca023-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ca023-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca023-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="ca023-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca023-108">Parameters</span></span>

<span data-ttu-id="ca023-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ca023-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ca023-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ca023-110">Return value</span></span>

<span data-ttu-id="ca023-111">Restituisce un valore pari a 0 (zero) se il file è stato eliminato correttamente e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="ca023-111">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="ca023-112">**0**</span><span class="sxs-lookup"><span data-stu-id="ca023-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="ca023-113">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="ca023-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="ca023-114">**2**</span><span class="sxs-lookup"><span data-stu-id="ca023-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="ca023-115">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="ca023-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="ca023-116">**8**</span><span class="sxs-lookup"><span data-stu-id="ca023-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="ca023-117">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="ca023-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="ca023-118">**9**</span><span class="sxs-lookup"><span data-stu-id="ca023-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="ca023-119">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="ca023-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ca023-120">**10**</span><span class="sxs-lookup"><span data-stu-id="ca023-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="ca023-121">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="ca023-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="ca023-122">**11**</span><span class="sxs-lookup"><span data-stu-id="ca023-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="ca023-123">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="ca023-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="ca023-124">**12**</span><span class="sxs-lookup"><span data-stu-id="ca023-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="ca023-125">La piattaforma non è Windows NT o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ca023-125">The platform is not Windows NT or Windows 2000.</span></span>

</dd> <dt>

<span data-ttu-id="ca023-126">**13**</span><span class="sxs-lookup"><span data-stu-id="ca023-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="ca023-127">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="ca023-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="ca023-128">**14**</span><span class="sxs-lookup"><span data-stu-id="ca023-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="ca023-129">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="ca023-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="ca023-130">**15**</span><span class="sxs-lookup"><span data-stu-id="ca023-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="ca023-131">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="ca023-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="ca023-132">**16**</span><span class="sxs-lookup"><span data-stu-id="ca023-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="ca023-133">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="ca023-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ca023-134">**17**</span><span class="sxs-lookup"><span data-stu-id="ca023-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="ca023-135">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="ca023-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="ca023-136">**21**</span><span class="sxs-lookup"><span data-stu-id="ca023-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="ca023-137">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="ca023-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca023-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca023-138">Requirements</span></span>



| <span data-ttu-id="ca023-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca023-139">Requirement</span></span> | <span data-ttu-id="ca023-140">Valore</span><span class="sxs-lookup"><span data-stu-id="ca023-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca023-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca023-141">Minimum supported client</span></span><br/> | <span data-ttu-id="ca023-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca023-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ca023-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca023-143">Minimum supported server</span></span><br/> | <span data-ttu-id="ca023-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca023-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ca023-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ca023-145">Namespace</span></span><br/>                | <span data-ttu-id="ca023-146">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ca023-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ca023-147">MOF</span><span class="sxs-lookup"><span data-stu-id="ca023-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca023-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca023-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca023-149">DLL</span><span class="sxs-lookup"><span data-stu-id="ca023-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca023-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca023-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca023-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca023-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="ca023-152">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ca023-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ca023-153">**Codecfile Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="ca023-153">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

