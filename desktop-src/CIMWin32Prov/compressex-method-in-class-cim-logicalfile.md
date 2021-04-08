---
description: Il metodo CompressEx comprime il file o la directory logica specificata nel percorso dell'oggetto. Questo metodo è una versione estesa del metodo Compress.
ms.assetid: 7d119865-c246-4cb5-9de4-48a4c42efd90
ms.tgt_platform: multiple
title: Metodo CompressEx della classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7570cbe3ebc00708023a18da42ef35ff3306d3b0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877361"
---
# <a name="compressex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="0f0e9-104">Metodo CompressEx della classe CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="0f0e9-104">CompressEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="0f0e9-105">Il metodo **CompressEx** comprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-105">The **CompressEx** method compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="0f0e9-106">Questo metodo è una versione estesa del metodo [**Compress**](compress-method-in-class-cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="0f0e9-106">This method is an extended version of the [**Compress**](compress-method-in-class-cim-logicalfile.md) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0f0e9-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0f0e9-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0f0e9-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0f0e9-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="0f0e9-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0f0e9-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0f0e9-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0f0e9-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f0e9-111">Syntax</span></span>


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="0f0e9-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f0e9-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f0e9-113">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0f0e9-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f0e9-114">Nome del file o della directory in cui il metodo ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-114">Name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="0f0e9-115">Questo parametro è null se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="0f0e9-116">*StartFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="0f0e9-116">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0f0e9-117">File figlio (o directory) da utilizzare come punto di partenza per il metodo.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-117">Child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="0f0e9-118">In genere, questo parametro è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="0f0e9-119">Se questo parametro è null, l'operazione viene eseguita sul file o sulla directory specificati nella chiamata [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="0f0e9-119">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="0f0e9-120">*Ricorsivo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="0f0e9-120">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0f0e9-121">Se è **true**, anche il metodo viene applicato in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="0f0e9-121">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="0f0e9-122">Per le istanze di file, questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-122">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f0e9-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f0e9-123">Return value</span></span>

<span data-ttu-id="0f0e9-124">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-124">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="0f0e9-125">**Success**</span><span class="sxs-lookup"><span data-stu-id="0f0e9-125">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="0f0e9-126">0</span><span class="sxs-lookup"><span data-stu-id="0f0e9-126">0</span></span>

<span data-ttu-id="0f0e9-127">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-127">Success.</span></span>

</dd> <dt>

<span data-ttu-id="0f0e9-128">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="0f0e9-128">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="0f0e9-129">2</span><span class="sxs-lookup"><span data-stu-id="0f0e9-129">2</span></span>

<span data-ttu-id="0f0e9-130">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-130">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="0f0e9-131">**Errore non specificato**</span><span class="sxs-lookup"><span data-stu-id="0f0e9-131">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="0f0e9-132">8</span><span class="sxs-lookup"><span data-stu-id="0f0e9-132">8</span></span>

<span data-ttu-id="0f0e9-133">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-133">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="0f0e9-134">**Oggetto non valido**</span><span class="sxs-lookup"><span data-stu-id="0f0e9-134">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="0f0e9-135">9</span><span class="sxs-lookup"><span data-stu-id="0f0e9-135">9</span></span>

<span data-ttu-id="0f0e9-136">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-136">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="0f0e9-137">**Oggetto già esistente**</span><span class="sxs-lookup"><span data-stu-id="0f0e9-137">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="0f0e9-138">10</span><span class="sxs-lookup"><span data-stu-id="0f0e9-138">10</span></span>

<span data-ttu-id="0f0e9-139">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-139">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="0f0e9-140">**File System non NTFS**</span><span class="sxs-lookup"><span data-stu-id="0f0e9-140">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="0f0e9-141">11</span><span class="sxs-lookup"><span data-stu-id="0f0e9-141">11</span></span>

<span data-ttu-id="0f0e9-142">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-142">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="0f0e9-143">**Piattaforma non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="0f0e9-143">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="0f0e9-144">12</span><span class="sxs-lookup"><span data-stu-id="0f0e9-144">12</span></span>

<span data-ttu-id="0f0e9-145">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-145">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="0f0e9-146">**Unità non uguale**</span><span class="sxs-lookup"><span data-stu-id="0f0e9-146">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="0f0e9-147">13</span><span class="sxs-lookup"><span data-stu-id="0f0e9-147">13</span></span>

<span data-ttu-id="0f0e9-148">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-148">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="0f0e9-149">**Directory non vuota**</span><span class="sxs-lookup"><span data-stu-id="0f0e9-149">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="0f0e9-150">14</span><span class="sxs-lookup"><span data-stu-id="0f0e9-150">14</span></span>

<span data-ttu-id="0f0e9-151">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-151">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="0f0e9-152">**Violazione di condivisione**</span><span class="sxs-lookup"><span data-stu-id="0f0e9-152">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="0f0e9-153">15</span><span class="sxs-lookup"><span data-stu-id="0f0e9-153">15</span></span>

<span data-ttu-id="0f0e9-154">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-154">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="0f0e9-155">**File di avvio non valido**</span><span class="sxs-lookup"><span data-stu-id="0f0e9-155">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="0f0e9-156">16</span><span class="sxs-lookup"><span data-stu-id="0f0e9-156">16</span></span>

<span data-ttu-id="0f0e9-157">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-157">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="0f0e9-158">**Privilegio non mantenuto**</span><span class="sxs-lookup"><span data-stu-id="0f0e9-158">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="0f0e9-159">17</span><span class="sxs-lookup"><span data-stu-id="0f0e9-159">17</span></span>

<span data-ttu-id="0f0e9-160">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-160">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="0f0e9-161">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="0f0e9-161">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="0f0e9-162">21</span><span class="sxs-lookup"><span data-stu-id="0f0e9-162">21</span></span>

<span data-ttu-id="0f0e9-163">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-163">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f0e9-164">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f0e9-164">Remarks</span></span>

<span data-ttu-id="0f0e9-165">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-165">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="0f0e9-166">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="0f0e9-166">To use this method, you must implement it in your own provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f0e9-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f0e9-167">Requirements</span></span>



| <span data-ttu-id="0f0e9-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f0e9-168">Requirement</span></span> | <span data-ttu-id="0f0e9-169">Valore</span><span class="sxs-lookup"><span data-stu-id="0f0e9-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f0e9-170">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f0e9-170">Minimum supported client</span></span><br/> | <span data-ttu-id="0f0e9-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f0e9-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0f0e9-172">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f0e9-172">Minimum supported server</span></span><br/> | <span data-ttu-id="0f0e9-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f0e9-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0f0e9-174">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0f0e9-174">Namespace</span></span><br/>                | <span data-ttu-id="0f0e9-175">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="0f0e9-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0f0e9-176">MOF</span><span class="sxs-lookup"><span data-stu-id="0f0e9-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f0e9-177"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f0e9-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f0e9-178">DLL</span><span class="sxs-lookup"><span data-stu-id="0f0e9-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f0e9-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f0e9-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f0e9-180">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f0e9-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f0e9-181">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="0f0e9-181">CIM\_LogicalFile</span></span>](compressex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="0f0e9-182">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="0f0e9-182">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

