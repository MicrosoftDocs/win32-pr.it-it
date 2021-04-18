---
description: Rinomina il file logico o la directory specificata nel percorso dell'oggetto. La ridenominazione non è supportata se la destinazione si trova in un'altra unità o se è necessario sovrascrivere un file logico esistente.
ms.assetid: 728737a7-7cb8-4237-be03-16c4dac530b2
ms.tgt_platform: multiple
title: Rinominare il metodo della classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 83429f3a5248b1d3be24832b26bf99213d442ce5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483732"
---
# <a name="rename-method-of-the-cim_directory-class"></a><span data-ttu-id="33486-104">Rinominare il metodo della \_ classe di directory CIM</span><span class="sxs-lookup"><span data-stu-id="33486-104">Rename method of the CIM\_Directory class</span></span>

<span data-ttu-id="33486-105">Il metodo **Rename Rinomina** il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="33486-105">The **Rename** method renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="33486-106">La ridenominazione non è supportata se la destinazione si trova in un'altra unità o se è necessario sovrascrivere un file logico esistente.</span><span class="sxs-lookup"><span data-stu-id="33486-106">Renaming is not supported if the destination is on another drive or overwriting an existing logical file is required.</span></span>

<span data-ttu-id="33486-107">Questo metodo viene ereditato da [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="33486-107">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="33486-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="33486-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="33486-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="33486-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="33486-110">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="33486-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="33486-111">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="33486-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="33486-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="33486-112">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="33486-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="33486-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33486-114">*Nome file* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33486-114">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33486-115">Nome completo del nuovo file (o directory).</span><span class="sxs-lookup"><span data-stu-id="33486-115">Fully qualified new name of the file (or directory).</span></span>

<span data-ttu-id="33486-116">Esempio: "c: \\ temp \\newname.txt"</span><span class="sxs-lookup"><span data-stu-id="33486-116">Example: "c:\\temp\\newname.txt"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33486-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="33486-117">Return value</span></span>

<span data-ttu-id="33486-118">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="33486-118">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="33486-119">**0**</span><span class="sxs-lookup"><span data-stu-id="33486-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="33486-120">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="33486-120">Success.</span></span>

</dd> <dt>

<span data-ttu-id="33486-121">**2**</span><span class="sxs-lookup"><span data-stu-id="33486-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="33486-122">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="33486-122">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="33486-123">**8**</span><span class="sxs-lookup"><span data-stu-id="33486-123">**8**</span></span>
</dt> <dd>

<span data-ttu-id="33486-124">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="33486-124">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="33486-125">**9**</span><span class="sxs-lookup"><span data-stu-id="33486-125">**9**</span></span>
</dt> <dd>

<span data-ttu-id="33486-126">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="33486-126">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="33486-127">**10**</span><span class="sxs-lookup"><span data-stu-id="33486-127">**10**</span></span>
</dt> <dd>

<span data-ttu-id="33486-128">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="33486-128">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="33486-129">**11**</span><span class="sxs-lookup"><span data-stu-id="33486-129">**11**</span></span>
</dt> <dd>

<span data-ttu-id="33486-130">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="33486-130">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="33486-131">**12**</span><span class="sxs-lookup"><span data-stu-id="33486-131">**12**</span></span>
</dt> <dd>

<span data-ttu-id="33486-132">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="33486-132">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="33486-133">**13**</span><span class="sxs-lookup"><span data-stu-id="33486-133">**13**</span></span>
</dt> <dd>

<span data-ttu-id="33486-134">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="33486-134">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="33486-135">**14**</span><span class="sxs-lookup"><span data-stu-id="33486-135">**14**</span></span>
</dt> <dd>

<span data-ttu-id="33486-136">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="33486-136">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="33486-137">**15**</span><span class="sxs-lookup"><span data-stu-id="33486-137">**15**</span></span>
</dt> <dd>

<span data-ttu-id="33486-138">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="33486-138">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="33486-139">**16**</span><span class="sxs-lookup"><span data-stu-id="33486-139">**16**</span></span>
</dt> <dd>

<span data-ttu-id="33486-140">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="33486-140">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="33486-141">**17**</span><span class="sxs-lookup"><span data-stu-id="33486-141">**17**</span></span>
</dt> <dd>

<span data-ttu-id="33486-142">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="33486-142">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="33486-143">**21**</span><span class="sxs-lookup"><span data-stu-id="33486-143">**21**</span></span>
</dt> <dd>

<span data-ttu-id="33486-144">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="33486-144">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33486-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="33486-145">Remarks</span></span>

<span data-ttu-id="33486-146">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="33486-146">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="33486-147">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="33486-147">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="33486-148">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="33486-148">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="33486-149">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="33486-149">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="33486-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33486-150">Requirements</span></span>



| <span data-ttu-id="33486-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="33486-151">Requirement</span></span> | <span data-ttu-id="33486-152">Valore</span><span class="sxs-lookup"><span data-stu-id="33486-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33486-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33486-153">Minimum supported client</span></span><br/> | <span data-ttu-id="33486-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33486-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="33486-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33486-155">Minimum supported server</span></span><br/> | <span data-ttu-id="33486-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33486-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="33486-157">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="33486-157">Namespace</span></span><br/>                | <span data-ttu-id="33486-158">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="33486-158">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="33486-159">MOF</span><span class="sxs-lookup"><span data-stu-id="33486-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33486-160"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33486-160"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="33486-161">DLL</span><span class="sxs-lookup"><span data-stu-id="33486-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33486-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33486-162"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33486-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33486-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33486-164">\_Directory CIM</span><span class="sxs-lookup"><span data-stu-id="33486-164">CIM\_Directory</span></span>](rename-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="33486-165">**\_Directory CIM**</span><span class="sxs-lookup"><span data-stu-id="33486-165">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

