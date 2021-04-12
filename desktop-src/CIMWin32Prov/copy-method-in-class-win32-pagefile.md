---
description: Copia il file o la directory di paging logica specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.
ms.assetid: e1ff3e91-dc30-4849-b80a-8838b527ad63
ms.tgt_platform: multiple
title: Metodo Copy della classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bde9e0b5cf9b8ab88b5efa1c6aae58a9b8a54cfb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225673"
---
# <a name="copy-method-of-the-win32_pagefile-class"></a><span data-ttu-id="eb7d0-103">Metodo Copy della \_ classe pagefile Win32</span><span class="sxs-lookup"><span data-stu-id="eb7d0-103">Copy method of the Win32\_PageFile class</span></span>

<span data-ttu-id="eb7d0-104">Il metodo **Copy** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) copia il file di paging logico o la directory specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.</span><span class="sxs-lookup"><span data-stu-id="eb7d0-104">The **Copy** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical paging file or directory specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="eb7d0-105">Una copia non è supportata se è necessario sovrascrivere un file logico esistente.</span><span class="sxs-lookup"><span data-stu-id="eb7d0-105">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="eb7d0-106">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="eb7d0-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="eb7d0-107">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="eb7d0-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb7d0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eb7d0-108">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="eb7d0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="eb7d0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb7d0-110">*Nome file* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb7d0-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb7d0-111">Nome completo della copia del file (o directory).</span><span class="sxs-lookup"><span data-stu-id="eb7d0-111">Fully qualified name of the copy of the file (or directory).</span></span>

<span data-ttu-id="eb7d0-112">Esempio: c: \\ temp \\ NewDirectory</span><span class="sxs-lookup"><span data-stu-id="eb7d0-112">Example: c:\\temp\\newdirectory</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb7d0-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eb7d0-113">Return value</span></span>

<span data-ttu-id="eb7d0-114">Restituisce un valore pari a 0 (zero) se il file è stato copiato correttamente e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="eb7d0-114">Returns a value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="eb7d0-115">**0**</span><span class="sxs-lookup"><span data-stu-id="eb7d0-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="eb7d0-116">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="eb7d0-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="eb7d0-117">**2**</span><span class="sxs-lookup"><span data-stu-id="eb7d0-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="eb7d0-118">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="eb7d0-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="eb7d0-119">**8**</span><span class="sxs-lookup"><span data-stu-id="eb7d0-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="eb7d0-120">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="eb7d0-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="eb7d0-121">**9**</span><span class="sxs-lookup"><span data-stu-id="eb7d0-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="eb7d0-122">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="eb7d0-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="eb7d0-123">**10**</span><span class="sxs-lookup"><span data-stu-id="eb7d0-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="eb7d0-124">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="eb7d0-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="eb7d0-125">**11**</span><span class="sxs-lookup"><span data-stu-id="eb7d0-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="eb7d0-126">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="eb7d0-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="eb7d0-127">**12**</span><span class="sxs-lookup"><span data-stu-id="eb7d0-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="eb7d0-128">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="eb7d0-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="eb7d0-129">**13**</span><span class="sxs-lookup"><span data-stu-id="eb7d0-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="eb7d0-130">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="eb7d0-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="eb7d0-131">**14**</span><span class="sxs-lookup"><span data-stu-id="eb7d0-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="eb7d0-132">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="eb7d0-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="eb7d0-133">**15**</span><span class="sxs-lookup"><span data-stu-id="eb7d0-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="eb7d0-134">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="eb7d0-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="eb7d0-135">**16**</span><span class="sxs-lookup"><span data-stu-id="eb7d0-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="eb7d0-136">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="eb7d0-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="eb7d0-137">**17**</span><span class="sxs-lookup"><span data-stu-id="eb7d0-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="eb7d0-138">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="eb7d0-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="eb7d0-139">**21**</span><span class="sxs-lookup"><span data-stu-id="eb7d0-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="eb7d0-140">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="eb7d0-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eb7d0-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb7d0-141">Requirements</span></span>



| <span data-ttu-id="eb7d0-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb7d0-142">Requirement</span></span> | <span data-ttu-id="eb7d0-143">Valore</span><span class="sxs-lookup"><span data-stu-id="eb7d0-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb7d0-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb7d0-144">Minimum supported client</span></span><br/> | <span data-ttu-id="eb7d0-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb7d0-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eb7d0-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb7d0-146">Minimum supported server</span></span><br/> | <span data-ttu-id="eb7d0-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb7d0-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eb7d0-148">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="eb7d0-148">Namespace</span></span><br/>                | <span data-ttu-id="eb7d0-149">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="eb7d0-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eb7d0-150">MOF</span><span class="sxs-lookup"><span data-stu-id="eb7d0-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb7d0-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb7d0-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb7d0-152">DLL</span><span class="sxs-lookup"><span data-stu-id="eb7d0-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb7d0-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb7d0-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb7d0-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb7d0-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="eb7d0-155">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eb7d0-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="eb7d0-156">**\_Pagefile Win32**</span><span class="sxs-lookup"><span data-stu-id="eb7d0-156">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

