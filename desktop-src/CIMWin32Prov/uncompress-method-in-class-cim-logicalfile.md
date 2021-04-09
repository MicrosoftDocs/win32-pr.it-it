---
description: Decomprime il file o la directory logica specificata nel percorso dell'oggetto.
ms.assetid: 0de01859-4a4b-4d70-802d-c52b2f56d7a1
ms.tgt_platform: multiple
title: Metodo Decompress della classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a2cde35ade1b1e8cbb3705a4c2f1b08f943139c5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966013"
---
# <a name="uncompress-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="9146d-103">Metodo Decompress della classe CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="9146d-103">Uncompress method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="9146d-104">Il metodo **uncompress** decomprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9146d-104">The **Uncompress** method uncompresses the logical file (or directory) specified in the object path.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9146d-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="9146d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9146d-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9146d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9146d-107">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="9146d-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9146d-108">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9146d-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9146d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9146d-109">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="9146d-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="9146d-110">Parameters</span></span>

<span data-ttu-id="9146d-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="9146d-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9146d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9146d-112">Return value</span></span>

<span data-ttu-id="9146d-113">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="9146d-113">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="9146d-114">**Success**</span><span class="sxs-lookup"><span data-stu-id="9146d-114">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="9146d-115">0</span><span class="sxs-lookup"><span data-stu-id="9146d-115">0</span></span>

<span data-ttu-id="9146d-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9146d-116">Success.</span></span>

</dd> <dt>

<span data-ttu-id="9146d-117">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="9146d-117">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="9146d-118">2</span><span class="sxs-lookup"><span data-stu-id="9146d-118">2</span></span>

<span data-ttu-id="9146d-119">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="9146d-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="9146d-120">**Errore non specificato**</span><span class="sxs-lookup"><span data-stu-id="9146d-120">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="9146d-121">8</span><span class="sxs-lookup"><span data-stu-id="9146d-121">8</span></span>

<span data-ttu-id="9146d-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="9146d-122">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="9146d-123">**Oggetto non valido**</span><span class="sxs-lookup"><span data-stu-id="9146d-123">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="9146d-124">9</span><span class="sxs-lookup"><span data-stu-id="9146d-124">9</span></span>

<span data-ttu-id="9146d-125">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="9146d-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="9146d-126">**Oggetto già esistente**</span><span class="sxs-lookup"><span data-stu-id="9146d-126">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="9146d-127">10</span><span class="sxs-lookup"><span data-stu-id="9146d-127">10</span></span>

<span data-ttu-id="9146d-128">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="9146d-128">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="9146d-129">**File System non NTFS**</span><span class="sxs-lookup"><span data-stu-id="9146d-129">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="9146d-130">11</span><span class="sxs-lookup"><span data-stu-id="9146d-130">11</span></span>

<span data-ttu-id="9146d-131">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="9146d-131">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="9146d-132">**Piattaforma non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="9146d-132">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="9146d-133">12</span><span class="sxs-lookup"><span data-stu-id="9146d-133">12</span></span>

<span data-ttu-id="9146d-134">Piattaforma non basata su Windows NT.</span><span class="sxs-lookup"><span data-stu-id="9146d-134">Platform not Windows NT-based.</span></span>

</dd> <dt>

<span data-ttu-id="9146d-135">**Unità non uguale**</span><span class="sxs-lookup"><span data-stu-id="9146d-135">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="9146d-136">13</span><span class="sxs-lookup"><span data-stu-id="9146d-136">13</span></span>

<span data-ttu-id="9146d-137">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="9146d-137">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="9146d-138">**Directory non vuota**</span><span class="sxs-lookup"><span data-stu-id="9146d-138">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="9146d-139">14</span><span class="sxs-lookup"><span data-stu-id="9146d-139">14</span></span>

<span data-ttu-id="9146d-140">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="9146d-140">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="9146d-141">**Violazione di condivisione**</span><span class="sxs-lookup"><span data-stu-id="9146d-141">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="9146d-142">15</span><span class="sxs-lookup"><span data-stu-id="9146d-142">15</span></span>

<span data-ttu-id="9146d-143">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="9146d-143">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="9146d-144">**File di avvio non valido**</span><span class="sxs-lookup"><span data-stu-id="9146d-144">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="9146d-145">16</span><span class="sxs-lookup"><span data-stu-id="9146d-145">16</span></span>

<span data-ttu-id="9146d-146">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="9146d-146">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="9146d-147">**Privilegio non mantenuto**</span><span class="sxs-lookup"><span data-stu-id="9146d-147">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="9146d-148">17</span><span class="sxs-lookup"><span data-stu-id="9146d-148">17</span></span>

<span data-ttu-id="9146d-149">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="9146d-149">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="9146d-150">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="9146d-150">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="9146d-151">21</span><span class="sxs-lookup"><span data-stu-id="9146d-151">21</span></span>

<span data-ttu-id="9146d-152">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="9146d-152">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9146d-153">Commenti</span><span class="sxs-lookup"><span data-stu-id="9146d-153">Remarks</span></span>

<span data-ttu-id="9146d-154">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="9146d-154">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="9146d-155">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="9146d-155">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="9146d-156">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="9146d-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9146d-157">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="9146d-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9146d-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9146d-158">Requirements</span></span>



| <span data-ttu-id="9146d-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="9146d-159">Requirement</span></span> | <span data-ttu-id="9146d-160">Valore</span><span class="sxs-lookup"><span data-stu-id="9146d-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9146d-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9146d-161">Minimum supported client</span></span><br/> | <span data-ttu-id="9146d-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9146d-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9146d-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9146d-163">Minimum supported server</span></span><br/> | <span data-ttu-id="9146d-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9146d-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9146d-165">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9146d-165">Namespace</span></span><br/>                | <span data-ttu-id="9146d-166">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="9146d-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9146d-167">MOF</span><span class="sxs-lookup"><span data-stu-id="9146d-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9146d-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9146d-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9146d-169">DLL</span><span class="sxs-lookup"><span data-stu-id="9146d-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9146d-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9146d-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9146d-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9146d-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9146d-172">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="9146d-172">CIM\_LogicalFile</span></span>](uncompress-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="9146d-173">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="9146d-173">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

