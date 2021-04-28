---
description: "Metodo Compress della classe CIM_DataFile: usa la compressione NTFS per comprimere il file logico (o la directory) specificato nel percorso dell'oggetto. Questo metodo viene ereditato da CIM \\_ LogicalFile."
ms.assetid: fce57569-8290-420e-a938-10ab08ac67c3
ms.tgt_platform: multiple
title: Metodo Compress della classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3cc63ed3cafd676a0d865953c52a14e6247d4b70
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089779"
---
# <a name="compress-method-of-the-cim_datafile-class"></a><span data-ttu-id="3806b-104">Metodo Compress della classe \_ CiM DataFile</span><span class="sxs-lookup"><span data-stu-id="3806b-104">Compress method of the CIM\_DataFile class</span></span>

<span data-ttu-id="3806b-105">Il **metodo Compress** usa la compressione NTFS per comprimere il file logico (o la directory) specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3806b-105">The **Compress** method uses NTFS compression to compress the logical file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="3806b-106">Questo metodo viene ereditato da [**CIM \_ LogicalFile.**](cim-logicalfile.md)</span><span class="sxs-lookup"><span data-stu-id="3806b-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3806b-107">Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="3806b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3806b-108">WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3806b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3806b-109">Questo argomento usa Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="3806b-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3806b-110">Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3806b-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3806b-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3806b-111">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="3806b-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="3806b-112">Parameters</span></span>

<span data-ttu-id="3806b-113">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="3806b-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3806b-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3806b-114">Return value</span></span>

<span data-ttu-id="3806b-115">Restituisce il valore 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="3806b-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="3806b-116">Per altri codici di errore, [**vedere Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)</span><span class="sxs-lookup"><span data-stu-id="3806b-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="3806b-117">Per i valori **HRESULT** generali, vedere [Codici di errore di sistema.](/windows/desktop/Debug/system-error-codes)</span><span class="sxs-lookup"><span data-stu-id="3806b-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="3806b-118">**0**</span><span class="sxs-lookup"><span data-stu-id="3806b-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="3806b-119">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="3806b-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="3806b-120">**2**</span><span class="sxs-lookup"><span data-stu-id="3806b-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="3806b-121">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="3806b-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="3806b-122">**8**</span><span class="sxs-lookup"><span data-stu-id="3806b-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="3806b-123">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="3806b-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="3806b-124">**9**</span><span class="sxs-lookup"><span data-stu-id="3806b-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="3806b-125">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="3806b-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="3806b-126">**10**</span><span class="sxs-lookup"><span data-stu-id="3806b-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="3806b-127">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="3806b-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3806b-128">**11**</span><span class="sxs-lookup"><span data-stu-id="3806b-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="3806b-129">File system non NTFS.</span><span class="sxs-lookup"><span data-stu-id="3806b-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="3806b-130">**12**</span><span class="sxs-lookup"><span data-stu-id="3806b-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="3806b-131">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="3806b-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="3806b-132">**13**</span><span class="sxs-lookup"><span data-stu-id="3806b-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="3806b-133">Unità non uguale.</span><span class="sxs-lookup"><span data-stu-id="3806b-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="3806b-134">**14**</span><span class="sxs-lookup"><span data-stu-id="3806b-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="3806b-135">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="3806b-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="3806b-136">**15**</span><span class="sxs-lookup"><span data-stu-id="3806b-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="3806b-137">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="3806b-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="3806b-138">**16**</span><span class="sxs-lookup"><span data-stu-id="3806b-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="3806b-139">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="3806b-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="3806b-140">**17**</span><span class="sxs-lookup"><span data-stu-id="3806b-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="3806b-141">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="3806b-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="3806b-142">**21**</span><span class="sxs-lookup"><span data-stu-id="3806b-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="3806b-143">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="3806b-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3806b-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="3806b-144">Remarks</span></span>

<span data-ttu-id="3806b-145">Il **metodo Compress** in [**CIM \_ DataFile**](cim-datafile.md) viene implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="3806b-145">The **Compress** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="3806b-146">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="3806b-146">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3806b-147">Microsoft potrebbe aver apportato modifiche per correggere gli errori minori, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="3806b-147">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3806b-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3806b-148">Requirements</span></span>



| <span data-ttu-id="3806b-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="3806b-149">Requirement</span></span> | <span data-ttu-id="3806b-150">Valore</span><span class="sxs-lookup"><span data-stu-id="3806b-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3806b-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3806b-151">Minimum supported client</span></span><br/> | <span data-ttu-id="3806b-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3806b-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3806b-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3806b-153">Minimum supported server</span></span><br/> | <span data-ttu-id="3806b-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3806b-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3806b-155">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3806b-155">Namespace</span></span><br/>                | <span data-ttu-id="3806b-156">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="3806b-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3806b-157">MOF</span><span class="sxs-lookup"><span data-stu-id="3806b-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3806b-158"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="3806b-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3806b-159">DLL</span><span class="sxs-lookup"><span data-stu-id="3806b-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3806b-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3806b-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3806b-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3806b-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3806b-162">**CIM \_ DataFile**</span><span class="sxs-lookup"><span data-stu-id="3806b-162">**CIM\_DataFile**</span></span>](compress-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="3806b-163">**CIM \_ DataFile**</span><span class="sxs-lookup"><span data-stu-id="3806b-163">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="3806b-164">Attività WMI: File e cartelle</span><span class="sxs-lookup"><span data-stu-id="3806b-164">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="3806b-165">**Costanti dei diritti di accesso a file e directory**</span><span class="sxs-lookup"><span data-stu-id="3806b-165">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

