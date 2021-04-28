---
description: "Metodo Delete della classe CIM_DeviceFile: il metodo Delete elimina il file logico (o la directory) specificato nel percorso dell'oggetto. Questo metodo viene ereditato da CIM \\_ LogicalFile."
ms.assetid: 490d0578-a545-423b-9640-ec09f4ef8d96
ms.tgt_platform: multiple
title: Metodo Delete della classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e96ba9837252158510c306a622df86c09bbfd96
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089629"
---
# <a name="delete-method-of-the-cim_devicefile-class"></a><span data-ttu-id="ec44c-104">Metodo Delete della classe CIM \_ DeviceFile</span><span class="sxs-lookup"><span data-stu-id="ec44c-104">Delete method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="ec44c-105">Il **metodo Delete** elimina il file logico (o la directory) specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ec44c-105">The **Delete** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="ec44c-106">Questo metodo viene ereditato da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ec44c-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ec44c-107">Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model) sono le classi padre su cui vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="ec44c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ec44c-108">WMI attualmente supporta solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ec44c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ec44c-109">Questo argomento usa Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="ec44c-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ec44c-110">Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ec44c-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ec44c-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec44c-111">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="ec44c-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="ec44c-112">Parameters</span></span>

<span data-ttu-id="ec44c-113">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ec44c-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ec44c-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ec44c-114">Return value</span></span>

<span data-ttu-id="ec44c-115">Restituisce il valore 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="ec44c-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="ec44c-116">**0**</span><span class="sxs-lookup"><span data-stu-id="ec44c-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="ec44c-117">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="ec44c-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="ec44c-118">**2**</span><span class="sxs-lookup"><span data-stu-id="ec44c-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="ec44c-119">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="ec44c-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="ec44c-120">**8**</span><span class="sxs-lookup"><span data-stu-id="ec44c-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="ec44c-121">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="ec44c-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="ec44c-122">**9**</span><span class="sxs-lookup"><span data-stu-id="ec44c-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="ec44c-123">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="ec44c-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="ec44c-124">**10**</span><span class="sxs-lookup"><span data-stu-id="ec44c-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="ec44c-125">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="ec44c-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="ec44c-126">**11**</span><span class="sxs-lookup"><span data-stu-id="ec44c-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="ec44c-127">File system non NTFS.</span><span class="sxs-lookup"><span data-stu-id="ec44c-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="ec44c-128">**12**</span><span class="sxs-lookup"><span data-stu-id="ec44c-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="ec44c-129">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="ec44c-129">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="ec44c-130">**13**</span><span class="sxs-lookup"><span data-stu-id="ec44c-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="ec44c-131">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="ec44c-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="ec44c-132">**14**</span><span class="sxs-lookup"><span data-stu-id="ec44c-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="ec44c-133">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="ec44c-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="ec44c-134">**15**</span><span class="sxs-lookup"><span data-stu-id="ec44c-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="ec44c-135">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="ec44c-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="ec44c-136">**16**</span><span class="sxs-lookup"><span data-stu-id="ec44c-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="ec44c-137">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="ec44c-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="ec44c-138">**17**</span><span class="sxs-lookup"><span data-stu-id="ec44c-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="ec44c-139">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="ec44c-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="ec44c-140">**21**</span><span class="sxs-lookup"><span data-stu-id="ec44c-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="ec44c-141">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="ec44c-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec44c-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec44c-142">Remarks</span></span>

<span data-ttu-id="ec44c-143">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="ec44c-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="ec44c-144">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="ec44c-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="ec44c-145">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="ec44c-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ec44c-146">Microsoft potrebbe aver apportato modifiche per correggere errori secondari, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="ec44c-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec44c-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec44c-147">Requirements</span></span>



| <span data-ttu-id="ec44c-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec44c-148">Requirement</span></span> | <span data-ttu-id="ec44c-149">Valore</span><span class="sxs-lookup"><span data-stu-id="ec44c-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec44c-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec44c-150">Minimum supported client</span></span><br/> | <span data-ttu-id="ec44c-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ec44c-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ec44c-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec44c-152">Minimum supported server</span></span><br/> | <span data-ttu-id="ec44c-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec44c-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ec44c-154">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ec44c-154">Namespace</span></span><br/>                | <span data-ttu-id="ec44c-155">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ec44c-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ec44c-156">MOF</span><span class="sxs-lookup"><span data-stu-id="ec44c-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec44c-157"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="ec44c-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ec44c-158">DLL</span><span class="sxs-lookup"><span data-stu-id="ec44c-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec44c-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec44c-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec44c-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec44c-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec44c-161">CIM \_ DeviceFile</span><span class="sxs-lookup"><span data-stu-id="ec44c-161">CIM\_DeviceFile</span></span>](delete-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="ec44c-162">**CIM \_ DeviceFile**</span><span class="sxs-lookup"><span data-stu-id="ec44c-162">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

