---
description: Il metodo DeleteEx Elimina il file o la directory logica specificata nel percorso dell'oggetto. Questo metodo è una versione estesa del metodo Delete ed è ereditato da CIM \_ LogicalFile.
ms.assetid: ef4d08cd-7287-47be-bcfc-edc248ac5c9b
ms.tgt_platform: multiple
title: Metodo DeleteEx della classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4e68e7118088b9da1f1a1e2990c0a253ac85714
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748154"
---
# <a name="deleteex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="1eeb2-104">Metodo DeleteEx della classe CIM \_ DeviceFile</span><span class="sxs-lookup"><span data-stu-id="1eeb2-104">DeleteEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="1eeb2-105">Il metodo **DeleteEx** Elimina il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-105">The **DeleteEx** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="1eeb2-106">Questo metodo è una versione estesa del metodo [**Delete**](delete-method-in-class-cim-devicefile.md) ed è ereditato da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="1eeb2-106">This method is an extended version of the [**Delete**](delete-method-in-class-cim-devicefile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1eeb2-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1eeb2-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1eeb2-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1eeb2-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="1eeb2-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1eeb2-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1eeb2-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1eeb2-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1eeb2-111">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="1eeb2-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="1eeb2-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1eeb2-113">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1eeb2-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eeb2-114">Stringa che rappresenta il nome del file o della directory in cui il metodo ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="1eeb2-115">Questo parametro è null se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="1eeb2-116">*StartFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1eeb2-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eeb2-117">Stringa che rappresenta il file o la directory figlio da utilizzare come punto di partenza per questo metodo.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-117">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="1eeb2-118">In genere, il parametro **StartFileName** è il parametro **StopFileName** che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-118">Typically, the **StartFileName** parameter is the **StopFileName** parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="1eeb2-119">Se questo parametro è null, l'operazione viene eseguita sul file o sulla directory specificata nella chiamata [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="1eeb2-119">If this parameter is null, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1eeb2-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1eeb2-120">Return value</span></span>

<span data-ttu-id="1eeb2-121">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-121">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="1eeb2-122">0</span><span class="sxs-lookup"><span data-stu-id="1eeb2-122">0</span></span>

<span data-ttu-id="1eeb2-123">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-123">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1eeb2-124">2</span><span class="sxs-lookup"><span data-stu-id="1eeb2-124">2</span></span>

<span data-ttu-id="1eeb2-125">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-125">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1eeb2-126">8</span><span class="sxs-lookup"><span data-stu-id="1eeb2-126">8</span></span>

<span data-ttu-id="1eeb2-127">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-127">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1eeb2-128">9</span><span class="sxs-lookup"><span data-stu-id="1eeb2-128">9</span></span>

<span data-ttu-id="1eeb2-129">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-129">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1eeb2-130">10</span><span class="sxs-lookup"><span data-stu-id="1eeb2-130">10</span></span>

<span data-ttu-id="1eeb2-131">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-131">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1eeb2-132">11</span><span class="sxs-lookup"><span data-stu-id="1eeb2-132">11</span></span>

<span data-ttu-id="1eeb2-133">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-133">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1eeb2-134">12</span><span class="sxs-lookup"><span data-stu-id="1eeb2-134">12</span></span>

<span data-ttu-id="1eeb2-135">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-135">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1eeb2-136">13</span><span class="sxs-lookup"><span data-stu-id="1eeb2-136">13</span></span>

<span data-ttu-id="1eeb2-137">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-137">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1eeb2-138">14</span><span class="sxs-lookup"><span data-stu-id="1eeb2-138">14</span></span>

<span data-ttu-id="1eeb2-139">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-139">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1eeb2-140">15</span><span class="sxs-lookup"><span data-stu-id="1eeb2-140">15</span></span>

<span data-ttu-id="1eeb2-141">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-141">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1eeb2-142">16</span><span class="sxs-lookup"><span data-stu-id="1eeb2-142">16</span></span>

<span data-ttu-id="1eeb2-143">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-143">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1eeb2-144">17</span><span class="sxs-lookup"><span data-stu-id="1eeb2-144">17</span></span>

<span data-ttu-id="1eeb2-145">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-145">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1eeb2-146">21</span><span class="sxs-lookup"><span data-stu-id="1eeb2-146">21</span></span>

<span data-ttu-id="1eeb2-147">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-147">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1eeb2-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="1eeb2-148">Remarks</span></span>

<span data-ttu-id="1eeb2-149">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-149">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="1eeb2-150">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-150">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="1eeb2-151">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-151">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1eeb2-152">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="1eeb2-152">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eeb2-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1eeb2-153">Requirements</span></span>



| <span data-ttu-id="1eeb2-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="1eeb2-154">Requirement</span></span> | <span data-ttu-id="1eeb2-155">Valore</span><span class="sxs-lookup"><span data-stu-id="1eeb2-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1eeb2-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1eeb2-156">Minimum supported client</span></span><br/> | <span data-ttu-id="1eeb2-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1eeb2-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1eeb2-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1eeb2-158">Minimum supported server</span></span><br/> | <span data-ttu-id="1eeb2-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1eeb2-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1eeb2-160">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1eeb2-160">Namespace</span></span><br/>                | <span data-ttu-id="1eeb2-161">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="1eeb2-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1eeb2-162">MOF</span><span class="sxs-lookup"><span data-stu-id="1eeb2-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1eeb2-163"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1eeb2-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1eeb2-164">DLL</span><span class="sxs-lookup"><span data-stu-id="1eeb2-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1eeb2-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1eeb2-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1eeb2-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1eeb2-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eeb2-167">\_DEVICEFILE CIM</span><span class="sxs-lookup"><span data-stu-id="1eeb2-167">CIM\_DeviceFile</span></span>](deleteex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="1eeb2-168">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="1eeb2-168">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

