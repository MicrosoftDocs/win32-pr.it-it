---
description: Comprime il file di voce o la directory della directory logica specificata nel percorso dell'oggetto (questo metodo è una versione estesa del metodo Compress).
ms.assetid: 6b6e559c-4ca6-49d4-b255-5e1511fdf2e2
ms.tgt_platform: multiple
title: Metodo CompressEx della classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3ee300919efa388d27ae9d594bc2b6c27def88e6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304520"
---
# <a name="compressex-method-of-the-win32_directory-class"></a><span data-ttu-id="88757-103">Metodo CompressEx della classe di \_ directory Win32</span><span class="sxs-lookup"><span data-stu-id="88757-103">CompressEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="88757-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CompressEx** comprime il file di voce o la directory della directory logica specificata nel percorso dell'oggetto (questo metodo è una versione estesa del metodo [**Compress**](compress-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="88757-104">The **CompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical directory entry file (or directory) specified in the object path (this method is an extended version of the [**Compress**](compress-method-in-class-win32-directory.md) method).</span></span>

<span data-ttu-id="88757-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="88757-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="88757-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="88757-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="88757-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88757-107">Syntax</span></span>


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="88757-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="88757-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88757-109">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="88757-109">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88757-110">Nome del file o della directory in cui il metodo **CompressEx** non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="88757-110">Name of the file or directory where the **CompressEx** method failed.</span></span> <span data-ttu-id="88757-111">Questo parametro sarà **null** se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="88757-111">This parameter will be **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="88757-112">*StartFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="88757-112">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="88757-113">Denomina il file o la directory figlio da utilizzare come punto di partenza per **CompressEx**.</span><span class="sxs-lookup"><span data-stu-id="88757-113">Names the child file or directory to use as a starting point for **CompressEx**.</span></span> <span data-ttu-id="88757-114">Il parametro *StartFileName* è in genere il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="88757-114">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="88757-115">Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificata nella chiamata **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="88757-115">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="88757-116">Se si usa *StartFileName* , è necessario impostare *ricorsivo* su true.</span><span class="sxs-lookup"><span data-stu-id="88757-116">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="88757-117">*Ricorsivo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="88757-117">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="88757-118">Se **true**, la modifica della proprietà verrà applicata in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="88757-118">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="88757-119">Per le istanze di file, il parametro di input *ricorsivo* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="88757-119">For file instances, the *Recursive* input parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88757-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88757-120">Return value</span></span>

<span data-ttu-id="88757-121">Restituisce un valore pari a 0 (zero) se il file è stato compresso correttamente e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="88757-121">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="88757-122">**0**</span><span class="sxs-lookup"><span data-stu-id="88757-122">**0**</span></span>
</dt> <dd>

<span data-ttu-id="88757-123">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="88757-123">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="88757-124">**2**</span><span class="sxs-lookup"><span data-stu-id="88757-124">**2**</span></span>
</dt> <dd>

<span data-ttu-id="88757-125">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="88757-125">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="88757-126">**8**</span><span class="sxs-lookup"><span data-stu-id="88757-126">**8**</span></span>
</dt> <dd>

<span data-ttu-id="88757-127">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="88757-127">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="88757-128">**9**</span><span class="sxs-lookup"><span data-stu-id="88757-128">**9**</span></span>
</dt> <dd>

<span data-ttu-id="88757-129">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="88757-129">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="88757-130">**10**</span><span class="sxs-lookup"><span data-stu-id="88757-130">**10**</span></span>
</dt> <dd>

<span data-ttu-id="88757-131">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="88757-131">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="88757-132">**11**</span><span class="sxs-lookup"><span data-stu-id="88757-132">**11**</span></span>
</dt> <dd>

<span data-ttu-id="88757-133">Il file system non è un NTFS.</span><span class="sxs-lookup"><span data-stu-id="88757-133">The file system is not an NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="88757-134">**12**</span><span class="sxs-lookup"><span data-stu-id="88757-134">**12**</span></span>
</dt> <dd>

<span data-ttu-id="88757-135">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="88757-135">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="88757-136">**13**</span><span class="sxs-lookup"><span data-stu-id="88757-136">**13**</span></span>
</dt> <dd>

<span data-ttu-id="88757-137">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="88757-137">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="88757-138">**14**</span><span class="sxs-lookup"><span data-stu-id="88757-138">**14**</span></span>
</dt> <dd>

<span data-ttu-id="88757-139">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="88757-139">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="88757-140">**15**</span><span class="sxs-lookup"><span data-stu-id="88757-140">**15**</span></span>
</dt> <dd>

<span data-ttu-id="88757-141">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="88757-141">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="88757-142">**16**</span><span class="sxs-lookup"><span data-stu-id="88757-142">**16**</span></span>
</dt> <dd>

<span data-ttu-id="88757-143">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="88757-143">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="88757-144">**17**</span><span class="sxs-lookup"><span data-stu-id="88757-144">**17**</span></span>
</dt> <dd>

<span data-ttu-id="88757-145">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="88757-145">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="88757-146">**21**</span><span class="sxs-lookup"><span data-stu-id="88757-146">**21**</span></span>
</dt> <dd>

<span data-ttu-id="88757-147">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="88757-147">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88757-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88757-148">Requirements</span></span>



| <span data-ttu-id="88757-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="88757-149">Requirement</span></span> | <span data-ttu-id="88757-150">Valore</span><span class="sxs-lookup"><span data-stu-id="88757-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88757-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88757-151">Minimum supported client</span></span><br/> | <span data-ttu-id="88757-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88757-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="88757-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88757-153">Minimum supported server</span></span><br/> | <span data-ttu-id="88757-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88757-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="88757-155">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="88757-155">Namespace</span></span><br/>                | <span data-ttu-id="88757-156">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="88757-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="88757-157">MOF</span><span class="sxs-lookup"><span data-stu-id="88757-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88757-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88757-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="88757-159">DLL</span><span class="sxs-lookup"><span data-stu-id="88757-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88757-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88757-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88757-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88757-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="88757-162">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="88757-162">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="88757-163">**\_Directory Win32**</span><span class="sxs-lookup"><span data-stu-id="88757-163">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

