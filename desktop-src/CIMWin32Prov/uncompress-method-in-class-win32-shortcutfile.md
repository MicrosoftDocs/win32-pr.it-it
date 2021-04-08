---
description: Decomprime il file di collegamento logico (o directory) specificato nel percorso dell'oggetto.
ms.assetid: e120391a-3839-4f8c-aca3-473d7f8b30bf
ms.tgt_platform: multiple
title: Metodo Decompress della classe Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 48267f519dce9ae5d78581050255bd8e8b02222c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748943"
---
# <a name="uncompress-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="07347-103">Metodo Decompress della classe Win32 \_ ShortcutFile</span><span class="sxs-lookup"><span data-stu-id="07347-103">Uncompress method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="07347-104">Il metodo di **decompressione** [WMI della classe](/windows/desktop/WmiSdk/retrieving-a-class) decomprime il file di collegamento logico (o directory) specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="07347-104">The **Uncompress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical shortcut file (or directory) specified in the object path.</span></span>

<span data-ttu-id="07347-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="07347-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="07347-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="07347-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="07347-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07347-107">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="07347-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="07347-108">Parameters</span></span>

<span data-ttu-id="07347-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="07347-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="07347-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07347-110">Return value</span></span>

<span data-ttu-id="07347-111">Restituisce un valore pari a 0 (zero) se il file è stato decompresso correttamente e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="07347-111">Returns a value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="07347-112">**0**</span><span class="sxs-lookup"><span data-stu-id="07347-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="07347-113">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="07347-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="07347-114">**2**</span><span class="sxs-lookup"><span data-stu-id="07347-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="07347-115">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="07347-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="07347-116">**8**</span><span class="sxs-lookup"><span data-stu-id="07347-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="07347-117">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="07347-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="07347-118">**9**</span><span class="sxs-lookup"><span data-stu-id="07347-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="07347-119">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="07347-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="07347-120">**10**</span><span class="sxs-lookup"><span data-stu-id="07347-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="07347-121">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="07347-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="07347-122">**11**</span><span class="sxs-lookup"><span data-stu-id="07347-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="07347-123">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="07347-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="07347-124">**12**</span><span class="sxs-lookup"><span data-stu-id="07347-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="07347-125">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="07347-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="07347-126">**13**</span><span class="sxs-lookup"><span data-stu-id="07347-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="07347-127">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="07347-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="07347-128">**14**</span><span class="sxs-lookup"><span data-stu-id="07347-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="07347-129">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="07347-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="07347-130">**15**</span><span class="sxs-lookup"><span data-stu-id="07347-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="07347-131">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="07347-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="07347-132">**16**</span><span class="sxs-lookup"><span data-stu-id="07347-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="07347-133">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="07347-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="07347-134">**17**</span><span class="sxs-lookup"><span data-stu-id="07347-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="07347-135">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="07347-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="07347-136">**21**</span><span class="sxs-lookup"><span data-stu-id="07347-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="07347-137">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="07347-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07347-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07347-138">Requirements</span></span>



| <span data-ttu-id="07347-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="07347-139">Requirement</span></span> | <span data-ttu-id="07347-140">Valore</span><span class="sxs-lookup"><span data-stu-id="07347-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07347-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07347-141">Minimum supported client</span></span><br/> | <span data-ttu-id="07347-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07347-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="07347-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07347-143">Minimum supported server</span></span><br/> | <span data-ttu-id="07347-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07347-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="07347-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="07347-145">Namespace</span></span><br/>                | <span data-ttu-id="07347-146">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="07347-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="07347-147">MOF</span><span class="sxs-lookup"><span data-stu-id="07347-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07347-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="07347-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="07347-149">DLL</span><span class="sxs-lookup"><span data-stu-id="07347-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07347-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07347-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07347-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07347-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="07347-152">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="07347-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="07347-153">**\_ShortcutFile Win32**</span><span class="sxs-lookup"><span data-stu-id="07347-153">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

