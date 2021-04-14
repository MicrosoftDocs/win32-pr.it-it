---
description: Il metodo DeleteEx Elimina il file o la directory logica specificata nel percorso dell'oggetto. Questo metodo è una versione estesa del metodo Delete.
ms.assetid: 53785f2e-8796-446c-8228-9abc2d9a0d68
ms.tgt_platform: multiple
title: Metodo DeleteEx della classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4f9799513111ff53bb97c14feaf70c922dfb085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523401"
---
# <a name="deleteex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="4b459-104">Metodo DeleteEx della classe CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="4b459-104">DeleteEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="4b459-105">Il metodo **DeleteEx** Elimina il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4b459-105">The **DeleteEx** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="4b459-106">Questo metodo è una versione estesa del metodo [**Delete**](delete-method-in-class-cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="4b459-106">This method is an extended version of the [**Delete**](delete-method-in-class-cim-logicalfile.md) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4b459-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="4b459-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4b459-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4b459-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4b459-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="4b459-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4b459-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4b459-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4b459-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b459-111">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out]          string StopFileName,
  [in, optional] string StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="4b459-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="4b459-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b459-113">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4b459-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b459-114">Stringa che rappresenta il nome del file o della directory in cui il metodo ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="4b459-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="4b459-115">Questo parametro è null se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4b459-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="4b459-116">*StartFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="4b459-116">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4b459-117">Stringa che assegna un nome al file figlio (o alla directory) da utilizzare come punto di partenza per il metodo.</span><span class="sxs-lookup"><span data-stu-id="4b459-117">String that names the child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="4b459-118">In genere, questo parametro è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="4b459-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="4b459-119">Se questo parametro è null, l'operazione viene eseguita sul file o sulla directory specificata nella chiamata [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="4b459-119">If this parameter is null, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b459-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4b459-120">Return value</span></span>

<span data-ttu-id="4b459-121">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="4b459-121">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="4b459-122">**Success**</span><span class="sxs-lookup"><span data-stu-id="4b459-122">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="4b459-123">0</span><span class="sxs-lookup"><span data-stu-id="4b459-123">0</span></span>

<span data-ttu-id="4b459-124">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4b459-124">Success.</span></span>

</dd> <dt>

<span data-ttu-id="4b459-125">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="4b459-125">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="4b459-126">2</span><span class="sxs-lookup"><span data-stu-id="4b459-126">2</span></span>

<span data-ttu-id="4b459-127">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="4b459-127">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="4b459-128">**Errore non specificato**</span><span class="sxs-lookup"><span data-stu-id="4b459-128">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="4b459-129">8</span><span class="sxs-lookup"><span data-stu-id="4b459-129">8</span></span>

<span data-ttu-id="4b459-130">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="4b459-130">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="4b459-131">**Oggetto non valido**</span><span class="sxs-lookup"><span data-stu-id="4b459-131">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="4b459-132">9</span><span class="sxs-lookup"><span data-stu-id="4b459-132">9</span></span>

<span data-ttu-id="4b459-133">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="4b459-133">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="4b459-134">**Oggetto già esistente**</span><span class="sxs-lookup"><span data-stu-id="4b459-134">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="4b459-135">10</span><span class="sxs-lookup"><span data-stu-id="4b459-135">10</span></span>

<span data-ttu-id="4b459-136">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="4b459-136">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="4b459-137">**File System non NTFS**</span><span class="sxs-lookup"><span data-stu-id="4b459-137">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="4b459-138">11</span><span class="sxs-lookup"><span data-stu-id="4b459-138">11</span></span>

<span data-ttu-id="4b459-139">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="4b459-139">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="4b459-140">**Piattaforma non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="4b459-140">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="4b459-141">12</span><span class="sxs-lookup"><span data-stu-id="4b459-141">12</span></span>

<span data-ttu-id="4b459-142">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="4b459-142">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="4b459-143">**Unità non uguale**</span><span class="sxs-lookup"><span data-stu-id="4b459-143">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="4b459-144">13</span><span class="sxs-lookup"><span data-stu-id="4b459-144">13</span></span>

<span data-ttu-id="4b459-145">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="4b459-145">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="4b459-146">**Directory non vuota**</span><span class="sxs-lookup"><span data-stu-id="4b459-146">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="4b459-147">14</span><span class="sxs-lookup"><span data-stu-id="4b459-147">14</span></span>

<span data-ttu-id="4b459-148">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="4b459-148">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="4b459-149">**Violazione di condivisione**</span><span class="sxs-lookup"><span data-stu-id="4b459-149">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="4b459-150">15</span><span class="sxs-lookup"><span data-stu-id="4b459-150">15</span></span>

<span data-ttu-id="4b459-151">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="4b459-151">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="4b459-152">**File di avvio non valido**</span><span class="sxs-lookup"><span data-stu-id="4b459-152">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="4b459-153">16</span><span class="sxs-lookup"><span data-stu-id="4b459-153">16</span></span>

<span data-ttu-id="4b459-154">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="4b459-154">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="4b459-155">**Privilegio non mantenuto**</span><span class="sxs-lookup"><span data-stu-id="4b459-155">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="4b459-156">17</span><span class="sxs-lookup"><span data-stu-id="4b459-156">17</span></span>

<span data-ttu-id="4b459-157">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="4b459-157">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="4b459-158">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="4b459-158">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="4b459-159">21</span><span class="sxs-lookup"><span data-stu-id="4b459-159">21</span></span>

<span data-ttu-id="4b459-160">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="4b459-160">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b459-161">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b459-161">Remarks</span></span>

<span data-ttu-id="4b459-162">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="4b459-162">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="4b459-163">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="4b459-163">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="4b459-164">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="4b459-164">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4b459-165">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="4b459-165">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b459-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b459-166">Requirements</span></span>



| <span data-ttu-id="4b459-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b459-167">Requirement</span></span> | <span data-ttu-id="4b459-168">Valore</span><span class="sxs-lookup"><span data-stu-id="4b459-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b459-169">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b459-169">Minimum supported client</span></span><br/> | <span data-ttu-id="4b459-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b459-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4b459-171">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b459-171">Minimum supported server</span></span><br/> | <span data-ttu-id="4b459-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b459-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4b459-173">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4b459-173">Namespace</span></span><br/>                | <span data-ttu-id="4b459-174">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="4b459-174">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4b459-175">MOF</span><span class="sxs-lookup"><span data-stu-id="4b459-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b459-176"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b459-176"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b459-177">DLL</span><span class="sxs-lookup"><span data-stu-id="4b459-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b459-178"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b459-178"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b459-179">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b459-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b459-180">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="4b459-180">CIM\_LogicalFile</span></span>](deleteex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="4b459-181">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="4b459-181">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

