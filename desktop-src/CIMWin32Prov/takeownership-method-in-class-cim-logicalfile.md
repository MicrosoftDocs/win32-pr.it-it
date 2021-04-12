---
description: Il metodo TakeOwnerShip ottiene la proprietà del file logico specificato nel percorso dell'oggetto. Se il file logico è una directory, questo metodo agisce in modo ricorsivo, assumendo la proprietà di tutti i file e le sottodirectory contenuti nella directory.
ms.assetid: 5db62da0-ac93-4a8c-af17-306e02bfa756
ms.tgt_platform: multiple
title: Metodo TakeOwnerShip della classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7cdd9515a5e947a3e707464dcbd524c875f7785f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523017"
---
# <a name="takeownership-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="4aa1e-104">Metodo TakeOwnerShip della classe CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="4aa1e-104">TakeOwnerShip method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="4aa1e-105">Il metodo **TakeOwnership** ottiene la proprietà del file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4aa1e-105">The **TakeOwnerShip** method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="4aa1e-106">Se il file logico è una directory, questo metodo agisce in modo ricorsivo, assumendo la proprietà di tutti i file e le sottodirectory contenuti nella directory.</span><span class="sxs-lookup"><span data-stu-id="4aa1e-106">If the logical file is a directory, then this method acts recursively, taking ownership of all files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4aa1e-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="4aa1e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4aa1e-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4aa1e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4aa1e-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="4aa1e-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4aa1e-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4aa1e-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4aa1e-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4aa1e-111">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="4aa1e-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="4aa1e-112">Parameters</span></span>

<span data-ttu-id="4aa1e-113">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="4aa1e-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4aa1e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4aa1e-114">Return value</span></span>

<span data-ttu-id="4aa1e-115">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="4aa1e-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="4aa1e-116">**Success**</span><span class="sxs-lookup"><span data-stu-id="4aa1e-116">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="4aa1e-117">0</span><span class="sxs-lookup"><span data-stu-id="4aa1e-117">0</span></span>

<span data-ttu-id="4aa1e-118">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4aa1e-118">Success.</span></span>

</dd> <dt>

<span data-ttu-id="4aa1e-119">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="4aa1e-119">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="4aa1e-120">2</span><span class="sxs-lookup"><span data-stu-id="4aa1e-120">2</span></span>

<span data-ttu-id="4aa1e-121">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="4aa1e-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="4aa1e-122">**Errore non specificato**</span><span class="sxs-lookup"><span data-stu-id="4aa1e-122">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="4aa1e-123">8</span><span class="sxs-lookup"><span data-stu-id="4aa1e-123">8</span></span>

<span data-ttu-id="4aa1e-124">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="4aa1e-124">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="4aa1e-125">**Oggetto non valido**</span><span class="sxs-lookup"><span data-stu-id="4aa1e-125">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="4aa1e-126">9</span><span class="sxs-lookup"><span data-stu-id="4aa1e-126">9</span></span>

<span data-ttu-id="4aa1e-127">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="4aa1e-127">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="4aa1e-128">**Oggetto già esistente**</span><span class="sxs-lookup"><span data-stu-id="4aa1e-128">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="4aa1e-129">10</span><span class="sxs-lookup"><span data-stu-id="4aa1e-129">10</span></span>

<span data-ttu-id="4aa1e-130">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="4aa1e-130">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="4aa1e-131">**File System non NTFS**</span><span class="sxs-lookup"><span data-stu-id="4aa1e-131">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="4aa1e-132">11</span><span class="sxs-lookup"><span data-stu-id="4aa1e-132">11</span></span>

<span data-ttu-id="4aa1e-133">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="4aa1e-133">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="4aa1e-134">**Piattaforma non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="4aa1e-134">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="4aa1e-135">12</span><span class="sxs-lookup"><span data-stu-id="4aa1e-135">12</span></span>

<span data-ttu-id="4aa1e-136">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="4aa1e-136">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="4aa1e-137">**Unità non uguale**</span><span class="sxs-lookup"><span data-stu-id="4aa1e-137">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="4aa1e-138">13</span><span class="sxs-lookup"><span data-stu-id="4aa1e-138">13</span></span>

<span data-ttu-id="4aa1e-139">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="4aa1e-139">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="4aa1e-140">**Directory non vuota**</span><span class="sxs-lookup"><span data-stu-id="4aa1e-140">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="4aa1e-141">14</span><span class="sxs-lookup"><span data-stu-id="4aa1e-141">14</span></span>

<span data-ttu-id="4aa1e-142">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="4aa1e-142">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="4aa1e-143">**Violazione di condivisione**</span><span class="sxs-lookup"><span data-stu-id="4aa1e-143">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="4aa1e-144">15</span><span class="sxs-lookup"><span data-stu-id="4aa1e-144">15</span></span>

<span data-ttu-id="4aa1e-145">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="4aa1e-145">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="4aa1e-146">**File di avvio non valido**</span><span class="sxs-lookup"><span data-stu-id="4aa1e-146">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="4aa1e-147">16</span><span class="sxs-lookup"><span data-stu-id="4aa1e-147">16</span></span>

<span data-ttu-id="4aa1e-148">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="4aa1e-148">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="4aa1e-149">**Privilegio non mantenuto**</span><span class="sxs-lookup"><span data-stu-id="4aa1e-149">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="4aa1e-150">17</span><span class="sxs-lookup"><span data-stu-id="4aa1e-150">17</span></span>

<span data-ttu-id="4aa1e-151">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="4aa1e-151">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="4aa1e-152">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="4aa1e-152">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="4aa1e-153">21</span><span class="sxs-lookup"><span data-stu-id="4aa1e-153">21</span></span>

<span data-ttu-id="4aa1e-154">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="4aa1e-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4aa1e-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="4aa1e-155">Remarks</span></span>

<span data-ttu-id="4aa1e-156">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="4aa1e-156">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="4aa1e-157">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="4aa1e-157">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="4aa1e-158">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="4aa1e-158">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4aa1e-159">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="4aa1e-159">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4aa1e-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4aa1e-160">Requirements</span></span>



| <span data-ttu-id="4aa1e-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="4aa1e-161">Requirement</span></span> | <span data-ttu-id="4aa1e-162">Valore</span><span class="sxs-lookup"><span data-stu-id="4aa1e-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4aa1e-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4aa1e-163">Minimum supported client</span></span><br/> | <span data-ttu-id="4aa1e-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4aa1e-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4aa1e-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4aa1e-165">Minimum supported server</span></span><br/> | <span data-ttu-id="4aa1e-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4aa1e-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4aa1e-167">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4aa1e-167">Namespace</span></span><br/>                | <span data-ttu-id="4aa1e-168">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="4aa1e-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4aa1e-169">MOF</span><span class="sxs-lookup"><span data-stu-id="4aa1e-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4aa1e-170"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4aa1e-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4aa1e-171">DLL</span><span class="sxs-lookup"><span data-stu-id="4aa1e-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4aa1e-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4aa1e-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aa1e-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4aa1e-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aa1e-174">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="4aa1e-174">CIM\_LogicalFile</span></span>](takeownership-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="4aa1e-175">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="4aa1e-175">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

