---
description: Copia il file o la directory del dispositivo logico specificato nel percorso dell'oggetto nel percorso specificato dal parametro FileName.
ms.assetid: 42cdb880-2431-4dcc-abdb-f271e2cd81a4
ms.tgt_platform: multiple
title: Metodo CopyEx della classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0e9519155accadc1a41a1c91492755db90eec696
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401447"
---
# <a name="copyex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="9fc0e-103">Metodo CopyEx della classe CIM \_ DeviceFile</span><span class="sxs-lookup"><span data-stu-id="9fc0e-103">CopyEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="9fc0e-104">Il metodo **CopyEx** copia il file o la directory del dispositivo logico specificato nel percorso dell'oggetto nel percorso specificato dal parametro *filename* .</span><span class="sxs-lookup"><span data-stu-id="9fc0e-104">The **CopyEx** method copies the logical device file (or directory) specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="9fc0e-105">Una copia non è supportata se è necessario sovrascrivere un file logico esistente.</span><span class="sxs-lookup"><span data-stu-id="9fc0e-105">A copy is not supported if overwriting an existing logical file is required.</span></span> <span data-ttu-id="9fc0e-106">Questo metodo è una versione estesa del metodo [**Copy**](copy-method-in-class-cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="9fc0e-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-devicefile.md) method.</span></span> <span data-ttu-id="9fc0e-107">Questo metodo viene ereditato da [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="9fc0e-107">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9fc0e-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="9fc0e-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9fc0e-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9fc0e-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9fc0e-110">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="9fc0e-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9fc0e-111">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9fc0e-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9fc0e-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9fc0e-112">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]  string     FileName,
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="9fc0e-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="9fc0e-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fc0e-114">*Nome file* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fc0e-114">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc0e-115">Nome completo del file di destinazione (o directory).</span><span class="sxs-lookup"><span data-stu-id="9fc0e-115">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="9fc0e-116">Esempio: "c: \\ temp \\ NewDirectory"</span><span class="sxs-lookup"><span data-stu-id="9fc0e-116">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="9fc0e-117">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9fc0e-117">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc0e-118">Stringa che rappresenta il nome del file o della directory in cui il metodo ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="9fc0e-118">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="9fc0e-119">Questo parametro è **null** se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9fc0e-119">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="9fc0e-120">*StartFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fc0e-120">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc0e-121">Stringa che rappresenta il file o la directory figlio da utilizzare come punto di partenza per questo metodo.</span><span class="sxs-lookup"><span data-stu-id="9fc0e-121">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="9fc0e-122">In genere, il parametro *StartFileName* è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="9fc0e-122">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="9fc0e-123">Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificati nella chiamata [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="9fc0e-123">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="9fc0e-124">*Ricorsivo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fc0e-124">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc0e-125">Se è TRUE, anche il metodo viene applicato in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza [**CIM \_ DeviceFile**](cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="9fc0e-125">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="9fc0e-126">Per le istanze di file, questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="9fc0e-126">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fc0e-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9fc0e-127">Return value</span></span>

<span data-ttu-id="9fc0e-128">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="9fc0e-128">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="9fc0e-129">0</span><span class="sxs-lookup"><span data-stu-id="9fc0e-129">0</span></span>

<span data-ttu-id="9fc0e-130">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9fc0e-130">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9fc0e-131">2</span><span class="sxs-lookup"><span data-stu-id="9fc0e-131">2</span></span>

<span data-ttu-id="9fc0e-132">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="9fc0e-132">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9fc0e-133">8</span><span class="sxs-lookup"><span data-stu-id="9fc0e-133">8</span></span>

<span data-ttu-id="9fc0e-134">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="9fc0e-134">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9fc0e-135">9</span><span class="sxs-lookup"><span data-stu-id="9fc0e-135">9</span></span>

<span data-ttu-id="9fc0e-136">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="9fc0e-136">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9fc0e-137">10</span><span class="sxs-lookup"><span data-stu-id="9fc0e-137">10</span></span>

<span data-ttu-id="9fc0e-138">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="9fc0e-138">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9fc0e-139">11</span><span class="sxs-lookup"><span data-stu-id="9fc0e-139">11</span></span>

<span data-ttu-id="9fc0e-140">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="9fc0e-140">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9fc0e-141">12</span><span class="sxs-lookup"><span data-stu-id="9fc0e-141">12</span></span>

<span data-ttu-id="9fc0e-142">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="9fc0e-142">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9fc0e-143">13</span><span class="sxs-lookup"><span data-stu-id="9fc0e-143">13</span></span>

<span data-ttu-id="9fc0e-144">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="9fc0e-144">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9fc0e-145">14</span><span class="sxs-lookup"><span data-stu-id="9fc0e-145">14</span></span>

<span data-ttu-id="9fc0e-146">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="9fc0e-146">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9fc0e-147">15</span><span class="sxs-lookup"><span data-stu-id="9fc0e-147">15</span></span>

<span data-ttu-id="9fc0e-148">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="9fc0e-148">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9fc0e-149">16</span><span class="sxs-lookup"><span data-stu-id="9fc0e-149">16</span></span>

<span data-ttu-id="9fc0e-150">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="9fc0e-150">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9fc0e-151">17</span><span class="sxs-lookup"><span data-stu-id="9fc0e-151">17</span></span>

<span data-ttu-id="9fc0e-152">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="9fc0e-152">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9fc0e-153">21</span><span class="sxs-lookup"><span data-stu-id="9fc0e-153">21</span></span>

<span data-ttu-id="9fc0e-154">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="9fc0e-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9fc0e-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="9fc0e-155">Remarks</span></span>

<span data-ttu-id="9fc0e-156">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="9fc0e-156">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="9fc0e-157">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="9fc0e-157">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="9fc0e-158">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="9fc0e-158">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9fc0e-159">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="9fc0e-159">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fc0e-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9fc0e-160">Requirements</span></span>



| <span data-ttu-id="9fc0e-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fc0e-161">Requirement</span></span> | <span data-ttu-id="9fc0e-162">Valore</span><span class="sxs-lookup"><span data-stu-id="9fc0e-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc0e-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fc0e-163">Minimum supported client</span></span><br/> | <span data-ttu-id="9fc0e-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9fc0e-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9fc0e-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fc0e-165">Minimum supported server</span></span><br/> | <span data-ttu-id="9fc0e-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9fc0e-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9fc0e-167">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9fc0e-167">Namespace</span></span><br/>                | <span data-ttu-id="9fc0e-168">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="9fc0e-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9fc0e-169">MOF</span><span class="sxs-lookup"><span data-stu-id="9fc0e-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9fc0e-170"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9fc0e-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9fc0e-171">DLL</span><span class="sxs-lookup"><span data-stu-id="9fc0e-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fc0e-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fc0e-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fc0e-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9fc0e-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fc0e-174">\_DEVICEFILE CIM</span><span class="sxs-lookup"><span data-stu-id="9fc0e-174">CIM\_DeviceFile</span></span>](copyex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="9fc0e-175">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="9fc0e-175">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

