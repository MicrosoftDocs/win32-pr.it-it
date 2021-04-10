---
description: Il metodo DeleteEx Elimina il file o la directory logica specificata nel percorso dell'oggetto. Questo metodo è una versione estesa del metodo Delete ed è ereditato da CIM \_ LogicalFile.
ms.assetid: 565d604f-01e0-4cd4-b182-9750c58bae5f
ms.tgt_platform: multiple
title: Metodo DeleteEx della classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9af120c76e4ab8c53c945bd13aa62a2295385ac2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126531"
---
# <a name="deleteex-method-of-the-cim_datafile-class"></a><span data-ttu-id="ecadb-104">Metodo DeleteEx della classe del file di \_ DataFile CIM</span><span class="sxs-lookup"><span data-stu-id="ecadb-104">DeleteEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="ecadb-105">Il metodo **DeleteEx** Elimina il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ecadb-105">The **DeleteEx** method deletes the logical file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="ecadb-106">Questo metodo è una versione estesa del metodo [**Delete**](delete-method-in-class-cim-datafile.md) ed è ereditato da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ecadb-106">This method is an extended version of the [**Delete**](delete-method-in-class-cim-datafile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ecadb-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="ecadb-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ecadb-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ecadb-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ecadb-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="ecadb-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ecadb-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ecadb-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ecadb-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ecadb-111">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="ecadb-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="ecadb-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecadb-113">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ecadb-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ecadb-114">Stringa che rappresenta il nome del file o della directory in cui il metodo ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ecadb-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="ecadb-115">Questo parametro è null se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ecadb-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="ecadb-116">*StartFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ecadb-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecadb-117">Stringa che rappresenta il file o la directory figlio da utilizzare come punto di partenza per questo metodo.</span><span class="sxs-lookup"><span data-stu-id="ecadb-117">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="ecadb-118">In genere, il parametro *StartFileName* è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="ecadb-118">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="ecadb-119">Se questo parametro è null, l'operazione viene eseguita sul file o sulla directory specificati nella chiamata [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="ecadb-119">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecadb-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ecadb-120">Return value</span></span>

<span data-ttu-id="ecadb-121">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="ecadb-121">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="ecadb-122">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ecadb-122">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ecadb-123">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ecadb-123">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="ecadb-124">0</span><span class="sxs-lookup"><span data-stu-id="ecadb-124">0</span></span>

<span data-ttu-id="ecadb-125">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ecadb-125">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ecadb-126">2</span><span class="sxs-lookup"><span data-stu-id="ecadb-126">2</span></span>

<span data-ttu-id="ecadb-127">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="ecadb-127">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ecadb-128">8</span><span class="sxs-lookup"><span data-stu-id="ecadb-128">8</span></span>

<span data-ttu-id="ecadb-129">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="ecadb-129">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ecadb-130">9</span><span class="sxs-lookup"><span data-stu-id="ecadb-130">9</span></span>

<span data-ttu-id="ecadb-131">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="ecadb-131">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ecadb-132">10</span><span class="sxs-lookup"><span data-stu-id="ecadb-132">10</span></span>

<span data-ttu-id="ecadb-133">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="ecadb-133">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ecadb-134">11</span><span class="sxs-lookup"><span data-stu-id="ecadb-134">11</span></span>

<span data-ttu-id="ecadb-135">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="ecadb-135">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ecadb-136">12</span><span class="sxs-lookup"><span data-stu-id="ecadb-136">12</span></span>

<span data-ttu-id="ecadb-137">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="ecadb-137">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ecadb-138">13</span><span class="sxs-lookup"><span data-stu-id="ecadb-138">13</span></span>

<span data-ttu-id="ecadb-139">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="ecadb-139">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ecadb-140">14</span><span class="sxs-lookup"><span data-stu-id="ecadb-140">14</span></span>

<span data-ttu-id="ecadb-141">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="ecadb-141">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ecadb-142">15</span><span class="sxs-lookup"><span data-stu-id="ecadb-142">15</span></span>

<span data-ttu-id="ecadb-143">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="ecadb-143">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ecadb-144">16</span><span class="sxs-lookup"><span data-stu-id="ecadb-144">16</span></span>

<span data-ttu-id="ecadb-145">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="ecadb-145">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ecadb-146">17</span><span class="sxs-lookup"><span data-stu-id="ecadb-146">17</span></span>

<span data-ttu-id="ecadb-147">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="ecadb-147">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="ecadb-148">21</span><span class="sxs-lookup"><span data-stu-id="ecadb-148">21</span></span>

<span data-ttu-id="ecadb-149">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="ecadb-149">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ecadb-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="ecadb-150">Remarks</span></span>

<span data-ttu-id="ecadb-151">Il metodo **DeleteEx** nel file di [**\_ DataFile CIM**](cim-datafile.md) viene implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="ecadb-151">The **DeleteEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="ecadb-152">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="ecadb-152">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ecadb-153">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="ecadb-153">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecadb-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ecadb-154">Requirements</span></span>



| <span data-ttu-id="ecadb-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecadb-155">Requirement</span></span> | <span data-ttu-id="ecadb-156">Valore</span><span class="sxs-lookup"><span data-stu-id="ecadb-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ecadb-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecadb-157">Minimum supported client</span></span><br/> | <span data-ttu-id="ecadb-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ecadb-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ecadb-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecadb-159">Minimum supported server</span></span><br/> | <span data-ttu-id="ecadb-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ecadb-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ecadb-161">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ecadb-161">Namespace</span></span><br/>                | <span data-ttu-id="ecadb-162">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ecadb-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ecadb-163">MOF</span><span class="sxs-lookup"><span data-stu-id="ecadb-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ecadb-164"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ecadb-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ecadb-165">DLL</span><span class="sxs-lookup"><span data-stu-id="ecadb-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecadb-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecadb-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecadb-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ecadb-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecadb-168">File di \_ DataFile CIM</span><span class="sxs-lookup"><span data-stu-id="ecadb-168">CIM\_DataFile</span></span>](deleteex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="ecadb-169">**File di \_ DataFile CIM**</span><span class="sxs-lookup"><span data-stu-id="ecadb-169">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="ecadb-170">Attività WMI: file e cartelle</span><span class="sxs-lookup"><span data-stu-id="ecadb-170">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="ecadb-171">**Costanti dei diritti di accesso a file e directory**</span><span class="sxs-lookup"><span data-stu-id="ecadb-171">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

