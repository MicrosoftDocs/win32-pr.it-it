---
description: Il metodo Copy copia il file o la directory logica specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.
ms.assetid: 13bd7da8-a562-414b-8d23-6f58e1c55878
ms.tgt_platform: multiple
title: Metodo Copy della classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c126f1cd54470e50a700fdea1c121776d687a9dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304901"
---
# <a name="copy-method-of-the-cim_datafile-class"></a><span data-ttu-id="800b9-103">Metodo Copy della classe del file di \_ DataFile CIM</span><span class="sxs-lookup"><span data-stu-id="800b9-103">Copy method of the CIM\_DataFile class</span></span>

<span data-ttu-id="800b9-104">Il metodo **Copy** copia il file o la directory logica specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.</span><span class="sxs-lookup"><span data-stu-id="800b9-104">The **Copy** method copies the logical file (or directory) that is specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="800b9-105">Una copia non è supportata se richiede la sovrascrittura di un file logico esistente.</span><span class="sxs-lookup"><span data-stu-id="800b9-105">A copy is not supported if it requires overwriting an existing logical file.</span></span> <span data-ttu-id="800b9-106">Questo metodo viene ereditato da [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="800b9-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="800b9-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="800b9-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="800b9-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="800b9-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="800b9-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="800b9-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="800b9-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="800b9-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="800b9-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="800b9-111">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="800b9-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="800b9-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="800b9-113">*Nome file* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="800b9-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="800b9-114">Nome completo del file di destinazione (o directory).</span><span class="sxs-lookup"><span data-stu-id="800b9-114">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="800b9-115">Esempio: "c: \\ temp \\ NewDirectory"</span><span class="sxs-lookup"><span data-stu-id="800b9-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="800b9-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="800b9-116">Return value</span></span>

<span data-ttu-id="800b9-117">Restituisce un valore pari a 0 in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="800b9-117">Returns a value of 0 on success, and any other number to indicate an error.</span></span> <span data-ttu-id="800b9-118">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="800b9-118">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="800b9-119">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="800b9-119">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="800b9-120">**0**</span><span class="sxs-lookup"><span data-stu-id="800b9-120">**0**</span></span>
</dt> <dd>

<span data-ttu-id="800b9-121">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="800b9-121">Success.</span></span>

</dd> <dt>

<span data-ttu-id="800b9-122">**2**</span><span class="sxs-lookup"><span data-stu-id="800b9-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="800b9-123">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="800b9-123">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="800b9-124">**8**</span><span class="sxs-lookup"><span data-stu-id="800b9-124">**8**</span></span>
</dt> <dd>

<span data-ttu-id="800b9-125">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="800b9-125">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="800b9-126">**9**</span><span class="sxs-lookup"><span data-stu-id="800b9-126">**9**</span></span>
</dt> <dd>

<span data-ttu-id="800b9-127">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="800b9-127">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="800b9-128">**10**</span><span class="sxs-lookup"><span data-stu-id="800b9-128">**10**</span></span>
</dt> <dd>

<span data-ttu-id="800b9-129">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="800b9-129">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="800b9-130">**11**</span><span class="sxs-lookup"><span data-stu-id="800b9-130">**11**</span></span>
</dt> <dd>

<span data-ttu-id="800b9-131">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="800b9-131">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="800b9-132">**12**</span><span class="sxs-lookup"><span data-stu-id="800b9-132">**12**</span></span>
</dt> <dd>

<span data-ttu-id="800b9-133">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="800b9-133">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="800b9-134">**13**</span><span class="sxs-lookup"><span data-stu-id="800b9-134">**13**</span></span>
</dt> <dd>

<span data-ttu-id="800b9-135">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="800b9-135">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="800b9-136">**14**</span><span class="sxs-lookup"><span data-stu-id="800b9-136">**14**</span></span>
</dt> <dd>

<span data-ttu-id="800b9-137">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="800b9-137">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="800b9-138">**15**</span><span class="sxs-lookup"><span data-stu-id="800b9-138">**15**</span></span>
</dt> <dd>

<span data-ttu-id="800b9-139">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="800b9-139">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="800b9-140">**16**</span><span class="sxs-lookup"><span data-stu-id="800b9-140">**16**</span></span>
</dt> <dd>

<span data-ttu-id="800b9-141">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="800b9-141">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="800b9-142">**17**</span><span class="sxs-lookup"><span data-stu-id="800b9-142">**17**</span></span>
</dt> <dd>

<span data-ttu-id="800b9-143">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="800b9-143">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="800b9-144">**21**</span><span class="sxs-lookup"><span data-stu-id="800b9-144">**21**</span></span>
</dt> <dd>

<span data-ttu-id="800b9-145">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="800b9-145">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="800b9-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="800b9-146">Remarks</span></span>

<span data-ttu-id="800b9-147">Il metodo di **copia** nel file di file [**CIM \_**](cim-datafile.md) viene implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="800b9-147">The **Copy** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="800b9-148">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="800b9-148">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="800b9-149">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="800b9-149">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="800b9-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="800b9-150">Requirements</span></span>



| <span data-ttu-id="800b9-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="800b9-151">Requirement</span></span> | <span data-ttu-id="800b9-152">Valore</span><span class="sxs-lookup"><span data-stu-id="800b9-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="800b9-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="800b9-153">Minimum supported client</span></span><br/> | <span data-ttu-id="800b9-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="800b9-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="800b9-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="800b9-155">Minimum supported server</span></span><br/> | <span data-ttu-id="800b9-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="800b9-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="800b9-157">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="800b9-157">Namespace</span></span><br/>                | <span data-ttu-id="800b9-158">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="800b9-158">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="800b9-159">MOF</span><span class="sxs-lookup"><span data-stu-id="800b9-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="800b9-160"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="800b9-160"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="800b9-161">DLL</span><span class="sxs-lookup"><span data-stu-id="800b9-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="800b9-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="800b9-162"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="800b9-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="800b9-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="800b9-164">File di \_ DataFile CIM</span><span class="sxs-lookup"><span data-stu-id="800b9-164">CIM\_DataFile</span></span>](copy-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="800b9-165">**File di \_ DataFile CIM**</span><span class="sxs-lookup"><span data-stu-id="800b9-165">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="800b9-166">Attività WMI: file e cartelle</span><span class="sxs-lookup"><span data-stu-id="800b9-166">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="800b9-167">**Costanti dei diritti di accesso a file e directory**</span><span class="sxs-lookup"><span data-stu-id="800b9-167">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

