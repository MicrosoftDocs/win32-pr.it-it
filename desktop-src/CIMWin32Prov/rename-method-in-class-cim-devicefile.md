---
description: Rinomina il file del dispositivo o la directory specificata nel percorso dell'oggetto.
ms.assetid: 48c2eab3-c76d-4e4b-927e-dbb17584cccd
ms.tgt_platform: multiple
title: Rinominare il metodo della classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 484d66a1b98ea58b7cb5de25c8f7d15065ce905b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127370"
---
# <a name="rename-method-of-the-cim_devicefile-class"></a><span data-ttu-id="90c6b-103">Rinominare il metodo della \_ classe CIM DeviceFile</span><span class="sxs-lookup"><span data-stu-id="90c6b-103">Rename method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="90c6b-104">Il metodo **Rename Rinomina** il file del dispositivo o la directory specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="90c6b-104">The **Rename** method renames the device file (or directory) specified in the object path.</span></span> <span data-ttu-id="90c6b-105">La ridenominazione non è supportata se la destinazione si trova in un'altra unità o se è necessario sovrascrivere un file logico esistente.</span><span class="sxs-lookup"><span data-stu-id="90c6b-105">Renaming is not supported if the destination is on another drive or overwriting an existing logical file is required.</span></span> <span data-ttu-id="90c6b-106">Questo metodo viene ereditato da [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="90c6b-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="90c6b-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="90c6b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="90c6b-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="90c6b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="90c6b-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="90c6b-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="90c6b-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="90c6b-110">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="90c6b-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="90c6b-111">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="90c6b-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="90c6b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90c6b-113">*Nome file* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90c6b-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90c6b-114">Nome completo del nuovo file (o directory).</span><span class="sxs-lookup"><span data-stu-id="90c6b-114">Fully qualified new name of the file (or directory).</span></span>

<span data-ttu-id="90c6b-115">Esempio: "c: \\ temp \\newfile.txt"</span><span class="sxs-lookup"><span data-stu-id="90c6b-115">Example: "c:\\temp\\newfile.txt"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90c6b-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="90c6b-116">Return value</span></span>

<span data-ttu-id="90c6b-117">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="90c6b-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="90c6b-118">**0**</span><span class="sxs-lookup"><span data-stu-id="90c6b-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="90c6b-119">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="90c6b-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="90c6b-120">**2**</span><span class="sxs-lookup"><span data-stu-id="90c6b-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="90c6b-121">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="90c6b-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="90c6b-122">**8**</span><span class="sxs-lookup"><span data-stu-id="90c6b-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="90c6b-123">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="90c6b-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="90c6b-124">**9**</span><span class="sxs-lookup"><span data-stu-id="90c6b-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="90c6b-125">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="90c6b-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="90c6b-126">**10**</span><span class="sxs-lookup"><span data-stu-id="90c6b-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="90c6b-127">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="90c6b-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="90c6b-128">**11**</span><span class="sxs-lookup"><span data-stu-id="90c6b-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="90c6b-129">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="90c6b-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="90c6b-130">**12**</span><span class="sxs-lookup"><span data-stu-id="90c6b-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="90c6b-131">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="90c6b-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="90c6b-132">**13**</span><span class="sxs-lookup"><span data-stu-id="90c6b-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="90c6b-133">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="90c6b-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="90c6b-134">**14**</span><span class="sxs-lookup"><span data-stu-id="90c6b-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="90c6b-135">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="90c6b-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="90c6b-136">**15**</span><span class="sxs-lookup"><span data-stu-id="90c6b-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="90c6b-137">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="90c6b-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="90c6b-138">**16**</span><span class="sxs-lookup"><span data-stu-id="90c6b-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="90c6b-139">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="90c6b-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="90c6b-140">**17**</span><span class="sxs-lookup"><span data-stu-id="90c6b-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="90c6b-141">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="90c6b-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="90c6b-142">**21**</span><span class="sxs-lookup"><span data-stu-id="90c6b-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="90c6b-143">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="90c6b-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90c6b-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="90c6b-144">Remarks</span></span>

<span data-ttu-id="90c6b-145">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="90c6b-145">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="90c6b-146">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="90c6b-146">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="90c6b-147">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="90c6b-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="90c6b-148">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="90c6b-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="90c6b-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90c6b-149">Requirements</span></span>



| <span data-ttu-id="90c6b-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="90c6b-150">Requirement</span></span> | <span data-ttu-id="90c6b-151">Valore</span><span class="sxs-lookup"><span data-stu-id="90c6b-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90c6b-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90c6b-152">Minimum supported client</span></span><br/> | <span data-ttu-id="90c6b-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="90c6b-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="90c6b-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90c6b-154">Minimum supported server</span></span><br/> | <span data-ttu-id="90c6b-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90c6b-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="90c6b-156">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="90c6b-156">Namespace</span></span><br/>                | <span data-ttu-id="90c6b-157">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="90c6b-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="90c6b-158">MOF</span><span class="sxs-lookup"><span data-stu-id="90c6b-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90c6b-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="90c6b-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="90c6b-160">DLL</span><span class="sxs-lookup"><span data-stu-id="90c6b-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90c6b-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90c6b-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90c6b-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90c6b-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90c6b-163">\_DEVICEFILE CIM</span><span class="sxs-lookup"><span data-stu-id="90c6b-163">CIM\_DeviceFile</span></span>](rename-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="90c6b-164">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="90c6b-164">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

