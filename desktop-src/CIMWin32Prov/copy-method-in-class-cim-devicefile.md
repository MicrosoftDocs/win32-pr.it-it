---
description: Il metodo Copy copia il file logico o la directory specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.
ms.assetid: 6c1c6172-80a2-4779-903a-935f8c7091a5
ms.tgt_platform: multiple
title: Metodo Copy della classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: dc8bb7878f4967dbc58adf6163c92c0d2bd67713
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877873"
---
# <a name="copy-method-of-the-cim_devicefile-class"></a><span data-ttu-id="201e1-103">Metodo Copy della classe CIM \_ DeviceFile</span><span class="sxs-lookup"><span data-stu-id="201e1-103">Copy method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="201e1-104">Il metodo **Copy** copia il file logico o la directory specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.</span><span class="sxs-lookup"><span data-stu-id="201e1-104">The **Copy** method copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="201e1-105">Una copia non è supportata se richiede la sovrascrittura di un file logico esistente.</span><span class="sxs-lookup"><span data-stu-id="201e1-105">A copy is not supported if it requires overwriting an existing logical file.</span></span> <span data-ttu-id="201e1-106">Questo metodo viene ereditato da [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="201e1-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="201e1-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="201e1-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="201e1-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="201e1-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="201e1-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="201e1-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="201e1-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="201e1-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="201e1-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="201e1-111">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="201e1-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="201e1-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="201e1-113">*Nome file* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="201e1-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="201e1-114">Nome completo della copia del file di destinazione (o della directory).</span><span class="sxs-lookup"><span data-stu-id="201e1-114">Fully qualified name of the destination file (or directory) copy.</span></span>

<span data-ttu-id="201e1-115">Esempio: "c: \\ temp \\ NewDirectory"</span><span class="sxs-lookup"><span data-stu-id="201e1-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="201e1-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="201e1-116">Return value</span></span>

<span data-ttu-id="201e1-117">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="201e1-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="201e1-118">**0**</span><span class="sxs-lookup"><span data-stu-id="201e1-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="201e1-119">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="201e1-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="201e1-120">**2**</span><span class="sxs-lookup"><span data-stu-id="201e1-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="201e1-121">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="201e1-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="201e1-122">**8**</span><span class="sxs-lookup"><span data-stu-id="201e1-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="201e1-123">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="201e1-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="201e1-124">**9**</span><span class="sxs-lookup"><span data-stu-id="201e1-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="201e1-125">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="201e1-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="201e1-126">**10**</span><span class="sxs-lookup"><span data-stu-id="201e1-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="201e1-127">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="201e1-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="201e1-128">**11**</span><span class="sxs-lookup"><span data-stu-id="201e1-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="201e1-129">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="201e1-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="201e1-130">**12**</span><span class="sxs-lookup"><span data-stu-id="201e1-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="201e1-131">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="201e1-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="201e1-132">**13**</span><span class="sxs-lookup"><span data-stu-id="201e1-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="201e1-133">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="201e1-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="201e1-134">**14**</span><span class="sxs-lookup"><span data-stu-id="201e1-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="201e1-135">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="201e1-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="201e1-136">**15**</span><span class="sxs-lookup"><span data-stu-id="201e1-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="201e1-137">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="201e1-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="201e1-138">**16**</span><span class="sxs-lookup"><span data-stu-id="201e1-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="201e1-139">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="201e1-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="201e1-140">**17**</span><span class="sxs-lookup"><span data-stu-id="201e1-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="201e1-141">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="201e1-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="201e1-142">**21**</span><span class="sxs-lookup"><span data-stu-id="201e1-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="201e1-143">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="201e1-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="201e1-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="201e1-144">Remarks</span></span>

<span data-ttu-id="201e1-145">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="201e1-145">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="201e1-146">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="201e1-146">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="201e1-147">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="201e1-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="201e1-148">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="201e1-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="201e1-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="201e1-149">Requirements</span></span>



| <span data-ttu-id="201e1-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="201e1-150">Requirement</span></span> | <span data-ttu-id="201e1-151">Valore</span><span class="sxs-lookup"><span data-stu-id="201e1-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="201e1-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="201e1-152">Minimum supported client</span></span><br/> | <span data-ttu-id="201e1-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="201e1-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="201e1-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="201e1-154">Minimum supported server</span></span><br/> | <span data-ttu-id="201e1-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="201e1-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="201e1-156">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="201e1-156">Namespace</span></span><br/>                | <span data-ttu-id="201e1-157">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="201e1-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="201e1-158">MOF</span><span class="sxs-lookup"><span data-stu-id="201e1-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="201e1-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="201e1-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="201e1-160">DLL</span><span class="sxs-lookup"><span data-stu-id="201e1-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="201e1-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="201e1-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="201e1-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="201e1-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="201e1-163">\_DEVICEFILE CIM</span><span class="sxs-lookup"><span data-stu-id="201e1-163">CIM\_DeviceFile</span></span>](copy-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="201e1-164">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="201e1-164">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

