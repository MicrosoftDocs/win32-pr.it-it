---
description: Comprime il file di collegamento logico (o directory) specificato nel percorso dell'oggetto.
ms.assetid: ade588a5-4e0c-486b-b187-805fcabbf326
ms.tgt_platform: multiple
title: Metodo Compress della classe Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 490f4d1a76844dc9ebad0449432f06833580d949
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304521"
---
# <a name="compress-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="f9300-103">Metodo Compress della classe Win32 \_ ShortcutFile</span><span class="sxs-lookup"><span data-stu-id="f9300-103">Compress method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="f9300-104">Il metodo **Compress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) comprime il file di collegamento logico (o directory) specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f9300-104">The **Compress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical shortcut file (or directory) specified in the object path.</span></span>

<span data-ttu-id="f9300-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="f9300-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f9300-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f9300-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f9300-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9300-107">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="f9300-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9300-108">Parameters</span></span>

<span data-ttu-id="f9300-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f9300-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f9300-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9300-110">Return value</span></span>

<span data-ttu-id="f9300-111">Restituisce un valore pari a 0 (zero) se il file è stato compresso correttamente e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="f9300-111">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="f9300-112">**0**</span><span class="sxs-lookup"><span data-stu-id="f9300-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="f9300-113">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="f9300-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="f9300-114">**2**</span><span class="sxs-lookup"><span data-stu-id="f9300-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="f9300-115">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="f9300-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="f9300-116">**8**</span><span class="sxs-lookup"><span data-stu-id="f9300-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="f9300-117">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="f9300-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="f9300-118">**9**</span><span class="sxs-lookup"><span data-stu-id="f9300-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="f9300-119">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="f9300-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f9300-120">**10**</span><span class="sxs-lookup"><span data-stu-id="f9300-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="f9300-121">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="f9300-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f9300-122">**11**</span><span class="sxs-lookup"><span data-stu-id="f9300-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="f9300-123">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="f9300-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="f9300-124">**12**</span><span class="sxs-lookup"><span data-stu-id="f9300-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="f9300-125">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="f9300-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="f9300-126">**13**</span><span class="sxs-lookup"><span data-stu-id="f9300-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="f9300-127">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="f9300-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="f9300-128">**14**</span><span class="sxs-lookup"><span data-stu-id="f9300-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="f9300-129">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="f9300-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="f9300-130">**15**</span><span class="sxs-lookup"><span data-stu-id="f9300-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="f9300-131">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="f9300-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="f9300-132">**16**</span><span class="sxs-lookup"><span data-stu-id="f9300-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="f9300-133">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="f9300-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f9300-134">**17**</span><span class="sxs-lookup"><span data-stu-id="f9300-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="f9300-135">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="f9300-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="f9300-136">**21**</span><span class="sxs-lookup"><span data-stu-id="f9300-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="f9300-137">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="f9300-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9300-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9300-138">Requirements</span></span>



| <span data-ttu-id="f9300-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9300-139">Requirement</span></span> | <span data-ttu-id="f9300-140">Valore</span><span class="sxs-lookup"><span data-stu-id="f9300-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9300-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9300-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f9300-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9300-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f9300-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9300-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f9300-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9300-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f9300-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f9300-145">Namespace</span></span><br/>                | <span data-ttu-id="f9300-146">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f9300-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f9300-147">MOF</span><span class="sxs-lookup"><span data-stu-id="f9300-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9300-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f9300-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9300-149">DLL</span><span class="sxs-lookup"><span data-stu-id="f9300-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9300-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9300-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9300-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9300-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="f9300-152">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f9300-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f9300-153">**\_ShortcutFile Win32**</span><span class="sxs-lookup"><span data-stu-id="f9300-153">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

