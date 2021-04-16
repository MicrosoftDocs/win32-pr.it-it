---
description: Decomprime il file o la directory del dispositivo logico specificato nel percorso dell'oggetto. Questo metodo è una versione estesa del metodo Decompress. Questo metodo viene ereditato da \_ LOGICALFILE CIM.
ms.assetid: dfa53b75-56ef-4119-83b9-08b4371762c6
ms.tgt_platform: multiple
title: Metodo UncompressEx della classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a760c31a2067c294ffb43064402ac179c5fba7c9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524129"
---
# <a name="uncompressex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="19e4f-105">Metodo UncompressEx della classe CIM \_ DeviceFile</span><span class="sxs-lookup"><span data-stu-id="19e4f-105">UncompressEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="19e4f-106">Il metodo **UncompressEx** decomprime il file (o la directory) del dispositivo logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="19e4f-106">The **UncompressEx** method uncompresses the logical device file (or directory) specified in the object path.</span></span> <span data-ttu-id="19e4f-107">Questo metodo è una versione estesa del metodo [**Decompress**](uncompress-method-in-class-cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="19e4f-107">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-cim-devicefile.md) method.</span></span> <span data-ttu-id="19e4f-108">Questo metodo viene ereditato da [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="19e4f-108">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="19e4f-109">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="19e4f-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="19e4f-110">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="19e4f-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="19e4f-111">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="19e4f-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="19e4f-112">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="19e4f-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="19e4f-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19e4f-113">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="19e4f-114">Parametri</span><span class="sxs-lookup"><span data-stu-id="19e4f-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19e4f-115">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="19e4f-115">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19e4f-116">Stringa che rappresenta il nome del file o della directory in cui il metodo ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="19e4f-116">String that represent the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="19e4f-117">Questo parametro è **null** se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="19e4f-117">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="19e4f-118">*StartFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19e4f-118">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19e4f-119">Stringa che rappresenta il file o la directory figlio da utilizzare come punto di partenza per il metodo.</span><span class="sxs-lookup"><span data-stu-id="19e4f-119">String that represents the child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="19e4f-120">In genere, il parametro *StartFileName* è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="19e4f-120">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="19e4f-121">Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificata nella chiamata [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="19e4f-121">If this parameter is **NULL**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="19e4f-122">*Ricorsivo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19e4f-122">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19e4f-123">Se **true**, questo metodo viene anche applicato in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza di [**CIM \_ DeviceFile**](cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="19e4f-123">If **TRUE**, this method is also applied recursively to files and directories within the directory specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="19e4f-124">Per le istanze di file, questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="19e4f-124">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19e4f-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="19e4f-125">Return value</span></span>

<span data-ttu-id="19e4f-126">Restituisce un valore pari a 0 in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="19e4f-126">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="19e4f-127">0</span><span class="sxs-lookup"><span data-stu-id="19e4f-127">0</span></span>

<span data-ttu-id="19e4f-128">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="19e4f-128">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="19e4f-129">2</span><span class="sxs-lookup"><span data-stu-id="19e4f-129">2</span></span>

<span data-ttu-id="19e4f-130">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="19e4f-130">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="19e4f-131">8</span><span class="sxs-lookup"><span data-stu-id="19e4f-131">8</span></span>

<span data-ttu-id="19e4f-132">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="19e4f-132">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="19e4f-133">9</span><span class="sxs-lookup"><span data-stu-id="19e4f-133">9</span></span>

<span data-ttu-id="19e4f-134">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="19e4f-134">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="19e4f-135">10</span><span class="sxs-lookup"><span data-stu-id="19e4f-135">10</span></span>

<span data-ttu-id="19e4f-136">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="19e4f-136">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="19e4f-137">11</span><span class="sxs-lookup"><span data-stu-id="19e4f-137">11</span></span>

<span data-ttu-id="19e4f-138">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="19e4f-138">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="19e4f-139">12</span><span class="sxs-lookup"><span data-stu-id="19e4f-139">12</span></span>

<span data-ttu-id="19e4f-140">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="19e4f-140">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="19e4f-141">13</span><span class="sxs-lookup"><span data-stu-id="19e4f-141">13</span></span>

<span data-ttu-id="19e4f-142">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="19e4f-142">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="19e4f-143">14</span><span class="sxs-lookup"><span data-stu-id="19e4f-143">14</span></span>

<span data-ttu-id="19e4f-144">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="19e4f-144">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="19e4f-145">15</span><span class="sxs-lookup"><span data-stu-id="19e4f-145">15</span></span>

<span data-ttu-id="19e4f-146">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="19e4f-146">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="19e4f-147">16</span><span class="sxs-lookup"><span data-stu-id="19e4f-147">16</span></span>

<span data-ttu-id="19e4f-148">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="19e4f-148">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="19e4f-149">17</span><span class="sxs-lookup"><span data-stu-id="19e4f-149">17</span></span>

<span data-ttu-id="19e4f-150">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="19e4f-150">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="19e4f-151">21</span><span class="sxs-lookup"><span data-stu-id="19e4f-151">21</span></span>

<span data-ttu-id="19e4f-152">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="19e4f-152">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19e4f-153">Commenti</span><span class="sxs-lookup"><span data-stu-id="19e4f-153">Remarks</span></span>

<span data-ttu-id="19e4f-154">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="19e4f-154">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="19e4f-155">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="19e4f-155">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="19e4f-156">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="19e4f-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="19e4f-157">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="19e4f-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="19e4f-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19e4f-158">Requirements</span></span>



| <span data-ttu-id="19e4f-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="19e4f-159">Requirement</span></span> | <span data-ttu-id="19e4f-160">Valore</span><span class="sxs-lookup"><span data-stu-id="19e4f-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19e4f-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19e4f-161">Minimum supported client</span></span><br/> | <span data-ttu-id="19e4f-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19e4f-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="19e4f-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19e4f-163">Minimum supported server</span></span><br/> | <span data-ttu-id="19e4f-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19e4f-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="19e4f-165">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="19e4f-165">Namespace</span></span><br/>                | <span data-ttu-id="19e4f-166">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="19e4f-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="19e4f-167">MOF</span><span class="sxs-lookup"><span data-stu-id="19e4f-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19e4f-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19e4f-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="19e4f-169">DLL</span><span class="sxs-lookup"><span data-stu-id="19e4f-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19e4f-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19e4f-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19e4f-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19e4f-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19e4f-172">\_DEVICEFILE CIM</span><span class="sxs-lookup"><span data-stu-id="19e4f-172">CIM\_DeviceFile</span></span>](uncompressex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="19e4f-173">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="19e4f-173">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

