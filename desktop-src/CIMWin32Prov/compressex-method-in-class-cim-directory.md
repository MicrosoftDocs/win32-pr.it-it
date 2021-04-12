---
description: Il metodo CompressEx comprime il file o la directory logica specificata nel percorso dell'oggetto. Questo metodo è una versione estesa del metodo Compress ed è ereditato da CIM \_ LogicalFile.
ms.assetid: 82a28a3b-b2e4-4834-b4a5-02ffe94f3fc7
ms.tgt_platform: multiple
title: Metodo CompressEx della classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8bebd729d87e012c3fce6dd2eb87b1c61ffa423a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523098"
---
# <a name="compressex-method-of-the-cim_directory-class"></a><span data-ttu-id="aed3f-104">Metodo CompressEx della classe di \_ directory CIM</span><span class="sxs-lookup"><span data-stu-id="aed3f-104">CompressEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="aed3f-105">Il metodo **CompressEx** comprime il file o la directory logica specificata nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aed3f-105">The **CompressEx** method compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="aed3f-106">Questo metodo è una versione estesa del metodo [**Compress**](compress-method-in-class-cim-directory.md) ed è ereditato da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="aed3f-106">This method is an extended version of the [**Compress**](compress-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aed3f-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="aed3f-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="aed3f-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="aed3f-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="aed3f-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="aed3f-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="aed3f-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="aed3f-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="aed3f-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aed3f-111">Syntax</span></span>


```mof
uint32 CompressEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="aed3f-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="aed3f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aed3f-113">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="aed3f-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aed3f-114">Stringa che rappresenta il nome del file o della directory in cui il metodo ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="aed3f-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="aed3f-115">Questo parametro è null se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="aed3f-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="aed3f-116">*StartFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aed3f-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aed3f-117">Stringa che rappresenta il file o la directory figlio da utilizzare come punto di partenza per questo metodo.</span><span class="sxs-lookup"><span data-stu-id="aed3f-117">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="aed3f-118">In genere, questo parametro è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="aed3f-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="aed3f-119">Se questo parametro è null, l'operazione viene eseguita sul file o sulla directory specificati nella chiamata [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="aed3f-119">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="aed3f-120">*Ricorsivo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aed3f-120">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aed3f-121">Se è **true**, anche il metodo viene applicato in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza di [**\_ directory CIM**](cim-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="aed3f-121">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="aed3f-122">Per le istanze di file, questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="aed3f-122">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aed3f-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aed3f-123">Return value</span></span>

<span data-ttu-id="aed3f-124">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="aed3f-124">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="aed3f-125">0</span><span class="sxs-lookup"><span data-stu-id="aed3f-125">0</span></span>

<span data-ttu-id="aed3f-126">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="aed3f-126">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="aed3f-127">2</span><span class="sxs-lookup"><span data-stu-id="aed3f-127">2</span></span>

<span data-ttu-id="aed3f-128">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="aed3f-128">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="aed3f-129">8</span><span class="sxs-lookup"><span data-stu-id="aed3f-129">8</span></span>

<span data-ttu-id="aed3f-130">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="aed3f-130">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="aed3f-131">9</span><span class="sxs-lookup"><span data-stu-id="aed3f-131">9</span></span>

<span data-ttu-id="aed3f-132">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="aed3f-132">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="aed3f-133">10</span><span class="sxs-lookup"><span data-stu-id="aed3f-133">10</span></span>

<span data-ttu-id="aed3f-134">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="aed3f-134">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="aed3f-135">11</span><span class="sxs-lookup"><span data-stu-id="aed3f-135">11</span></span>

<span data-ttu-id="aed3f-136">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="aed3f-136">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="aed3f-137">12</span><span class="sxs-lookup"><span data-stu-id="aed3f-137">12</span></span>

<span data-ttu-id="aed3f-138">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="aed3f-138">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="aed3f-139">13</span><span class="sxs-lookup"><span data-stu-id="aed3f-139">13</span></span>

<span data-ttu-id="aed3f-140">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="aed3f-140">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="aed3f-141">14</span><span class="sxs-lookup"><span data-stu-id="aed3f-141">14</span></span>

<span data-ttu-id="aed3f-142">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="aed3f-142">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="aed3f-143">15</span><span class="sxs-lookup"><span data-stu-id="aed3f-143">15</span></span>

<span data-ttu-id="aed3f-144">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="aed3f-144">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="aed3f-145">16</span><span class="sxs-lookup"><span data-stu-id="aed3f-145">16</span></span>

<span data-ttu-id="aed3f-146">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="aed3f-146">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="aed3f-147">17</span><span class="sxs-lookup"><span data-stu-id="aed3f-147">17</span></span>

<span data-ttu-id="aed3f-148">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="aed3f-148">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="aed3f-149">21</span><span class="sxs-lookup"><span data-stu-id="aed3f-149">21</span></span>

<span data-ttu-id="aed3f-150">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="aed3f-150">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aed3f-151">Commenti</span><span class="sxs-lookup"><span data-stu-id="aed3f-151">Remarks</span></span>

<span data-ttu-id="aed3f-152">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="aed3f-152">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="aed3f-153">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="aed3f-153">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="aed3f-154">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="aed3f-154">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="aed3f-155">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="aed3f-155">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="aed3f-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aed3f-156">Requirements</span></span>



| <span data-ttu-id="aed3f-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="aed3f-157">Requirement</span></span> | <span data-ttu-id="aed3f-158">Valore</span><span class="sxs-lookup"><span data-stu-id="aed3f-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aed3f-159">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aed3f-159">Minimum supported client</span></span><br/> | <span data-ttu-id="aed3f-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aed3f-160">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aed3f-161">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aed3f-161">Minimum supported server</span></span><br/> | <span data-ttu-id="aed3f-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aed3f-162">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aed3f-163">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="aed3f-163">Namespace</span></span><br/>                | <span data-ttu-id="aed3f-164">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="aed3f-164">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aed3f-165">MOF</span><span class="sxs-lookup"><span data-stu-id="aed3f-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aed3f-166"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aed3f-166"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aed3f-167">DLL</span><span class="sxs-lookup"><span data-stu-id="aed3f-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aed3f-168"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aed3f-168"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aed3f-169">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aed3f-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aed3f-170">\_Directory CIM</span><span class="sxs-lookup"><span data-stu-id="aed3f-170">CIM\_Directory</span></span>](compressex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="aed3f-171">**\_Directory CIM**</span><span class="sxs-lookup"><span data-stu-id="aed3f-171">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

