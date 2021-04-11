---
description: Il metodo Copy copia il file logico o la directory specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.
ms.assetid: 71481cc8-9052-4c62-9c26-6887ea646ee1
ms.tgt_platform: multiple
title: Metodo Copy della classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 02bca61e559cea9ee56b9d36b28d13c33e423f9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126927"
---
# <a name="copy-method-of-the-cim_directory-class"></a><span data-ttu-id="7f6c3-103">Metodo Copy della classe di \_ directory CIM</span><span class="sxs-lookup"><span data-stu-id="7f6c3-103">Copy method of the CIM\_Directory class</span></span>

<span data-ttu-id="7f6c3-104">Il metodo **Copy** copia il file logico o la directory specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.</span><span class="sxs-lookup"><span data-stu-id="7f6c3-104">The **Copy** method copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="7f6c3-105">Una copia non è supportata se è necessario sovrascrivere un file logico esistente.</span><span class="sxs-lookup"><span data-stu-id="7f6c3-105">A copy is not supported if overwriting an existing logical file is required.</span></span> <span data-ttu-id="7f6c3-106">Questo metodo viene ereditato da [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="7f6c3-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7f6c3-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="7f6c3-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7f6c3-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7f6c3-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7f6c3-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="7f6c3-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7f6c3-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7f6c3-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7f6c3-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f6c3-111">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="7f6c3-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="7f6c3-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f6c3-113">*Nome file* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f6c3-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f6c3-114">Nome completo della copia del file o della directory di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7f6c3-114">Fully qualified name of the copy of the destination file (or directory).</span></span>

<span data-ttu-id="7f6c3-115">Esempio: "c: \\ temp \\ NewDirectory"</span><span class="sxs-lookup"><span data-stu-id="7f6c3-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f6c3-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7f6c3-116">Return value</span></span>

<span data-ttu-id="7f6c3-117">Restituisce un valore pari a 0 in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="7f6c3-117">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="7f6c3-118">**0**</span><span class="sxs-lookup"><span data-stu-id="7f6c3-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="7f6c3-119">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="7f6c3-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="7f6c3-120">**2**</span><span class="sxs-lookup"><span data-stu-id="7f6c3-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="7f6c3-121">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="7f6c3-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="7f6c3-122">**8**</span><span class="sxs-lookup"><span data-stu-id="7f6c3-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="7f6c3-123">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="7f6c3-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="7f6c3-124">**9**</span><span class="sxs-lookup"><span data-stu-id="7f6c3-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="7f6c3-125">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="7f6c3-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="7f6c3-126">**10**</span><span class="sxs-lookup"><span data-stu-id="7f6c3-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="7f6c3-127">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="7f6c3-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="7f6c3-128">**11**</span><span class="sxs-lookup"><span data-stu-id="7f6c3-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="7f6c3-129">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="7f6c3-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="7f6c3-130">**12**</span><span class="sxs-lookup"><span data-stu-id="7f6c3-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="7f6c3-131">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="7f6c3-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="7f6c3-132">**13**</span><span class="sxs-lookup"><span data-stu-id="7f6c3-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="7f6c3-133">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="7f6c3-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="7f6c3-134">**14**</span><span class="sxs-lookup"><span data-stu-id="7f6c3-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="7f6c3-135">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="7f6c3-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="7f6c3-136">**15**</span><span class="sxs-lookup"><span data-stu-id="7f6c3-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="7f6c3-137">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="7f6c3-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="7f6c3-138">**16**</span><span class="sxs-lookup"><span data-stu-id="7f6c3-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="7f6c3-139">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="7f6c3-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="7f6c3-140">**17**</span><span class="sxs-lookup"><span data-stu-id="7f6c3-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="7f6c3-141">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="7f6c3-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="7f6c3-142">**21**</span><span class="sxs-lookup"><span data-stu-id="7f6c3-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="7f6c3-143">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="7f6c3-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f6c3-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f6c3-144">Remarks</span></span>

<span data-ttu-id="7f6c3-145">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="7f6c3-145">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="7f6c3-146">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="7f6c3-146">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="7f6c3-147">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="7f6c3-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7f6c3-148">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="7f6c3-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f6c3-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f6c3-149">Requirements</span></span>



| <span data-ttu-id="7f6c3-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f6c3-150">Requirement</span></span> | <span data-ttu-id="7f6c3-151">Valore</span><span class="sxs-lookup"><span data-stu-id="7f6c3-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f6c3-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f6c3-152">Minimum supported client</span></span><br/> | <span data-ttu-id="7f6c3-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7f6c3-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7f6c3-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f6c3-154">Minimum supported server</span></span><br/> | <span data-ttu-id="7f6c3-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f6c3-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7f6c3-156">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7f6c3-156">Namespace</span></span><br/>                | <span data-ttu-id="7f6c3-157">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="7f6c3-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7f6c3-158">MOF</span><span class="sxs-lookup"><span data-stu-id="7f6c3-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f6c3-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7f6c3-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f6c3-160">DLL</span><span class="sxs-lookup"><span data-stu-id="7f6c3-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f6c3-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f6c3-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f6c3-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f6c3-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f6c3-163">\_Directory CIM</span><span class="sxs-lookup"><span data-stu-id="7f6c3-163">CIM\_Directory</span></span>](copy-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="7f6c3-164">**\_Directory CIM**</span><span class="sxs-lookup"><span data-stu-id="7f6c3-164">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

