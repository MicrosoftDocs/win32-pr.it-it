---
description: "Metodo CompressEx della classe CIM_DataFile : usa la compressione NTFS per comprimere il file logico (o la directory) specificato nel percorso dell'oggetto. Questo metodo viene ereditato da CIM \\_ LogicalFile."
ms.assetid: 553b6a90-d16c-4abb-9015-66fe8e1606f6
ms.tgt_platform: multiple
title: Metodo CompressEx della classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ccc155c04c6c25f38050bd37827eb0c2e2e0e73e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089789"
---
# <a name="compressex-method-of-the-cim_datafile-class"></a><span data-ttu-id="cc58b-104">Metodo CompressEx della classe \_ CiM DataFile</span><span class="sxs-lookup"><span data-stu-id="cc58b-104">CompressEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="cc58b-105">Il **metodo CompressEx** usa la compressione NTFS per comprimere il file logico (o la directory) specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cc58b-105">The **CompressEx** method uses NTFS compression to compress the logical file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="cc58b-106">Questo metodo viene ereditato da [**CIM \_ LogicalFile.**](cim-logicalfile.md)</span><span class="sxs-lookup"><span data-stu-id="cc58b-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span> <span data-ttu-id="cc58b-107">Questo metodo è una versione estesa del [**metodo Compress**](compress-method-in-class-cim-datafile.md) ed è ereditato da [CIM \_ LogicalFile.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="cc58b-107">This method is an extended version of the [**Compress**](compress-method-in-class-cim-datafile.md) method and is inherited from [CIM\_LogicalFile](/windows/desktop/WmiSdk/calling-a-method).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cc58b-108">Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="cc58b-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cc58b-109">WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cc58b-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cc58b-110">Questo argomento usa Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="cc58b-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cc58b-111">Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="cc58b-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cc58b-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cc58b-112">Syntax</span></span>


```mof
uint32 CompressEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="cc58b-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="cc58b-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc58b-114">*StopFileName* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="cc58b-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc58b-115">Stringa che rappresenta il nome del file (o directory) in cui il metodo non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="cc58b-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="cc58b-116">Questo parametro è Null se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="cc58b-116">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="cc58b-117">*StartFileName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="cc58b-117">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc58b-118">Stringa che rappresenta il file figlio (o la directory) da usare come punto di partenza per questo metodo.</span><span class="sxs-lookup"><span data-stu-id="cc58b-118">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="cc58b-119">In genere, il *parametro StartFileName* è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="cc58b-119">Typically, the *StartFileName* parameter is the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="cc58b-120">Se questo parametro è Null, l'operazione viene eseguita sul file o sulla directory specificata nella **chiamata a ExecMethod.**</span><span class="sxs-lookup"><span data-stu-id="cc58b-120">If this parameter is null, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="cc58b-121">Se *si usa StartFileName,* *anche Recursive* deve essere impostato su true.</span><span class="sxs-lookup"><span data-stu-id="cc58b-121">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="cc58b-122">*Ricorsivo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="cc58b-122">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc58b-123">Se **TRUE,** il metodo viene applicato in modo ricorsivo anche ai file e alle directory all'interno della directory specificata [**dall'istanza di CIM \_ DataFile.**](cim-datafile.md)</span><span class="sxs-lookup"><span data-stu-id="cc58b-123">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="cc58b-124">Per le istanze di file, questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="cc58b-124">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc58b-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cc58b-125">Return value</span></span>

<span data-ttu-id="cc58b-126">Restituisce il valore 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="cc58b-126">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="cc58b-127">Per altri codici di errore, vedere [**Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="cc58b-127">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="cc58b-128">Per i valori **HRESULT** generali, vedere [Codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="cc58b-128">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="cc58b-129">**0**</span><span class="sxs-lookup"><span data-stu-id="cc58b-129">**0**</span></span>
</dt> <dd>

<span data-ttu-id="cc58b-130">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="cc58b-130">Success.</span></span>

</dd> <dt>

<span data-ttu-id="cc58b-131">**2**</span><span class="sxs-lookup"><span data-stu-id="cc58b-131">**2**</span></span>
</dt> <dd>

<span data-ttu-id="cc58b-132">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="cc58b-132">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="cc58b-133">**8**</span><span class="sxs-lookup"><span data-stu-id="cc58b-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="cc58b-134">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="cc58b-134">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="cc58b-135">**9**</span><span class="sxs-lookup"><span data-stu-id="cc58b-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="cc58b-136">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="cc58b-136">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="cc58b-137">**10**</span><span class="sxs-lookup"><span data-stu-id="cc58b-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="cc58b-138">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="cc58b-138">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="cc58b-139">**11**</span><span class="sxs-lookup"><span data-stu-id="cc58b-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="cc58b-140">File system non NTFS.</span><span class="sxs-lookup"><span data-stu-id="cc58b-140">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="cc58b-141">**12**</span><span class="sxs-lookup"><span data-stu-id="cc58b-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="cc58b-142">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="cc58b-142">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="cc58b-143">**13**</span><span class="sxs-lookup"><span data-stu-id="cc58b-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="cc58b-144">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="cc58b-144">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="cc58b-145">**14**</span><span class="sxs-lookup"><span data-stu-id="cc58b-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="cc58b-146">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="cc58b-146">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="cc58b-147">**15**</span><span class="sxs-lookup"><span data-stu-id="cc58b-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="cc58b-148">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="cc58b-148">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="cc58b-149">**16**</span><span class="sxs-lookup"><span data-stu-id="cc58b-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="cc58b-150">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="cc58b-150">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="cc58b-151">**17**</span><span class="sxs-lookup"><span data-stu-id="cc58b-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="cc58b-152">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="cc58b-152">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="cc58b-153">**21**</span><span class="sxs-lookup"><span data-stu-id="cc58b-153">**21**</span></span>
</dt> <dd>

<span data-ttu-id="cc58b-154">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="cc58b-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc58b-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="cc58b-155">Remarks</span></span>

<span data-ttu-id="cc58b-156">Il **metodo CompressEx** in [**CIM \_ DataFile**](cim-datafile.md) viene implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="cc58b-156">The **CompressEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="cc58b-157">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="cc58b-157">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cc58b-158">Microsoft potrebbe aver apportato modifiche per correggere gli errori minori, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="cc58b-158">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc58b-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc58b-159">Requirements</span></span>



| <span data-ttu-id="cc58b-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc58b-160">Requirement</span></span> | <span data-ttu-id="cc58b-161">Valore</span><span class="sxs-lookup"><span data-stu-id="cc58b-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc58b-162">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc58b-162">Minimum supported client</span></span><br/> | <span data-ttu-id="cc58b-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cc58b-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cc58b-164">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc58b-164">Minimum supported server</span></span><br/> | <span data-ttu-id="cc58b-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc58b-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cc58b-166">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cc58b-166">Namespace</span></span><br/>                | <span data-ttu-id="cc58b-167">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="cc58b-167">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cc58b-168">MOF</span><span class="sxs-lookup"><span data-stu-id="cc58b-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc58b-169"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc58b-169"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cc58b-170">DLL</span><span class="sxs-lookup"><span data-stu-id="cc58b-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc58b-171"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc58b-171"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc58b-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc58b-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc58b-173">CIM \_ DataFile</span><span class="sxs-lookup"><span data-stu-id="cc58b-173">CIM\_DataFile</span></span>](compressex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="cc58b-174">**CIM \_ DataFile**</span><span class="sxs-lookup"><span data-stu-id="cc58b-174">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="cc58b-175">Attività WMI: File e cartelle</span><span class="sxs-lookup"><span data-stu-id="cc58b-175">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="cc58b-176">**Costanti dei diritti di accesso a file e directory**</span><span class="sxs-lookup"><span data-stu-id="cc58b-176">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

