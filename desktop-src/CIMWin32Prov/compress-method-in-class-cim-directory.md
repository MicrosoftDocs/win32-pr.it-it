---
description: Comprime il file di voce o la directory della directory logica specificata nel percorso dell'oggetto. Questo metodo viene ereditato da \_ LOGICALFILE CIM.
ms.assetid: 40aac2f8-4ff6-4e21-9395-5d3d40b39b00
ms.tgt_platform: multiple
title: Metodo Compress della classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f1717e77fdedb0c6b2e218e66f61d67bcef7c1a8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304524"
---
# <a name="compress-method-of-the-cim_directory-class"></a><span data-ttu-id="dd759-104">Metodo Compress della classe di \_ directory CIM</span><span class="sxs-lookup"><span data-stu-id="dd759-104">Compress method of the CIM\_Directory class</span></span>

<span data-ttu-id="dd759-105">Il metodo **Compress comprime** il file di voce o la directory della directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="dd759-105">The **Compress** method compresses the logical directory entry file (or directory) specified in the object path.</span></span> <span data-ttu-id="dd759-106">Questo metodo viene ereditato da [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="dd759-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd759-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="dd759-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dd759-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dd759-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dd759-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="dd759-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="dd759-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="dd759-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="dd759-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd759-111">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="dd759-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="dd759-112">Parameters</span></span>

<span data-ttu-id="dd759-113">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="dd759-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dd759-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dd759-114">Return value</span></span>

<span data-ttu-id="dd759-115">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="dd759-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="dd759-116">**0**</span><span class="sxs-lookup"><span data-stu-id="dd759-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="dd759-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="dd759-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="dd759-118">**2**</span><span class="sxs-lookup"><span data-stu-id="dd759-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="dd759-119">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="dd759-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="dd759-120">**8**</span><span class="sxs-lookup"><span data-stu-id="dd759-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="dd759-121">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="dd759-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="dd759-122">**9**</span><span class="sxs-lookup"><span data-stu-id="dd759-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="dd759-123">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="dd759-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="dd759-124">**10**</span><span class="sxs-lookup"><span data-stu-id="dd759-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="dd759-125">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="dd759-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="dd759-126">**11**</span><span class="sxs-lookup"><span data-stu-id="dd759-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="dd759-127">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="dd759-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="dd759-128">**12**</span><span class="sxs-lookup"><span data-stu-id="dd759-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="dd759-129">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="dd759-129">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="dd759-130">**13**</span><span class="sxs-lookup"><span data-stu-id="dd759-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="dd759-131">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="dd759-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="dd759-132">**14**</span><span class="sxs-lookup"><span data-stu-id="dd759-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="dd759-133">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="dd759-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="dd759-134">**15**</span><span class="sxs-lookup"><span data-stu-id="dd759-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="dd759-135">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="dd759-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="dd759-136">**16**</span><span class="sxs-lookup"><span data-stu-id="dd759-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="dd759-137">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="dd759-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="dd759-138">**17**</span><span class="sxs-lookup"><span data-stu-id="dd759-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="dd759-139">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="dd759-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="dd759-140">**21**</span><span class="sxs-lookup"><span data-stu-id="dd759-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="dd759-141">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="dd759-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd759-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd759-142">Remarks</span></span>

<span data-ttu-id="dd759-143">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="dd759-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="dd759-144">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="dd759-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="dd759-145">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="dd759-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dd759-146">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="dd759-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd759-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd759-147">Requirements</span></span>



| <span data-ttu-id="dd759-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd759-148">Requirement</span></span> | <span data-ttu-id="dd759-149">Valore</span><span class="sxs-lookup"><span data-stu-id="dd759-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd759-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd759-150">Minimum supported client</span></span><br/> | <span data-ttu-id="dd759-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dd759-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dd759-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd759-152">Minimum supported server</span></span><br/> | <span data-ttu-id="dd759-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd759-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dd759-154">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dd759-154">Namespace</span></span><br/>                | <span data-ttu-id="dd759-155">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="dd759-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dd759-156">MOF</span><span class="sxs-lookup"><span data-stu-id="dd759-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd759-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd759-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd759-158">DLL</span><span class="sxs-lookup"><span data-stu-id="dd759-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd759-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd759-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd759-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dd759-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd759-161">\_Directory CIM</span><span class="sxs-lookup"><span data-stu-id="dd759-161">CIM\_Directory</span></span>](compress-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="dd759-162">**\_Directory CIM**</span><span class="sxs-lookup"><span data-stu-id="dd759-162">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

