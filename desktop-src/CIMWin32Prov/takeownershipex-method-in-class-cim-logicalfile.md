---
description: Ottiene la proprietà del file logico specificato nel percorso dell'oggetto. Questo metodo è una versione estesa del metodo TakeOwnerShip.
ms.assetid: c01ab071-86e4-484d-aaed-4783b6c3bebf
ms.tgt_platform: multiple
title: Metodo TakeOwnerShipEx della classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2e7f08413440ec32037554476ced386c56827239
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304479"
---
# <a name="takeownershipex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="2dd55-104">Metodo TakeOwnerShipEx della classe CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="2dd55-104">TakeOwnerShipEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="2dd55-105">Il metodo **TakeOwnerShipEx** ottiene la proprietà del file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2dd55-105">The **TakeOwnerShipEx** method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="2dd55-106">Questo metodo è una versione estesa del metodo [**TakeOwnership**](takeownership-method-in-class-cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="2dd55-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-cim-logicalfile.md) method.</span></span> <span data-ttu-id="2dd55-107">Se il file logico è una directory, questo metodo agisce in modo ricorsivo, assumendo la proprietà di tutti i file e le sottodirectory contenuti nella directory.</span><span class="sxs-lookup"><span data-stu-id="2dd55-107">If the logical file is a directory, then this method acts recursively, taking ownership of all files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2dd55-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="2dd55-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2dd55-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2dd55-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2dd55-110">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="2dd55-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2dd55-111">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2dd55-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2dd55-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2dd55-112">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="2dd55-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="2dd55-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dd55-114">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2dd55-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2dd55-115">Stringa che rappresenta il nome del file o della directory in cui il metodo ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="2dd55-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="2dd55-116">Questo parametro è **null** se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="2dd55-116">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="2dd55-117">*StartFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2dd55-117">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2dd55-118">Stringa che assegna un nome al file figlio (o alla directory) da utilizzare come punto di partenza per il metodo.</span><span class="sxs-lookup"><span data-stu-id="2dd55-118">String that names the child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="2dd55-119">In genere, questo parametro è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="2dd55-119">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="2dd55-120">Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificati nella chiamata [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="2dd55-120">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="2dd55-121">*Ricorsivo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2dd55-121">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2dd55-122">Se è **true**, anche il metodo viene applicato in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="2dd55-122">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="2dd55-123">Per le istanze di file, questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="2dd55-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dd55-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2dd55-124">Return value</span></span>

<span data-ttu-id="2dd55-125">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="2dd55-125">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="2dd55-126">**Success**</span><span class="sxs-lookup"><span data-stu-id="2dd55-126">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="2dd55-127">0</span><span class="sxs-lookup"><span data-stu-id="2dd55-127">0</span></span>

<span data-ttu-id="2dd55-128">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="2dd55-128">Success.</span></span>

</dd> <dt>

<span data-ttu-id="2dd55-129">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="2dd55-129">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="2dd55-130">2</span><span class="sxs-lookup"><span data-stu-id="2dd55-130">2</span></span>

<span data-ttu-id="2dd55-131">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="2dd55-131">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="2dd55-132">**Errore non specificato**</span><span class="sxs-lookup"><span data-stu-id="2dd55-132">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="2dd55-133">8</span><span class="sxs-lookup"><span data-stu-id="2dd55-133">8</span></span>

<span data-ttu-id="2dd55-134">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="2dd55-134">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="2dd55-135">**Oggetto non valido**</span><span class="sxs-lookup"><span data-stu-id="2dd55-135">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="2dd55-136">9</span><span class="sxs-lookup"><span data-stu-id="2dd55-136">9</span></span>

<span data-ttu-id="2dd55-137">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="2dd55-137">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="2dd55-138">**Oggetto già esistente**</span><span class="sxs-lookup"><span data-stu-id="2dd55-138">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="2dd55-139">10</span><span class="sxs-lookup"><span data-stu-id="2dd55-139">10</span></span>

<span data-ttu-id="2dd55-140">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="2dd55-140">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2dd55-141">**File System non NTFS**</span><span class="sxs-lookup"><span data-stu-id="2dd55-141">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="2dd55-142">11</span><span class="sxs-lookup"><span data-stu-id="2dd55-142">11</span></span>

<span data-ttu-id="2dd55-143">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="2dd55-143">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="2dd55-144">**Piattaforma non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="2dd55-144">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="2dd55-145">12</span><span class="sxs-lookup"><span data-stu-id="2dd55-145">12</span></span>

<span data-ttu-id="2dd55-146">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="2dd55-146">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="2dd55-147">**Unità non uguale**</span><span class="sxs-lookup"><span data-stu-id="2dd55-147">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="2dd55-148">13</span><span class="sxs-lookup"><span data-stu-id="2dd55-148">13</span></span>

<span data-ttu-id="2dd55-149">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="2dd55-149">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="2dd55-150">**Directory non vuota**</span><span class="sxs-lookup"><span data-stu-id="2dd55-150">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="2dd55-151">14</span><span class="sxs-lookup"><span data-stu-id="2dd55-151">14</span></span>

<span data-ttu-id="2dd55-152">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="2dd55-152">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="2dd55-153">**Violazione di condivisione**</span><span class="sxs-lookup"><span data-stu-id="2dd55-153">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="2dd55-154">15</span><span class="sxs-lookup"><span data-stu-id="2dd55-154">15</span></span>

<span data-ttu-id="2dd55-155">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="2dd55-155">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="2dd55-156">**File di avvio non valido**</span><span class="sxs-lookup"><span data-stu-id="2dd55-156">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="2dd55-157">16</span><span class="sxs-lookup"><span data-stu-id="2dd55-157">16</span></span>

<span data-ttu-id="2dd55-158">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="2dd55-158">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="2dd55-159">**Privilegio non mantenuto**</span><span class="sxs-lookup"><span data-stu-id="2dd55-159">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="2dd55-160">17</span><span class="sxs-lookup"><span data-stu-id="2dd55-160">17</span></span>

<span data-ttu-id="2dd55-161">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="2dd55-161">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="2dd55-162">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="2dd55-162">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="2dd55-163">21</span><span class="sxs-lookup"><span data-stu-id="2dd55-163">21</span></span>

<span data-ttu-id="2dd55-164">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="2dd55-164">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2dd55-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="2dd55-165">Remarks</span></span>

<span data-ttu-id="2dd55-166">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="2dd55-166">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="2dd55-167">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="2dd55-167">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="2dd55-168">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="2dd55-168">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2dd55-169">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="2dd55-169">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dd55-170">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2dd55-170">Requirements</span></span>



| <span data-ttu-id="2dd55-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dd55-171">Requirement</span></span> | <span data-ttu-id="2dd55-172">Valore</span><span class="sxs-lookup"><span data-stu-id="2dd55-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2dd55-173">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2dd55-173">Minimum supported client</span></span><br/> | <span data-ttu-id="2dd55-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2dd55-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2dd55-175">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2dd55-175">Minimum supported server</span></span><br/> | <span data-ttu-id="2dd55-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2dd55-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2dd55-177">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2dd55-177">Namespace</span></span><br/>                | <span data-ttu-id="2dd55-178">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="2dd55-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2dd55-179">MOF</span><span class="sxs-lookup"><span data-stu-id="2dd55-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2dd55-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2dd55-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2dd55-181">DLL</span><span class="sxs-lookup"><span data-stu-id="2dd55-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2dd55-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2dd55-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dd55-183">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2dd55-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dd55-184">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="2dd55-184">CIM\_LogicalFile</span></span>](takeownershipex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="2dd55-185">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="2dd55-185">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

