---
description: Copia il file o la directory della voce di directory logica specificata nel percorso dell'oggetto nel percorso specificato dal parametro FileName. Questo metodo è una versione estesa del metodo Copy.
ms.assetid: c15bd1ae-a60d-4875-a76e-99486820c42c
ms.tgt_platform: multiple
title: Metodo CopyEx della classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 55f2fdb0aa4e8306e8ec0aa4f5f265c0a8ee6689
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878401"
---
# <a name="copyex-method-of-the-win32_directory-class"></a><span data-ttu-id="091e7-104">Metodo CopyEx della classe di \_ directory Win32</span><span class="sxs-lookup"><span data-stu-id="091e7-104">CopyEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="091e7-105">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CopyEx** copia il file di voce della directory logica o la directory specificata nel percorso dell'oggetto nel percorso specificato dal parametro *filename* .</span><span class="sxs-lookup"><span data-stu-id="091e7-105">The **CopyEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical directory entry file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="091e7-106">Questo metodo è una versione estesa del metodo [**Copy**](copy-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="091e7-106">This method is an extended version of the [**Copy**](copy-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="091e7-107">Una copia non è supportata se è necessario sovrascrivere un file logico esistente.</span><span class="sxs-lookup"><span data-stu-id="091e7-107">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="091e7-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="091e7-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="091e7-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="091e7-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="091e7-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="091e7-110">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="091e7-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="091e7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="091e7-112">*Nome file* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="091e7-112">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="091e7-113">Nome completo della copia del file (o directory).</span><span class="sxs-lookup"><span data-stu-id="091e7-113">Fully qualified name of the copy of the file (or directory).</span></span> <span data-ttu-id="091e7-114">Esempio: c: \\ temp \\ NewDirectory.</span><span class="sxs-lookup"><span data-stu-id="091e7-114">Example: c:\\temp\\newdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="091e7-115">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="091e7-115">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="091e7-116">Nome del file o della directory in cui il metodo **CopyEx** non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="091e7-116">Name of the file or directory where the **CopyEx** method failed.</span></span> <span data-ttu-id="091e7-117">Questo parametro sarà **null** se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="091e7-117">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="091e7-118">*StartFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="091e7-118">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="091e7-119">Denomina il file o la directory figlio da utilizzare come punto di partenza per **CopyEx**.</span><span class="sxs-lookup"><span data-stu-id="091e7-119">Names the child file or directory to use as a starting point for **CopyEx**.</span></span> <span data-ttu-id="091e7-120">Il parametro *StartFileName* è in genere il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="091e7-120">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="091e7-121">Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificata nella chiamata **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="091e7-121">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="091e7-122">Se si usa *StartFileName* , è necessario impostare *ricorsivo* su true.</span><span class="sxs-lookup"><span data-stu-id="091e7-122">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="091e7-123">*Ricorsivo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="091e7-123">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="091e7-124">Se **true**, i file e le directory vengono copiati in modo ricorsivo all'interno della directory specificata dall'istanza [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="091e7-124">If **true**, files and directories will be copied recursively within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="091e7-125">Per le istanze di file, il parametro di input *ricorsivo* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="091e7-125">For file instances, the *Recursive* input parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="091e7-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="091e7-126">Return value</span></span>

<span data-ttu-id="091e7-127">Restituisce un valore pari a 0 (zero) se il file è stato copiato correttamente e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="091e7-127">Returns a value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="091e7-128">**0**</span><span class="sxs-lookup"><span data-stu-id="091e7-128">**0**</span></span>
</dt> <dd>

<span data-ttu-id="091e7-129">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="091e7-129">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="091e7-130">**2**</span><span class="sxs-lookup"><span data-stu-id="091e7-130">**2**</span></span>
</dt> <dd>

<span data-ttu-id="091e7-131">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="091e7-131">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="091e7-132">**8**</span><span class="sxs-lookup"><span data-stu-id="091e7-132">**8**</span></span>
</dt> <dd>

<span data-ttu-id="091e7-133">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="091e7-133">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="091e7-134">**9**</span><span class="sxs-lookup"><span data-stu-id="091e7-134">**9**</span></span>
</dt> <dd>

<span data-ttu-id="091e7-135">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="091e7-135">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="091e7-136">**10**</span><span class="sxs-lookup"><span data-stu-id="091e7-136">**10**</span></span>
</dt> <dd>

<span data-ttu-id="091e7-137">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="091e7-137">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="091e7-138">**11**</span><span class="sxs-lookup"><span data-stu-id="091e7-138">**11**</span></span>
</dt> <dd>

<span data-ttu-id="091e7-139">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="091e7-139">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="091e7-140">**12**</span><span class="sxs-lookup"><span data-stu-id="091e7-140">**12**</span></span>
</dt> <dd>

<span data-ttu-id="091e7-141">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="091e7-141">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="091e7-142">**13**</span><span class="sxs-lookup"><span data-stu-id="091e7-142">**13**</span></span>
</dt> <dd>

<span data-ttu-id="091e7-143">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="091e7-143">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="091e7-144">**14**</span><span class="sxs-lookup"><span data-stu-id="091e7-144">**14**</span></span>
</dt> <dd>

<span data-ttu-id="091e7-145">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="091e7-145">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="091e7-146">**15**</span><span class="sxs-lookup"><span data-stu-id="091e7-146">**15**</span></span>
</dt> <dd>

<span data-ttu-id="091e7-147">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="091e7-147">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="091e7-148">**16**</span><span class="sxs-lookup"><span data-stu-id="091e7-148">**16**</span></span>
</dt> <dd>

<span data-ttu-id="091e7-149">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="091e7-149">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="091e7-150">**17**</span><span class="sxs-lookup"><span data-stu-id="091e7-150">**17**</span></span>
</dt> <dd>

<span data-ttu-id="091e7-151">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="091e7-151">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="091e7-152">**21**</span><span class="sxs-lookup"><span data-stu-id="091e7-152">**21**</span></span>
</dt> <dd>

<span data-ttu-id="091e7-153">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="091e7-153">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="091e7-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="091e7-154">Requirements</span></span>



| <span data-ttu-id="091e7-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="091e7-155">Requirement</span></span> | <span data-ttu-id="091e7-156">Valore</span><span class="sxs-lookup"><span data-stu-id="091e7-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="091e7-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="091e7-157">Minimum supported client</span></span><br/> | <span data-ttu-id="091e7-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="091e7-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="091e7-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="091e7-159">Minimum supported server</span></span><br/> | <span data-ttu-id="091e7-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="091e7-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="091e7-161">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="091e7-161">Namespace</span></span><br/>                | <span data-ttu-id="091e7-162">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="091e7-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="091e7-163">MOF</span><span class="sxs-lookup"><span data-stu-id="091e7-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="091e7-164"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="091e7-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="091e7-165">DLL</span><span class="sxs-lookup"><span data-stu-id="091e7-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="091e7-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="091e7-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="091e7-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="091e7-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="091e7-168">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="091e7-168">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="091e7-169">**\_Directory Win32**</span><span class="sxs-lookup"><span data-stu-id="091e7-169">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

