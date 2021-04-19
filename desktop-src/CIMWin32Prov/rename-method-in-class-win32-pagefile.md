---
description: Rinomina il file di paging specificato nel percorso dell'oggetto.
ms.assetid: 6a98e05f-337e-4224-a847-f01913031b20
ms.tgt_platform: multiple
title: Rinominare il metodo della classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c9ba8162cd115a567e9e9010420c558061fed08
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304435"
---
# <a name="rename-method-of-the-win32_pagefile-class"></a><span data-ttu-id="06046-103">Rinominare il metodo della \_ classe Win32 pagefile</span><span class="sxs-lookup"><span data-stu-id="06046-103">Rename method of the Win32\_PageFile class</span></span>

<span data-ttu-id="06046-104">Il metodo **Rinomina** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) Rinomina il file di paging specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="06046-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames the paging file specified in the object path.</span></span> <span data-ttu-id="06046-105">Una ridenominazione non è supportata se la destinazione si trova in un'altra unità o se è necessario sovrascrivere un file logico esistente.</span><span class="sxs-lookup"><span data-stu-id="06046-105">A rename is not supported if the destination is on another drive or if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="06046-106">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="06046-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="06046-107">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="06046-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="06046-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06046-108">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="06046-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="06046-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06046-110">*Nome file* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06046-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06046-111">Nome completo del nuovo file (o directory).</span><span class="sxs-lookup"><span data-stu-id="06046-111">Fully qualified new name of the file (or directory).</span></span>

<span data-ttu-id="06046-112">Esempio: c: \\ temp \\newfile.txt</span><span class="sxs-lookup"><span data-stu-id="06046-112">Example: c:\\temp\\newfile.txt</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06046-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="06046-113">Return value</span></span>

<span data-ttu-id="06046-114">Restituisce un valore pari a 0 (zero) se il file è stato rinominato correttamente e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="06046-114">Returns a value of 0 (zero) if the file was successfully renamed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="06046-115">**0**</span><span class="sxs-lookup"><span data-stu-id="06046-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="06046-116">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="06046-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="06046-117">**2**</span><span class="sxs-lookup"><span data-stu-id="06046-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="06046-118">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="06046-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="06046-119">**8**</span><span class="sxs-lookup"><span data-stu-id="06046-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="06046-120">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="06046-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="06046-121">**9**</span><span class="sxs-lookup"><span data-stu-id="06046-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="06046-122">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="06046-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="06046-123">**10**</span><span class="sxs-lookup"><span data-stu-id="06046-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="06046-124">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="06046-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="06046-125">**11**</span><span class="sxs-lookup"><span data-stu-id="06046-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="06046-126">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="06046-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="06046-127">**12**</span><span class="sxs-lookup"><span data-stu-id="06046-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="06046-128">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="06046-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="06046-129">**13**</span><span class="sxs-lookup"><span data-stu-id="06046-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="06046-130">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="06046-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="06046-131">**14**</span><span class="sxs-lookup"><span data-stu-id="06046-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="06046-132">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="06046-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="06046-133">**15**</span><span class="sxs-lookup"><span data-stu-id="06046-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="06046-134">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="06046-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="06046-135">**16**</span><span class="sxs-lookup"><span data-stu-id="06046-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="06046-136">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="06046-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="06046-137">**17**</span><span class="sxs-lookup"><span data-stu-id="06046-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="06046-138">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="06046-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="06046-139">**21**</span><span class="sxs-lookup"><span data-stu-id="06046-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="06046-140">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="06046-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="06046-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06046-141">Requirements</span></span>



| <span data-ttu-id="06046-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="06046-142">Requirement</span></span> | <span data-ttu-id="06046-143">Valore</span><span class="sxs-lookup"><span data-stu-id="06046-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06046-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06046-144">Minimum supported client</span></span><br/> | <span data-ttu-id="06046-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06046-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="06046-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06046-146">Minimum supported server</span></span><br/> | <span data-ttu-id="06046-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06046-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="06046-148">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="06046-148">Namespace</span></span><br/>                | <span data-ttu-id="06046-149">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="06046-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="06046-150">MOF</span><span class="sxs-lookup"><span data-stu-id="06046-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06046-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06046-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="06046-152">DLL</span><span class="sxs-lookup"><span data-stu-id="06046-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06046-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06046-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06046-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06046-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="06046-155">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="06046-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="06046-156">**\_Pagefile Win32**</span><span class="sxs-lookup"><span data-stu-id="06046-156">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

