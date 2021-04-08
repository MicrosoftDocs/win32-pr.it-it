---
description: Ottiene la proprietà del file di dispositivo logico specificato nel percorso dell'oggetto. Questo metodo è una versione estesa del metodo TakeOwnerShip e viene ereditato da CIM \_ LogicalFile.
ms.assetid: 084f755a-e837-4d21-8bd2-0f63f80302fc
ms.tgt_platform: multiple
title: Metodo TakeOwnerShipEx della classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3c36239d7d0ea6b0bf3bfa67bfb2f59617ab209a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877274"
---
# <a name="takeownershipex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="f838d-104">Metodo TakeOwnerShipEx della classe CIM \_ DeviceFile</span><span class="sxs-lookup"><span data-stu-id="f838d-104">TakeOwnerShipEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="f838d-105">Il metodo **TakeOwnerShipEx** ottiene la proprietà del file di dispositivo logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f838d-105">The **TakeOwnerShipEx** method obtains ownership of the logical device file specified in the object path.</span></span> <span data-ttu-id="f838d-106">Questo metodo è una versione estesa del metodo [**TakeOwnership**](takeownership-method-in-class-cim-devicefile.md) e viene ereditato da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="f838d-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-cim-devicefile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span> <span data-ttu-id="f838d-107">Se il file logico è una directory, questo metodo agisce in modo ricorsivo, assumendo la proprietà di tutti i file e le sottodirectory contenuti nella directory.</span><span class="sxs-lookup"><span data-stu-id="f838d-107">If the logical file is a directory, then this method acts recursively, taking ownership of all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f838d-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="f838d-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f838d-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f838d-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f838d-110">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="f838d-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f838d-111">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f838d-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f838d-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f838d-112">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="f838d-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="f838d-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f838d-114">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f838d-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f838d-115">Stringa che rappresenta il nome del file o della directory in cui il metodo ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="f838d-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="f838d-116">Questo parametro è **null** se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="f838d-116">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="f838d-117">*StartFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f838d-117">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f838d-118">Stringa che rappresenta il file o la directory figlio da utilizzare come punto di partenza per questo metodo.</span><span class="sxs-lookup"><span data-stu-id="f838d-118">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="f838d-119">In genere, il parametro *StartFileName* è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="f838d-119">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="f838d-120">Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificata nella chiamata **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="f838d-120">If this parameter is **null**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="f838d-121">*Ricorsivo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f838d-121">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f838d-122">Se è **true**, anche il metodo viene applicato in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza [**CIM \_ DeviceFile**](cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="f838d-122">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="f838d-123">Per le istanze di file, questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="f838d-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f838d-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f838d-124">Return value</span></span>

<span data-ttu-id="f838d-125">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="f838d-125">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="f838d-126">0</span><span class="sxs-lookup"><span data-stu-id="f838d-126">0</span></span>

<span data-ttu-id="f838d-127">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="f838d-127">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f838d-128">2</span><span class="sxs-lookup"><span data-stu-id="f838d-128">2</span></span>

<span data-ttu-id="f838d-129">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="f838d-129">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f838d-130">8</span><span class="sxs-lookup"><span data-stu-id="f838d-130">8</span></span>

<span data-ttu-id="f838d-131">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="f838d-131">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f838d-132">9</span><span class="sxs-lookup"><span data-stu-id="f838d-132">9</span></span>

<span data-ttu-id="f838d-133">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="f838d-133">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f838d-134">10</span><span class="sxs-lookup"><span data-stu-id="f838d-134">10</span></span>

<span data-ttu-id="f838d-135">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="f838d-135">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f838d-136">11</span><span class="sxs-lookup"><span data-stu-id="f838d-136">11</span></span>

<span data-ttu-id="f838d-137">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="f838d-137">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f838d-138">12</span><span class="sxs-lookup"><span data-stu-id="f838d-138">12</span></span>

<span data-ttu-id="f838d-139">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="f838d-139">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f838d-140">13</span><span class="sxs-lookup"><span data-stu-id="f838d-140">13</span></span>

<span data-ttu-id="f838d-141">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="f838d-141">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f838d-142">14</span><span class="sxs-lookup"><span data-stu-id="f838d-142">14</span></span>

<span data-ttu-id="f838d-143">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="f838d-143">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f838d-144">15</span><span class="sxs-lookup"><span data-stu-id="f838d-144">15</span></span>

<span data-ttu-id="f838d-145">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="f838d-145">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f838d-146">16</span><span class="sxs-lookup"><span data-stu-id="f838d-146">16</span></span>

<span data-ttu-id="f838d-147">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="f838d-147">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f838d-148">17</span><span class="sxs-lookup"><span data-stu-id="f838d-148">17</span></span>

<span data-ttu-id="f838d-149">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="f838d-149">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f838d-150">21</span><span class="sxs-lookup"><span data-stu-id="f838d-150">21</span></span>

<span data-ttu-id="f838d-151">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="f838d-151">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f838d-152">Commenti</span><span class="sxs-lookup"><span data-stu-id="f838d-152">Remarks</span></span>

<span data-ttu-id="f838d-153">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="f838d-153">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="f838d-154">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="f838d-154">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="f838d-155">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="f838d-155">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f838d-156">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="f838d-156">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f838d-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f838d-157">Requirements</span></span>



| <span data-ttu-id="f838d-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="f838d-158">Requirement</span></span> | <span data-ttu-id="f838d-159">Valore</span><span class="sxs-lookup"><span data-stu-id="f838d-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f838d-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f838d-160">Minimum supported client</span></span><br/> | <span data-ttu-id="f838d-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f838d-161">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f838d-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f838d-162">Minimum supported server</span></span><br/> | <span data-ttu-id="f838d-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f838d-163">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f838d-164">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f838d-164">Namespace</span></span><br/>                | <span data-ttu-id="f838d-165">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f838d-165">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f838d-166">MOF</span><span class="sxs-lookup"><span data-stu-id="f838d-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f838d-167"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f838d-167"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f838d-168">DLL</span><span class="sxs-lookup"><span data-stu-id="f838d-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f838d-169"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f838d-169"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f838d-170">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f838d-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f838d-171">\_DEVICEFILE CIM</span><span class="sxs-lookup"><span data-stu-id="f838d-171">CIM\_DeviceFile</span></span>](takeownershipex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="f838d-172">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="f838d-172">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

