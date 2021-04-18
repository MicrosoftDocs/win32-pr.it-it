---
description: Il metodo CopyEx copia il file o la directory logica specificata nel percorso dell'oggetto nel percorso specificato dal parametro FileName.
ms.assetid: e52c1a0f-e34c-4a61-9e54-ed172976cb61
ms.tgt_platform: multiple
title: Metodo CopyEx della classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a83f1556aeeafbb5cc95eddbd84806bdaef0be14
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304896"
---
# <a name="copyex-method-of-the-cim_datafile-class"></a><span data-ttu-id="0e2ae-103">Metodo CopyEx della classe del file di \_ DataFile CIM</span><span class="sxs-lookup"><span data-stu-id="0e2ae-103">CopyEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="0e2ae-104">Il metodo **CopyEx** copia il file o la directory logica specificata nel percorso dell'oggetto nel percorso specificato dal parametro *filename* .</span><span class="sxs-lookup"><span data-stu-id="0e2ae-104">The **CopyEx** method copies the logical file (or directory) that is specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="0e2ae-105">Una copia non è supportata se richiede la sovrascrittura di un file logico esistente.</span><span class="sxs-lookup"><span data-stu-id="0e2ae-105">A copy is not supported if it requires overwriting an existing logical file.</span></span> <span data-ttu-id="0e2ae-106">Questo metodo è una versione estesa del metodo [**Copy**](copy-method-in-class-cim-datafile.md) ed è ereditato da [CIM \_ LogicalFile](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="0e2ae-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-datafile.md) method and is inherited from [CIM\_LogicalFile](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0e2ae-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="0e2ae-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0e2ae-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0e2ae-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0e2ae-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="0e2ae-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0e2ae-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0e2ae-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0e2ae-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e2ae-111">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]  string     FileName,
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="0e2ae-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="0e2ae-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e2ae-113">*Nome file* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e2ae-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e2ae-114">Nome completo del file di destinazione (o directory).</span><span class="sxs-lookup"><span data-stu-id="0e2ae-114">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="0e2ae-115">Esempio: "c: \\ temp \\ NewDirectory"</span><span class="sxs-lookup"><span data-stu-id="0e2ae-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="0e2ae-116">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0e2ae-116">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e2ae-117">Stringa che rappresenta il nome del file o della directory in cui il metodo ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="0e2ae-117">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="0e2ae-118">Questo parametro sarà **null** se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0e2ae-118">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="0e2ae-119">*StartFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e2ae-119">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e2ae-120">Stringa che rappresenta il file o la directory figlio da utilizzare come punto di partenza per questo metodo.</span><span class="sxs-lookup"><span data-stu-id="0e2ae-120">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="0e2ae-121">In genere, il parametro *StartFileName* è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="0e2ae-121">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="0e2ae-122">Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificati nella chiamata [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="0e2ae-122">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

<span data-ttu-id="0e2ae-123">Se si usa *StartFileName* , è necessario impostare *ricorsivo* su true.</span><span class="sxs-lookup"><span data-stu-id="0e2ae-123">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="0e2ae-124">*Ricorsivo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e2ae-124">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e2ae-125">Se TRUE, il metodo viene anche applicato in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza di [**\_ DataFile DataFile**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="0e2ae-125">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="0e2ae-126">Per le istanze di file, questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="0e2ae-126">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e2ae-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0e2ae-127">Return value</span></span>

<span data-ttu-id="0e2ae-128">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="0e2ae-128">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="0e2ae-129">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="0e2ae-129">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="0e2ae-130">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="0e2ae-130">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="0e2ae-131">0</span><span class="sxs-lookup"><span data-stu-id="0e2ae-131">0</span></span>

<span data-ttu-id="0e2ae-132">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0e2ae-132">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0e2ae-133">2</span><span class="sxs-lookup"><span data-stu-id="0e2ae-133">2</span></span>

<span data-ttu-id="0e2ae-134">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="0e2ae-134">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0e2ae-135">8</span><span class="sxs-lookup"><span data-stu-id="0e2ae-135">8</span></span>

<span data-ttu-id="0e2ae-136">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="0e2ae-136">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0e2ae-137">9</span><span class="sxs-lookup"><span data-stu-id="0e2ae-137">9</span></span>

<span data-ttu-id="0e2ae-138">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="0e2ae-138">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0e2ae-139">10</span><span class="sxs-lookup"><span data-stu-id="0e2ae-139">10</span></span>

<span data-ttu-id="0e2ae-140">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="0e2ae-140">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0e2ae-141">11</span><span class="sxs-lookup"><span data-stu-id="0e2ae-141">11</span></span>

<span data-ttu-id="0e2ae-142">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="0e2ae-142">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0e2ae-143">12</span><span class="sxs-lookup"><span data-stu-id="0e2ae-143">12</span></span>

<span data-ttu-id="0e2ae-144">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="0e2ae-144">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0e2ae-145">13</span><span class="sxs-lookup"><span data-stu-id="0e2ae-145">13</span></span>

<span data-ttu-id="0e2ae-146">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="0e2ae-146">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0e2ae-147">14</span><span class="sxs-lookup"><span data-stu-id="0e2ae-147">14</span></span>

<span data-ttu-id="0e2ae-148">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="0e2ae-148">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0e2ae-149">15</span><span class="sxs-lookup"><span data-stu-id="0e2ae-149">15</span></span>

<span data-ttu-id="0e2ae-150">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="0e2ae-150">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0e2ae-151">16</span><span class="sxs-lookup"><span data-stu-id="0e2ae-151">16</span></span>

<span data-ttu-id="0e2ae-152">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="0e2ae-152">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0e2ae-153">17</span><span class="sxs-lookup"><span data-stu-id="0e2ae-153">17</span></span>

<span data-ttu-id="0e2ae-154">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="0e2ae-154">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0e2ae-155">21</span><span class="sxs-lookup"><span data-stu-id="0e2ae-155">21</span></span>

<span data-ttu-id="0e2ae-156">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="0e2ae-156">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e2ae-157">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e2ae-157">Remarks</span></span>

<span data-ttu-id="0e2ae-158">Il metodo **CopyEx** nel file di [**\_ DataFile CIM**](cim-datafile.md) viene implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="0e2ae-158">The **CopyEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="0e2ae-159">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="0e2ae-159">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0e2ae-160">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="0e2ae-160">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e2ae-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e2ae-161">Requirements</span></span>



| <span data-ttu-id="0e2ae-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e2ae-162">Requirement</span></span> | <span data-ttu-id="0e2ae-163">Valore</span><span class="sxs-lookup"><span data-stu-id="0e2ae-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e2ae-164">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e2ae-164">Minimum supported client</span></span><br/> | <span data-ttu-id="0e2ae-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e2ae-165">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0e2ae-166">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e2ae-166">Minimum supported server</span></span><br/> | <span data-ttu-id="0e2ae-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e2ae-167">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0e2ae-168">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0e2ae-168">Namespace</span></span><br/>                | <span data-ttu-id="0e2ae-169">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="0e2ae-169">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0e2ae-170">MOF</span><span class="sxs-lookup"><span data-stu-id="0e2ae-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e2ae-171"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e2ae-171"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e2ae-172">DLL</span><span class="sxs-lookup"><span data-stu-id="0e2ae-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e2ae-173"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e2ae-173"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e2ae-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e2ae-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e2ae-175">**File di \_ DataFile CIM**</span><span class="sxs-lookup"><span data-stu-id="0e2ae-175">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="0e2ae-176">Attività WMI: file e cartelle</span><span class="sxs-lookup"><span data-stu-id="0e2ae-176">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="0e2ae-177">**Costanti dei diritti di accesso a file e directory**</span><span class="sxs-lookup"><span data-stu-id="0e2ae-177">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

