---
description: "Metodo Copy della classe CIM_DeviceFile: il metodo Copy copia il file logico (o la directory) specificato nel percorso dell'oggetto nel percorso specificato dal parametro di input."
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
ms.openlocfilehash: 09c6d0f9400a04cc6e5a8ed4bd49ec7075b3c190
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089802"
---
# <a name="copy-method-of-the-cim_devicefile-class"></a><span data-ttu-id="33b29-103">Metodo Copy della classe CIM \_ DeviceFile</span><span class="sxs-lookup"><span data-stu-id="33b29-103">Copy method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="33b29-104">Il **metodo Copy** copia il file logico (o la directory) specificato nel percorso dell'oggetto nel percorso specificato dal parametro di input.</span><span class="sxs-lookup"><span data-stu-id="33b29-104">The **Copy** method copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="33b29-105">Una copia non è supportata se richiede la sovrascrittura di un file logico esistente.</span><span class="sxs-lookup"><span data-stu-id="33b29-105">A copy is not supported if it requires overwriting an existing logical file.</span></span> <span data-ttu-id="33b29-106">Questo metodo viene ereditato da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="33b29-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="33b29-107">Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="33b29-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="33b29-108">WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="33b29-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="33b29-109">Questo argomento usa Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="33b29-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="33b29-110">Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="33b29-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="33b29-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="33b29-111">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="33b29-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="33b29-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33b29-113">*FileName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="33b29-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33b29-114">Nome completo della copia del file o della directory di destinazione.</span><span class="sxs-lookup"><span data-stu-id="33b29-114">Fully qualified name of the destination file (or directory) copy.</span></span>

<span data-ttu-id="33b29-115">Esempio: "c: \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="33b29-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33b29-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="33b29-116">Return value</span></span>

<span data-ttu-id="33b29-117">Restituisce il valore 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="33b29-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="33b29-118">**0**</span><span class="sxs-lookup"><span data-stu-id="33b29-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="33b29-119">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="33b29-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="33b29-120">**2**</span><span class="sxs-lookup"><span data-stu-id="33b29-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="33b29-121">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="33b29-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="33b29-122">**8**</span><span class="sxs-lookup"><span data-stu-id="33b29-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="33b29-123">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="33b29-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="33b29-124">**9**</span><span class="sxs-lookup"><span data-stu-id="33b29-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="33b29-125">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="33b29-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="33b29-126">**10**</span><span class="sxs-lookup"><span data-stu-id="33b29-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="33b29-127">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="33b29-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="33b29-128">**11**</span><span class="sxs-lookup"><span data-stu-id="33b29-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="33b29-129">File system non NTFS.</span><span class="sxs-lookup"><span data-stu-id="33b29-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="33b29-130">**12**</span><span class="sxs-lookup"><span data-stu-id="33b29-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="33b29-131">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="33b29-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="33b29-132">**13**</span><span class="sxs-lookup"><span data-stu-id="33b29-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="33b29-133">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="33b29-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="33b29-134">**14**</span><span class="sxs-lookup"><span data-stu-id="33b29-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="33b29-135">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="33b29-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="33b29-136">**15**</span><span class="sxs-lookup"><span data-stu-id="33b29-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="33b29-137">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="33b29-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="33b29-138">**16**</span><span class="sxs-lookup"><span data-stu-id="33b29-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="33b29-139">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="33b29-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="33b29-140">**17**</span><span class="sxs-lookup"><span data-stu-id="33b29-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="33b29-141">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="33b29-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="33b29-142">**21**</span><span class="sxs-lookup"><span data-stu-id="33b29-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="33b29-143">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="33b29-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33b29-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="33b29-144">Remarks</span></span>

<span data-ttu-id="33b29-145">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="33b29-145">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="33b29-146">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="33b29-146">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="33b29-147">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="33b29-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="33b29-148">Microsoft potrebbe aver apportato modifiche per correggere errori secondari, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="33b29-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="33b29-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33b29-149">Requirements</span></span>



| <span data-ttu-id="33b29-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="33b29-150">Requirement</span></span> | <span data-ttu-id="33b29-151">Valore</span><span class="sxs-lookup"><span data-stu-id="33b29-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33b29-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33b29-152">Minimum supported client</span></span><br/> | <span data-ttu-id="33b29-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33b29-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="33b29-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33b29-154">Minimum supported server</span></span><br/> | <span data-ttu-id="33b29-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33b29-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="33b29-156">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="33b29-156">Namespace</span></span><br/>                | <span data-ttu-id="33b29-157">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="33b29-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="33b29-158">MOF</span><span class="sxs-lookup"><span data-stu-id="33b29-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33b29-159"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="33b29-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="33b29-160">DLL</span><span class="sxs-lookup"><span data-stu-id="33b29-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33b29-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33b29-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33b29-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33b29-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33b29-163">CIM \_ DeviceFile</span><span class="sxs-lookup"><span data-stu-id="33b29-163">CIM\_DeviceFile</span></span>](copy-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="33b29-164">**CIM \_ DeviceFile**</span><span class="sxs-lookup"><span data-stu-id="33b29-164">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

