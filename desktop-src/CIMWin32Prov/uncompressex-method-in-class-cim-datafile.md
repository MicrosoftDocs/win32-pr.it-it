---
description: Decomprime il file di dati logico o la directory specificata nel percorso dell'oggetto. Questo metodo è una versione estesa del metodo Decompress ed è ereditato da CIM \_ LogicalFile.
ms.assetid: 30b62930-1d4a-47c0-8b57-b460edb5dbd0
ms.tgt_platform: multiple
title: Metodo UncompressEx della classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0d11585a834ecc357447394ce09b73698bf2de86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127510"
---
# <a name="uncompressex-method-of-the-cim_datafile-class"></a><span data-ttu-id="b88fc-104">Metodo UncompressEx della classe del file di \_ DataFile CIM</span><span class="sxs-lookup"><span data-stu-id="b88fc-104">UncompressEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="b88fc-105">Il metodo **UncompressEx** decomprime il file di dati logico o la directory specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b88fc-105">The **UncompressEx** method uncompresses the logical data file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="b88fc-106">Questo metodo è una versione estesa del metodo [**Decompress**](uncompress-method-in-class-cim-datafile.md) ed è ereditato da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b88fc-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-cim-datafile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b88fc-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="b88fc-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b88fc-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b88fc-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b88fc-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="b88fc-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b88fc-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b88fc-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b88fc-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b88fc-111">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="b88fc-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="b88fc-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b88fc-113">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b88fc-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b88fc-114">Nome del file o della directory in cui il metodo ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b88fc-114">Name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="b88fc-115">Questo parametro è **null** se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b88fc-115">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="b88fc-116">*StartFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b88fc-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b88fc-117">File figlio (o directory) da utilizzare come punto di partenza per questo metodo.</span><span class="sxs-lookup"><span data-stu-id="b88fc-117">Child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="b88fc-118">In genere, il parametro *StartFileName* è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="b88fc-118">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="b88fc-119">Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificati nella chiamata [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="b88fc-119">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

<span data-ttu-id="b88fc-120">Se si usa *StartFileName* , è necessario impostare *ricorsivo* su true.</span><span class="sxs-lookup"><span data-stu-id="b88fc-120">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="b88fc-121">*Ricorsivo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b88fc-121">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b88fc-122">Se **true**, il metodo viene anche applicato in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza di [**\_ DataFile DataFile**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="b88fc-122">If **TRUE**, the method is also applied recursively to files and directories within the directory that is specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="b88fc-123">Per le istanze di file, questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="b88fc-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b88fc-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b88fc-124">Return value</span></span>

<span data-ttu-id="b88fc-125">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="b88fc-125">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="b88fc-126">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="b88fc-126">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b88fc-127">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="b88fc-127">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b88fc-128">**0**</span><span class="sxs-lookup"><span data-stu-id="b88fc-128">**0**</span></span>
</dt> <dd>

<span data-ttu-id="b88fc-129">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b88fc-129">Success.</span></span>

</dd> <dt>

<span data-ttu-id="b88fc-130">**2**</span><span class="sxs-lookup"><span data-stu-id="b88fc-130">**2**</span></span>
</dt> <dd>

<span data-ttu-id="b88fc-131">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="b88fc-131">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="b88fc-132">**8**</span><span class="sxs-lookup"><span data-stu-id="b88fc-132">**8**</span></span>
</dt> <dd>

<span data-ttu-id="b88fc-133">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="b88fc-133">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="b88fc-134">**9**</span><span class="sxs-lookup"><span data-stu-id="b88fc-134">**9**</span></span>
</dt> <dd>

<span data-ttu-id="b88fc-135">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="b88fc-135">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="b88fc-136">**10**</span><span class="sxs-lookup"><span data-stu-id="b88fc-136">**10**</span></span>
</dt> <dd>

<span data-ttu-id="b88fc-137">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="b88fc-137">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b88fc-138">**11**</span><span class="sxs-lookup"><span data-stu-id="b88fc-138">**11**</span></span>
</dt> <dd>

<span data-ttu-id="b88fc-139">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="b88fc-139">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="b88fc-140">**12**</span><span class="sxs-lookup"><span data-stu-id="b88fc-140">**12**</span></span>
</dt> <dd>

<span data-ttu-id="b88fc-141">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="b88fc-141">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="b88fc-142">**13**</span><span class="sxs-lookup"><span data-stu-id="b88fc-142">**13**</span></span>
</dt> <dd>

<span data-ttu-id="b88fc-143">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="b88fc-143">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="b88fc-144">**14**</span><span class="sxs-lookup"><span data-stu-id="b88fc-144">**14**</span></span>
</dt> <dd>

<span data-ttu-id="b88fc-145">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="b88fc-145">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="b88fc-146">**15**</span><span class="sxs-lookup"><span data-stu-id="b88fc-146">**15**</span></span>
</dt> <dd>

<span data-ttu-id="b88fc-147">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="b88fc-147">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="b88fc-148">**16**</span><span class="sxs-lookup"><span data-stu-id="b88fc-148">**16**</span></span>
</dt> <dd>

<span data-ttu-id="b88fc-149">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="b88fc-149">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="b88fc-150">**17**</span><span class="sxs-lookup"><span data-stu-id="b88fc-150">**17**</span></span>
</dt> <dd>

<span data-ttu-id="b88fc-151">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="b88fc-151">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="b88fc-152">**21**</span><span class="sxs-lookup"><span data-stu-id="b88fc-152">**21**</span></span>
</dt> <dd>

<span data-ttu-id="b88fc-153">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="b88fc-153">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b88fc-154">Commenti</span><span class="sxs-lookup"><span data-stu-id="b88fc-154">Remarks</span></span>

<span data-ttu-id="b88fc-155">Il metodo **UncompressEx** nel file di [**\_ DataFile CIM**](cim-datafile.md) viene implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="b88fc-155">The **UncompressEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="b88fc-156">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="b88fc-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b88fc-157">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="b88fc-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b88fc-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b88fc-158">Requirements</span></span>



| <span data-ttu-id="b88fc-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="b88fc-159">Requirement</span></span> | <span data-ttu-id="b88fc-160">Valore</span><span class="sxs-lookup"><span data-stu-id="b88fc-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b88fc-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b88fc-161">Minimum supported client</span></span><br/> | <span data-ttu-id="b88fc-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b88fc-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b88fc-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b88fc-163">Minimum supported server</span></span><br/> | <span data-ttu-id="b88fc-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b88fc-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b88fc-165">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b88fc-165">Namespace</span></span><br/>                | <span data-ttu-id="b88fc-166">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="b88fc-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b88fc-167">MOF</span><span class="sxs-lookup"><span data-stu-id="b88fc-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b88fc-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b88fc-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b88fc-169">DLL</span><span class="sxs-lookup"><span data-stu-id="b88fc-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b88fc-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b88fc-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b88fc-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b88fc-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b88fc-172">**File di \_ DataFile CIM**</span><span class="sxs-lookup"><span data-stu-id="b88fc-172">**CIM\_DataFile**</span></span>](uncompressex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="b88fc-173">**File di \_ DataFile CIM**</span><span class="sxs-lookup"><span data-stu-id="b88fc-173">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="b88fc-174">Attività WMI: file e cartelle</span><span class="sxs-lookup"><span data-stu-id="b88fc-174">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="b88fc-175">**Costanti dei diritti di accesso a file e directory**</span><span class="sxs-lookup"><span data-stu-id="b88fc-175">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

