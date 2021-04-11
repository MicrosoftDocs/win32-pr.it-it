---
description: Decomprime il file di voce o directory della directory logica specificato nel percorso dell'oggetto.
ms.assetid: dd39aae3-7c88-48fc-93ed-5225d2f1491c
ms.tgt_platform: multiple
title: Metodo Decompress della classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c46a6bb90d43c1b793350bb96822a1aaed8dd9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127511"
---
# <a name="uncompress-method-of-the-win32_directory-class"></a><span data-ttu-id="28005-103">Metodo Decompress della classe di \_ directory Win32</span><span class="sxs-lookup"><span data-stu-id="28005-103">Uncompress method of the Win32\_Directory class</span></span>

<span data-ttu-id="28005-104">Il metodo di **decompressione** [WMI della classe](/windows/desktop/WmiSdk/retrieving-a-class) decomprime il file di voce o la directory della directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="28005-104">The **Uncompress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical directory entry file (or directory) specified in the object path.</span></span>

<span data-ttu-id="28005-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="28005-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="28005-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="28005-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="28005-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="28005-107">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="28005-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="28005-108">Parameters</span></span>

<span data-ttu-id="28005-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="28005-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="28005-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="28005-110">Return value</span></span>

<span data-ttu-id="28005-111">Restituisce un valore intero pari a 0 (zero) se il file è stato decompresso correttamente e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="28005-111">Returns an integer value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="28005-112">**0**</span><span class="sxs-lookup"><span data-stu-id="28005-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="28005-113">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="28005-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="28005-114">**2**</span><span class="sxs-lookup"><span data-stu-id="28005-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="28005-115">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="28005-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="28005-116">**8**</span><span class="sxs-lookup"><span data-stu-id="28005-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="28005-117">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="28005-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="28005-118">**9**</span><span class="sxs-lookup"><span data-stu-id="28005-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="28005-119">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="28005-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="28005-120">**10**</span><span class="sxs-lookup"><span data-stu-id="28005-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="28005-121">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="28005-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="28005-122">**11**</span><span class="sxs-lookup"><span data-stu-id="28005-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="28005-123">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="28005-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="28005-124">**12**</span><span class="sxs-lookup"><span data-stu-id="28005-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="28005-125">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="28005-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="28005-126">**13**</span><span class="sxs-lookup"><span data-stu-id="28005-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="28005-127">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="28005-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="28005-128">**14**</span><span class="sxs-lookup"><span data-stu-id="28005-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="28005-129">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="28005-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="28005-130">**15**</span><span class="sxs-lookup"><span data-stu-id="28005-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="28005-131">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="28005-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="28005-132">**16**</span><span class="sxs-lookup"><span data-stu-id="28005-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="28005-133">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="28005-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="28005-134">**17**</span><span class="sxs-lookup"><span data-stu-id="28005-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="28005-135">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="28005-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="28005-136">**21**</span><span class="sxs-lookup"><span data-stu-id="28005-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="28005-137">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="28005-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="28005-138">Esempio</span><span class="sxs-lookup"><span data-stu-id="28005-138">Examples</span></span>

<span data-ttu-id="28005-139">L'esempio VBScript seguente decomprime la cartella c: \\ Scripts.</span><span class="sxs-lookup"><span data-stu-id="28005-139">The following VBScript sample uncompresses the folder c:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Uncompress
 Wscript.Echo errResults
Next
```



## <a name="requirements"></a><span data-ttu-id="28005-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28005-140">Requirements</span></span>



| <span data-ttu-id="28005-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="28005-141">Requirement</span></span> | <span data-ttu-id="28005-142">Valore</span><span class="sxs-lookup"><span data-stu-id="28005-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28005-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28005-143">Minimum supported client</span></span><br/> | <span data-ttu-id="28005-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="28005-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="28005-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28005-145">Minimum supported server</span></span><br/> | <span data-ttu-id="28005-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28005-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="28005-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="28005-147">Namespace</span></span><br/>                | <span data-ttu-id="28005-148">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="28005-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="28005-149">MOF</span><span class="sxs-lookup"><span data-stu-id="28005-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28005-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="28005-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="28005-151">DLL</span><span class="sxs-lookup"><span data-stu-id="28005-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28005-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28005-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28005-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28005-153">See also</span></span>

<dl> <dt>

<span data-ttu-id="28005-154">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="28005-154">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="28005-155">**\_Directory Win32**</span><span class="sxs-lookup"><span data-stu-id="28005-155">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> <dt>

[<span data-ttu-id="28005-156">**Comprimere**</span><span class="sxs-lookup"><span data-stu-id="28005-156">**Compress**</span></span>](compress-method-in-class-win32-directory.md)
</dt> </dl>

 

