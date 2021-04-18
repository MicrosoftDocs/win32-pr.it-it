---
description: Copia il file o la directory logica specificata nel percorso dell'oggetto nel percorso specificato dal parametro FileName.
ms.assetid: 534d8b73-fc22-4a42-b8e6-24a54353bb14
ms.tgt_platform: multiple
title: Metodo CopyEx della classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ec7c44ec3fc01074a0f4af70249236aa366d64bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305294"
---
# <a name="copyex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="3d44e-103">Metodo CopyEx della classe CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="3d44e-103">CopyEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="3d44e-104">Il metodo **CopyEx** copia il file logico o la directory specificata nel percorso dell'oggetto nella posizione specificata dal parametro *filename* .</span><span class="sxs-lookup"><span data-stu-id="3d44e-104">The **CopyEx** method copies the logical file (or directory) specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="3d44e-105">Una copia non è supportata se è necessario sovrascrivere un file logico esistente.</span><span class="sxs-lookup"><span data-stu-id="3d44e-105">A copy is not supported if overwriting an existing logical file is required.</span></span> <span data-ttu-id="3d44e-106">Questo metodo è una versione estesa del metodo [**Copy**](copy-method-in-class-cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="3d44e-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-logicalfile.md) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3d44e-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="3d44e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3d44e-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3d44e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3d44e-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="3d44e-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3d44e-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3d44e-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3d44e-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d44e-111">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="3d44e-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d44e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d44e-113">*Nome file* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d44e-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d44e-114">Nome completo del file di destinazione (o directory).</span><span class="sxs-lookup"><span data-stu-id="3d44e-114">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="3d44e-115">Esempio: "c: \\ temp \\ NewDirectory"</span><span class="sxs-lookup"><span data-stu-id="3d44e-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="3d44e-116">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3d44e-116">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d44e-117">Stringa che rappresenta il nome del file o della directory in cui il metodo ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="3d44e-117">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="3d44e-118">Questo parametro è **null** se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="3d44e-118">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="3d44e-119">*StartFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3d44e-119">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3d44e-120">Stringa che assegna un nome al file figlio (o alla directory) da utilizzare come punto di partenza per questo metodo.</span><span class="sxs-lookup"><span data-stu-id="3d44e-120">String that names the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="3d44e-121">In genere, il parametro *StartFileName* è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="3d44e-121">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="3d44e-122">Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificata nella chiamata [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="3d44e-122">If this parameter is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="3d44e-123">*Ricorsivo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3d44e-123">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3d44e-124">Se è TRUE, anche il metodo viene applicato in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="3d44e-124">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="3d44e-125">Per le istanze di file, questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="3d44e-125">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d44e-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3d44e-126">Return value</span></span>

<span data-ttu-id="3d44e-127">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="3d44e-127">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="3d44e-128">**Success**</span><span class="sxs-lookup"><span data-stu-id="3d44e-128">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="3d44e-129">0</span><span class="sxs-lookup"><span data-stu-id="3d44e-129">0</span></span>

<span data-ttu-id="3d44e-130">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="3d44e-130">Success.</span></span>

</dd> <dt>

<span data-ttu-id="3d44e-131">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="3d44e-131">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="3d44e-132">2</span><span class="sxs-lookup"><span data-stu-id="3d44e-132">2</span></span>

<span data-ttu-id="3d44e-133">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="3d44e-133">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="3d44e-134">**Errore non specificato**</span><span class="sxs-lookup"><span data-stu-id="3d44e-134">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="3d44e-135">8</span><span class="sxs-lookup"><span data-stu-id="3d44e-135">8</span></span>

<span data-ttu-id="3d44e-136">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="3d44e-136">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="3d44e-137">**Oggetto non valido**</span><span class="sxs-lookup"><span data-stu-id="3d44e-137">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="3d44e-138">9</span><span class="sxs-lookup"><span data-stu-id="3d44e-138">9</span></span>

<span data-ttu-id="3d44e-139">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="3d44e-139">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="3d44e-140">**Oggetto già esistente**</span><span class="sxs-lookup"><span data-stu-id="3d44e-140">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="3d44e-141">10</span><span class="sxs-lookup"><span data-stu-id="3d44e-141">10</span></span>

<span data-ttu-id="3d44e-142">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="3d44e-142">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3d44e-143">**File System non NTFS**</span><span class="sxs-lookup"><span data-stu-id="3d44e-143">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="3d44e-144">11</span><span class="sxs-lookup"><span data-stu-id="3d44e-144">11</span></span>

<span data-ttu-id="3d44e-145">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="3d44e-145">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="3d44e-146">**Piattaforma non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="3d44e-146">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="3d44e-147">12</span><span class="sxs-lookup"><span data-stu-id="3d44e-147">12</span></span>

<span data-ttu-id="3d44e-148">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="3d44e-148">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="3d44e-149">**Unità non uguale**</span><span class="sxs-lookup"><span data-stu-id="3d44e-149">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="3d44e-150">13</span><span class="sxs-lookup"><span data-stu-id="3d44e-150">13</span></span>

<span data-ttu-id="3d44e-151">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="3d44e-151">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="3d44e-152">**Directory non vuota**</span><span class="sxs-lookup"><span data-stu-id="3d44e-152">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="3d44e-153">14</span><span class="sxs-lookup"><span data-stu-id="3d44e-153">14</span></span>

<span data-ttu-id="3d44e-154">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="3d44e-154">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="3d44e-155">**Violazione di condivisione**</span><span class="sxs-lookup"><span data-stu-id="3d44e-155">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="3d44e-156">15</span><span class="sxs-lookup"><span data-stu-id="3d44e-156">15</span></span>

<span data-ttu-id="3d44e-157">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="3d44e-157">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="3d44e-158">**File di avvio non valido**</span><span class="sxs-lookup"><span data-stu-id="3d44e-158">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="3d44e-159">16</span><span class="sxs-lookup"><span data-stu-id="3d44e-159">16</span></span>

<span data-ttu-id="3d44e-160">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="3d44e-160">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="3d44e-161">**Privilegio non mantenuto**</span><span class="sxs-lookup"><span data-stu-id="3d44e-161">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="3d44e-162">17</span><span class="sxs-lookup"><span data-stu-id="3d44e-162">17</span></span>

<span data-ttu-id="3d44e-163">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="3d44e-163">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="3d44e-164">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="3d44e-164">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="3d44e-165">21</span><span class="sxs-lookup"><span data-stu-id="3d44e-165">21</span></span>

<span data-ttu-id="3d44e-166">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="3d44e-166">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d44e-167">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d44e-167">Remarks</span></span>

<span data-ttu-id="3d44e-168">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="3d44e-168">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="3d44e-169">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="3d44e-169">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="3d44e-170">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="3d44e-170">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3d44e-171">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="3d44e-171">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d44e-172">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d44e-172">Requirements</span></span>



| <span data-ttu-id="3d44e-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d44e-173">Requirement</span></span> | <span data-ttu-id="3d44e-174">Valore</span><span class="sxs-lookup"><span data-stu-id="3d44e-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d44e-175">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d44e-175">Minimum supported client</span></span><br/> | <span data-ttu-id="3d44e-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d44e-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3d44e-177">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d44e-177">Minimum supported server</span></span><br/> | <span data-ttu-id="3d44e-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d44e-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3d44e-179">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3d44e-179">Namespace</span></span><br/>                | <span data-ttu-id="3d44e-180">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="3d44e-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3d44e-181">MOF</span><span class="sxs-lookup"><span data-stu-id="3d44e-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d44e-182"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d44e-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d44e-183">DLL</span><span class="sxs-lookup"><span data-stu-id="3d44e-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d44e-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d44e-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d44e-185">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d44e-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d44e-186">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="3d44e-186">CIM\_LogicalFile</span></span>](copyex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="3d44e-187">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="3d44e-187">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

