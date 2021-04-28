---
description: "Metodo TakeOwnerShip della CIM_Directory: il metodo TakeOwnerShip ottiene la proprietà del file logico specificato nel percorso dell'oggetto."
ms.assetid: 053647d0-3ba0-4cd4-a84a-a1a96ef7151c
ms.tgt_platform: multiple
title: Metodo TakeOwnerShip della CIM_Directory classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12c328f30e56db348b018b73b02aa4320bf99505
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086059"
---
# <a name="takeownership-method-of-the-cim_directory-class"></a><span data-ttu-id="802ba-103">Metodo TakeOwnerShip della classe Directory CIM \_</span><span class="sxs-lookup"><span data-stu-id="802ba-103">TakeOwnerShip method of the CIM\_Directory class</span></span>

<span data-ttu-id="802ba-104">Il **metodo TakeOwnerShip** ottiene la proprietà del file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="802ba-104">The **TakeOwnerShip** method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="802ba-105">Se il file logico è una directory, questo metodo agisce in modo ricorsivo, assumendo la proprietà di tutti i file e le sottodirectory contenuti nella directory.</span><span class="sxs-lookup"><span data-stu-id="802ba-105">If the logical file is a directory, this method acts recursively, taking ownership of all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="802ba-106">Questo metodo viene ereditato da [**CIM \_ LogicalFile.**](cim-logicalfile.md)</span><span class="sxs-lookup"><span data-stu-id="802ba-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="802ba-107">Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="802ba-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="802ba-108">WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="802ba-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="802ba-109">Questo argomento usa Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="802ba-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="802ba-110">Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="802ba-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="802ba-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="802ba-111">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="802ba-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="802ba-112">Parameters</span></span>

<span data-ttu-id="802ba-113">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="802ba-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="802ba-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="802ba-114">Return value</span></span>

<span data-ttu-id="802ba-115">Restituisce il valore 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="802ba-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="802ba-116">**0**</span><span class="sxs-lookup"><span data-stu-id="802ba-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="802ba-117">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="802ba-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="802ba-118">**2**</span><span class="sxs-lookup"><span data-stu-id="802ba-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="802ba-119">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="802ba-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="802ba-120">**8**</span><span class="sxs-lookup"><span data-stu-id="802ba-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="802ba-121">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="802ba-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="802ba-122">**9**</span><span class="sxs-lookup"><span data-stu-id="802ba-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="802ba-123">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="802ba-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="802ba-124">**10**</span><span class="sxs-lookup"><span data-stu-id="802ba-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="802ba-125">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="802ba-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="802ba-126">**11**</span><span class="sxs-lookup"><span data-stu-id="802ba-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="802ba-127">File system non NTFS.</span><span class="sxs-lookup"><span data-stu-id="802ba-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="802ba-128">**12**</span><span class="sxs-lookup"><span data-stu-id="802ba-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="802ba-129">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="802ba-129">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="802ba-130">**13**</span><span class="sxs-lookup"><span data-stu-id="802ba-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="802ba-131">Unità non uguale.</span><span class="sxs-lookup"><span data-stu-id="802ba-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="802ba-132">**14**</span><span class="sxs-lookup"><span data-stu-id="802ba-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="802ba-133">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="802ba-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="802ba-134">**15**</span><span class="sxs-lookup"><span data-stu-id="802ba-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="802ba-135">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="802ba-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="802ba-136">**16**</span><span class="sxs-lookup"><span data-stu-id="802ba-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="802ba-137">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="802ba-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="802ba-138">**17**</span><span class="sxs-lookup"><span data-stu-id="802ba-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="802ba-139">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="802ba-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="802ba-140">**21**</span><span class="sxs-lookup"><span data-stu-id="802ba-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="802ba-141">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="802ba-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="802ba-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="802ba-142">Remarks</span></span>

<span data-ttu-id="802ba-143">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="802ba-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="802ba-144">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="802ba-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="802ba-145">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="802ba-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="802ba-146">Microsoft potrebbe aver apportato modifiche per correggere gli errori minori, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="802ba-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="examples"></a><span data-ttu-id="802ba-147">Esempio</span><span class="sxs-lookup"><span data-stu-id="802ba-147">Examples</span></span>

<span data-ttu-id="802ba-148">Il codice Visual Basic script seguente chiama il **metodo TakeOwnerShip** per assumere la proprietà della cartella \\ C: temp.</span><span class="sxs-lookup"><span data-stu-id="802ba-148">The following Visual Basic Script code calls the **TakeOwnerShip** method to take ownership of the C:\\temp folder.</span></span>


```VB
strComputer = "." 

Set objWMIService = _
    GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 

' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\\temp'", "TakeOwnerShip")

wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a><span data-ttu-id="802ba-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="802ba-149">Requirements</span></span>



| <span data-ttu-id="802ba-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="802ba-150">Requirement</span></span> | <span data-ttu-id="802ba-151">Valore</span><span class="sxs-lookup"><span data-stu-id="802ba-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="802ba-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="802ba-152">Minimum supported client</span></span><br/> | <span data-ttu-id="802ba-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="802ba-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="802ba-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="802ba-154">Minimum supported server</span></span><br/> | <span data-ttu-id="802ba-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="802ba-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="802ba-156">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="802ba-156">Namespace</span></span><br/>                | <span data-ttu-id="802ba-157">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="802ba-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="802ba-158">MOF</span><span class="sxs-lookup"><span data-stu-id="802ba-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="802ba-159"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="802ba-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="802ba-160">DLL</span><span class="sxs-lookup"><span data-stu-id="802ba-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="802ba-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="802ba-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="802ba-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="802ba-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="802ba-163">CIM \_ Directory</span><span class="sxs-lookup"><span data-stu-id="802ba-163">CIM\_Directory</span></span>](takeownership-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="802ba-164">**CIM \_ Directory**</span><span class="sxs-lookup"><span data-stu-id="802ba-164">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

