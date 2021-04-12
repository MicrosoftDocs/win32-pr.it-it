---
description: Decomprime il file di dati logico o la directory specificata nel percorso dell'oggetto. Questo metodo viene ereditato da \_ LOGICALFILE CIM.
ms.assetid: 0966ba13-8bbc-4283-919a-7675444409be
ms.tgt_platform: multiple
title: Metodo Decompress della classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 24495c94cca0eb6b99bc209cad8f25fac8f66896
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482981"
---
# <a name="uncompress-method-of-the-cim_datafile-class"></a><span data-ttu-id="303a2-104">Metodo Decompress della classe di file di \_ Codice CIM</span><span class="sxs-lookup"><span data-stu-id="303a2-104">Uncompress method of the CIM\_DataFile class</span></span>

<span data-ttu-id="303a2-105">Il metodo **uncompress** decomprime il file di dati logico o la directory specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="303a2-105">The **Uncompress** method uncompresses the logical data file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="303a2-106">Questo metodo viene ereditato da [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="303a2-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="303a2-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="303a2-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="303a2-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="303a2-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="303a2-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="303a2-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="303a2-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="303a2-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="303a2-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="303a2-111">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="303a2-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="303a2-112">Parameters</span></span>

<span data-ttu-id="303a2-113">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="303a2-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="303a2-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="303a2-114">Return value</span></span>

<span data-ttu-id="303a2-115">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="303a2-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="303a2-116">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="303a2-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="303a2-117">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="303a2-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="303a2-118">**0**</span><span class="sxs-lookup"><span data-stu-id="303a2-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="303a2-119">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="303a2-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="303a2-120">**2**</span><span class="sxs-lookup"><span data-stu-id="303a2-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="303a2-121">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="303a2-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="303a2-122">**8**</span><span class="sxs-lookup"><span data-stu-id="303a2-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="303a2-123">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="303a2-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="303a2-124">**9**</span><span class="sxs-lookup"><span data-stu-id="303a2-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="303a2-125">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="303a2-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="303a2-126">**10**</span><span class="sxs-lookup"><span data-stu-id="303a2-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="303a2-127">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="303a2-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="303a2-128">**11**</span><span class="sxs-lookup"><span data-stu-id="303a2-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="303a2-129">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="303a2-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="303a2-130">**12**</span><span class="sxs-lookup"><span data-stu-id="303a2-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="303a2-131">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="303a2-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="303a2-132">**13**</span><span class="sxs-lookup"><span data-stu-id="303a2-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="303a2-133">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="303a2-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="303a2-134">**14**</span><span class="sxs-lookup"><span data-stu-id="303a2-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="303a2-135">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="303a2-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="303a2-136">**15**</span><span class="sxs-lookup"><span data-stu-id="303a2-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="303a2-137">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="303a2-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="303a2-138">**16**</span><span class="sxs-lookup"><span data-stu-id="303a2-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="303a2-139">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="303a2-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="303a2-140">**17**</span><span class="sxs-lookup"><span data-stu-id="303a2-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="303a2-141">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="303a2-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="303a2-142">**21**</span><span class="sxs-lookup"><span data-stu-id="303a2-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="303a2-143">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="303a2-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="303a2-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="303a2-144">Remarks</span></span>

<span data-ttu-id="303a2-145">Il metodo **Decompress** in file di file [**CIM \_**](cim-datafile.md) viene implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="303a2-145">The **Uncompress** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="303a2-146">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="303a2-146">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="303a2-147">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="303a2-147">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="303a2-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="303a2-148">Requirements</span></span>



| <span data-ttu-id="303a2-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="303a2-149">Requirement</span></span> | <span data-ttu-id="303a2-150">Valore</span><span class="sxs-lookup"><span data-stu-id="303a2-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="303a2-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="303a2-151">Minimum supported client</span></span><br/> | <span data-ttu-id="303a2-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="303a2-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="303a2-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="303a2-153">Minimum supported server</span></span><br/> | <span data-ttu-id="303a2-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="303a2-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="303a2-155">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="303a2-155">Namespace</span></span><br/>                | <span data-ttu-id="303a2-156">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="303a2-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="303a2-157">MOF</span><span class="sxs-lookup"><span data-stu-id="303a2-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="303a2-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="303a2-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="303a2-159">DLL</span><span class="sxs-lookup"><span data-stu-id="303a2-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="303a2-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="303a2-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="303a2-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="303a2-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="303a2-162">**File di \_ DataFile CIM**</span><span class="sxs-lookup"><span data-stu-id="303a2-162">**CIM\_DataFile**</span></span>](uncompress-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="303a2-163">**File di \_ DataFile CIM**</span><span class="sxs-lookup"><span data-stu-id="303a2-163">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="303a2-164">Attività WMI: file e cartelle</span><span class="sxs-lookup"><span data-stu-id="303a2-164">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="303a2-165">**Costanti dei diritti di accesso a file e directory**</span><span class="sxs-lookup"><span data-stu-id="303a2-165">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

