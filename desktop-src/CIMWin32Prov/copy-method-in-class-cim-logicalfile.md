---
description: Il metodo Copy copia il file logico o la directory specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.
ms.assetid: 643946e4-5d32-4839-ae1f-80ec7cede429
ms.tgt_platform: multiple
title: Metodo Copy della classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4a69107bd173be0aa853c1541a1e1365148c2e59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049204"
---
# <a name="copy-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="59399-103">Metodo Copy della classe CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="59399-103">Copy method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="59399-104">Il metodo **Copy** copia il file logico o la directory specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.</span><span class="sxs-lookup"><span data-stu-id="59399-104">The **Copy** method copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="59399-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="59399-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="59399-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="59399-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="59399-107">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="59399-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="59399-108">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="59399-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="59399-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59399-109">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="59399-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="59399-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59399-111">*Nome file* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59399-111">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59399-112">Nome completo del file di destinazione (o directory).</span><span class="sxs-lookup"><span data-stu-id="59399-112">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="59399-113">Esempio: "c: \\ temp \\ NewDirectory"</span><span class="sxs-lookup"><span data-stu-id="59399-113">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59399-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="59399-114">Return value</span></span>

<span data-ttu-id="59399-115">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="59399-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="59399-116">**Success**</span><span class="sxs-lookup"><span data-stu-id="59399-116">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="59399-117">0</span><span class="sxs-lookup"><span data-stu-id="59399-117">0</span></span>

<span data-ttu-id="59399-118">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="59399-118">Success.</span></span>

</dd> <dt>

<span data-ttu-id="59399-119">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="59399-119">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="59399-120">2</span><span class="sxs-lookup"><span data-stu-id="59399-120">2</span></span>

<span data-ttu-id="59399-121">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="59399-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="59399-122">**Errore non specificato**</span><span class="sxs-lookup"><span data-stu-id="59399-122">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="59399-123">8</span><span class="sxs-lookup"><span data-stu-id="59399-123">8</span></span>

<span data-ttu-id="59399-124">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="59399-124">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="59399-125">**Oggetto non valido**</span><span class="sxs-lookup"><span data-stu-id="59399-125">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="59399-126">9</span><span class="sxs-lookup"><span data-stu-id="59399-126">9</span></span>

<span data-ttu-id="59399-127">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="59399-127">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="59399-128">**Oggetto già esistente**</span><span class="sxs-lookup"><span data-stu-id="59399-128">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="59399-129">10</span><span class="sxs-lookup"><span data-stu-id="59399-129">10</span></span>

<span data-ttu-id="59399-130">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="59399-130">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="59399-131">**File System non NTFS**</span><span class="sxs-lookup"><span data-stu-id="59399-131">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="59399-132">11</span><span class="sxs-lookup"><span data-stu-id="59399-132">11</span></span>

<span data-ttu-id="59399-133">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="59399-133">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="59399-134">**Piattaforma non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="59399-134">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="59399-135">12</span><span class="sxs-lookup"><span data-stu-id="59399-135">12</span></span>

<span data-ttu-id="59399-136">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="59399-136">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="59399-137">**Unità non uguale**</span><span class="sxs-lookup"><span data-stu-id="59399-137">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="59399-138">13</span><span class="sxs-lookup"><span data-stu-id="59399-138">13</span></span>

<span data-ttu-id="59399-139">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="59399-139">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="59399-140">**Directory non vuota**</span><span class="sxs-lookup"><span data-stu-id="59399-140">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="59399-141">14</span><span class="sxs-lookup"><span data-stu-id="59399-141">14</span></span>

<span data-ttu-id="59399-142">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="59399-142">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="59399-143">**Violazione di condivisione**</span><span class="sxs-lookup"><span data-stu-id="59399-143">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="59399-144">15</span><span class="sxs-lookup"><span data-stu-id="59399-144">15</span></span>

<span data-ttu-id="59399-145">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="59399-145">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="59399-146">**File di avvio non valido**</span><span class="sxs-lookup"><span data-stu-id="59399-146">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="59399-147">16</span><span class="sxs-lookup"><span data-stu-id="59399-147">16</span></span>

<span data-ttu-id="59399-148">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="59399-148">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="59399-149">**Privilegio non mantenuto**</span><span class="sxs-lookup"><span data-stu-id="59399-149">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="59399-150">17</span><span class="sxs-lookup"><span data-stu-id="59399-150">17</span></span>

<span data-ttu-id="59399-151">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="59399-151">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="59399-152">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="59399-152">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="59399-153">21</span><span class="sxs-lookup"><span data-stu-id="59399-153">21</span></span>

<span data-ttu-id="59399-154">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="59399-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="59399-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="59399-155">Remarks</span></span>

<span data-ttu-id="59399-156">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="59399-156">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="59399-157">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="59399-157">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="59399-158">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="59399-158">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="59399-159">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="59399-159">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="59399-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59399-160">Requirements</span></span>



| <span data-ttu-id="59399-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="59399-161">Requirement</span></span> | <span data-ttu-id="59399-162">Valore</span><span class="sxs-lookup"><span data-stu-id="59399-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59399-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59399-163">Minimum supported client</span></span><br/> | <span data-ttu-id="59399-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59399-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="59399-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59399-165">Minimum supported server</span></span><br/> | <span data-ttu-id="59399-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59399-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="59399-167">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="59399-167">Namespace</span></span><br/>                | <span data-ttu-id="59399-168">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="59399-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="59399-169">MOF</span><span class="sxs-lookup"><span data-stu-id="59399-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59399-170"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="59399-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="59399-171">DLL</span><span class="sxs-lookup"><span data-stu-id="59399-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59399-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59399-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59399-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59399-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59399-174">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="59399-174">CIM\_LogicalFile</span></span>](copy-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="59399-175">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="59399-175">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

