---
description: Il metodo Rename Rinomina il file o la directory logica specificata nel percorso dell'oggetto. La ridenominazione non è supportata se la destinazione si trova in un'altra unità o se è necessario sovrascrivere un file logico esistente.
ms.assetid: 5a62ff64-d1d2-43a2-997c-0ad46896b31f
ms.tgt_platform: multiple
title: Rinominare il metodo della classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0da38020d7b22dceb6f1d061f8feaf858eeb5f04
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127366"
---
# <a name="rename-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="abfab-104">Rinominare il metodo della \_ classe CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="abfab-104">Rename method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="abfab-105">Il metodo **Rename Rinomina** il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="abfab-105">The **Rename** method renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="abfab-106">La ridenominazione non è supportata se la destinazione si trova in un'altra unità o se è necessario sovrascrivere un file logico esistente.</span><span class="sxs-lookup"><span data-stu-id="abfab-106">Renaming is not supported if the destination is on another drive, or overwriting an existing logical file is required.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="abfab-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="abfab-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="abfab-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="abfab-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="abfab-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="abfab-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="abfab-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="abfab-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="abfab-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="abfab-111">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="abfab-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="abfab-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abfab-113">*Nome file* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="abfab-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abfab-114">Nome completo del nuovo file (o directory).</span><span class="sxs-lookup"><span data-stu-id="abfab-114">Fully qualified new file (or directory) name.</span></span>

<span data-ttu-id="abfab-115">Esempio: "c: \\ temp \\newfile.txt"</span><span class="sxs-lookup"><span data-stu-id="abfab-115">Example: "c:\\temp\\newfile.txt"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abfab-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="abfab-116">Return value</span></span>

<span data-ttu-id="abfab-117">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="abfab-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="abfab-118">**Success**</span><span class="sxs-lookup"><span data-stu-id="abfab-118">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="abfab-119">0</span><span class="sxs-lookup"><span data-stu-id="abfab-119">0</span></span>

<span data-ttu-id="abfab-120">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="abfab-120">Success.</span></span>

</dd> <dt>

<span data-ttu-id="abfab-121">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="abfab-121">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="abfab-122">2</span><span class="sxs-lookup"><span data-stu-id="abfab-122">2</span></span>

<span data-ttu-id="abfab-123">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="abfab-123">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="abfab-124">**Errore non specificato**</span><span class="sxs-lookup"><span data-stu-id="abfab-124">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="abfab-125">8</span><span class="sxs-lookup"><span data-stu-id="abfab-125">8</span></span>

<span data-ttu-id="abfab-126">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="abfab-126">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="abfab-127">**Oggetto non valido**</span><span class="sxs-lookup"><span data-stu-id="abfab-127">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="abfab-128">9</span><span class="sxs-lookup"><span data-stu-id="abfab-128">9</span></span>

<span data-ttu-id="abfab-129">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="abfab-129">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="abfab-130">**Oggetto già esistente**</span><span class="sxs-lookup"><span data-stu-id="abfab-130">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="abfab-131">10</span><span class="sxs-lookup"><span data-stu-id="abfab-131">10</span></span>

<span data-ttu-id="abfab-132">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="abfab-132">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="abfab-133">**File System non NTFS**</span><span class="sxs-lookup"><span data-stu-id="abfab-133">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="abfab-134">11</span><span class="sxs-lookup"><span data-stu-id="abfab-134">11</span></span>

<span data-ttu-id="abfab-135">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="abfab-135">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="abfab-136">**Piattaforma non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="abfab-136">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="abfab-137">12</span><span class="sxs-lookup"><span data-stu-id="abfab-137">12</span></span>

<span data-ttu-id="abfab-138">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="abfab-138">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="abfab-139">**Unità non uguale**</span><span class="sxs-lookup"><span data-stu-id="abfab-139">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="abfab-140">13</span><span class="sxs-lookup"><span data-stu-id="abfab-140">13</span></span>

<span data-ttu-id="abfab-141">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="abfab-141">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="abfab-142">**Directory non vuota**</span><span class="sxs-lookup"><span data-stu-id="abfab-142">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="abfab-143">14</span><span class="sxs-lookup"><span data-stu-id="abfab-143">14</span></span>

<span data-ttu-id="abfab-144">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="abfab-144">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="abfab-145">**Violazione di condivisione**</span><span class="sxs-lookup"><span data-stu-id="abfab-145">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="abfab-146">15</span><span class="sxs-lookup"><span data-stu-id="abfab-146">15</span></span>

<span data-ttu-id="abfab-147">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="abfab-147">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="abfab-148">**File di avvio non valido**</span><span class="sxs-lookup"><span data-stu-id="abfab-148">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="abfab-149">16</span><span class="sxs-lookup"><span data-stu-id="abfab-149">16</span></span>

<span data-ttu-id="abfab-150">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="abfab-150">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="abfab-151">**Privilegio non mantenuto**</span><span class="sxs-lookup"><span data-stu-id="abfab-151">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="abfab-152">17</span><span class="sxs-lookup"><span data-stu-id="abfab-152">17</span></span>

<span data-ttu-id="abfab-153">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="abfab-153">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="abfab-154">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="abfab-154">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="abfab-155">21</span><span class="sxs-lookup"><span data-stu-id="abfab-155">21</span></span>

<span data-ttu-id="abfab-156">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="abfab-156">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="abfab-157">Commenti</span><span class="sxs-lookup"><span data-stu-id="abfab-157">Remarks</span></span>

<span data-ttu-id="abfab-158">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="abfab-158">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="abfab-159">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="abfab-159">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="abfab-160">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="abfab-160">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="abfab-161">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="abfab-161">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="abfab-162">Requisiti</span><span class="sxs-lookup"><span data-stu-id="abfab-162">Requirements</span></span>



| <span data-ttu-id="abfab-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="abfab-163">Requirement</span></span> | <span data-ttu-id="abfab-164">Valore</span><span class="sxs-lookup"><span data-stu-id="abfab-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="abfab-165">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="abfab-165">Minimum supported client</span></span><br/> | <span data-ttu-id="abfab-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abfab-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="abfab-167">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="abfab-167">Minimum supported server</span></span><br/> | <span data-ttu-id="abfab-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="abfab-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="abfab-169">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="abfab-169">Namespace</span></span><br/>                | <span data-ttu-id="abfab-170">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="abfab-170">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="abfab-171">MOF</span><span class="sxs-lookup"><span data-stu-id="abfab-171">MOF</span></span><br/>                      | <dl> <span data-ttu-id="abfab-172"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="abfab-172"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="abfab-173">DLL</span><span class="sxs-lookup"><span data-stu-id="abfab-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abfab-174"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abfab-174"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abfab-175">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="abfab-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abfab-176">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="abfab-176">CIM\_LogicalFile</span></span>](rename-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="abfab-177">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="abfab-177">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

