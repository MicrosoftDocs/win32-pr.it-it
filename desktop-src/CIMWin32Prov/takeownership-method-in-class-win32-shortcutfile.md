---
description: Metodo TakeOwnerShip della classe Win32_ShortcutFile - TakeOwnerShip&\# 8194; Il metodo della classe WMI ottiene la proprietà del file logico specificato nel percorso dell'oggetto.
ms.assetid: 1a8ff156-50b2-4550-abcc-7a6ae0e4630f
ms.tgt_platform: multiple
title: Metodo TakeOwnerShip della Win32_ShortcutFile classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 36364a55276842518480c3d3d37c57c3ae0a06ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085999"
---
# <a name="takeownership-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="a4e13-103">Metodo TakeOwnerShip della classe ShortcutFile Win32 \_</span><span class="sxs-lookup"><span data-stu-id="a4e13-103">TakeOwnerShip method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="a4e13-104">Il metodo della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShip** ottiene la proprietà del file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a4e13-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="a4e13-105">Se il file logico è effettivamente una directory, **TakeOwnerShip** agisce in modo ricorsivo, assumendo la proprietà di tutti i file e le sottodirectory contenuti nella directory.</span><span class="sxs-lookup"><span data-stu-id="a4e13-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="a4e13-106">Questo argomento usa Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="a4e13-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a4e13-107">Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a4e13-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a4e13-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a4e13-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="a4e13-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a4e13-109">Parameters</span></span>

<span data-ttu-id="a4e13-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a4e13-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a4e13-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a4e13-111">Return value</span></span>

<span data-ttu-id="a4e13-112">Restituisce uno dei seguenti valori interi.</span><span class="sxs-lookup"><span data-stu-id="a4e13-112">Returns one of the following integer values.</span></span>

<dl> <dt>

<span data-ttu-id="a4e13-113">**0**</span><span class="sxs-lookup"><span data-stu-id="a4e13-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="a4e13-114">La richiesta ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a4e13-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="a4e13-115">**2**</span><span class="sxs-lookup"><span data-stu-id="a4e13-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="a4e13-116">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="a4e13-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="a4e13-117">**8**</span><span class="sxs-lookup"><span data-stu-id="a4e13-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="a4e13-118">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="a4e13-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="a4e13-119">**9**</span><span class="sxs-lookup"><span data-stu-id="a4e13-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="a4e13-120">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="a4e13-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a4e13-121">**10**</span><span class="sxs-lookup"><span data-stu-id="a4e13-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="a4e13-122">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="a4e13-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="a4e13-123">**11**</span><span class="sxs-lookup"><span data-stu-id="a4e13-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="a4e13-124">Il file system non è NTFS.</span><span class="sxs-lookup"><span data-stu-id="a4e13-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="a4e13-125">**12**</span><span class="sxs-lookup"><span data-stu-id="a4e13-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="a4e13-126">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="a4e13-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="a4e13-127">**13**</span><span class="sxs-lookup"><span data-stu-id="a4e13-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="a4e13-128">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="a4e13-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="a4e13-129">**14**</span><span class="sxs-lookup"><span data-stu-id="a4e13-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="a4e13-130">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="a4e13-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="a4e13-131">**15**</span><span class="sxs-lookup"><span data-stu-id="a4e13-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="a4e13-132">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="a4e13-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="a4e13-133">**16**</span><span class="sxs-lookup"><span data-stu-id="a4e13-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="a4e13-134">Il file iniziale specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="a4e13-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a4e13-135">**17**</span><span class="sxs-lookup"><span data-stu-id="a4e13-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="a4e13-136">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="a4e13-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="a4e13-137">**21**</span><span class="sxs-lookup"><span data-stu-id="a4e13-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="a4e13-138">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="a4e13-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a4e13-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4e13-139">Requirements</span></span>



| <span data-ttu-id="a4e13-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4e13-140">Requirement</span></span> | <span data-ttu-id="a4e13-141">Valore</span><span class="sxs-lookup"><span data-stu-id="a4e13-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4e13-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4e13-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a4e13-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4e13-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a4e13-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4e13-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a4e13-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4e13-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a4e13-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a4e13-146">Namespace</span></span><br/>                | <span data-ttu-id="a4e13-147">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a4e13-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a4e13-148">MOF</span><span class="sxs-lookup"><span data-stu-id="a4e13-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4e13-149"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4e13-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4e13-150">DLL</span><span class="sxs-lookup"><span data-stu-id="a4e13-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4e13-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4e13-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4e13-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4e13-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="a4e13-153">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a4e13-153">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a4e13-154">**Win32 \_ ShortcutFile**</span><span class="sxs-lookup"><span data-stu-id="a4e13-154">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

