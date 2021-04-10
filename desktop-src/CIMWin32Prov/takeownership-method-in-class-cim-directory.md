---
description: Il metodo TakeOwnerShip ottiene la proprietà del file logico specificato nel percorso dell'oggetto.
ms.assetid: 053647d0-3ba0-4cd4-a84a-a1a96ef7151c
ms.tgt_platform: multiple
title: Metodo TakeOwnerShip della classe CIM_Directory
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
ms.openlocfilehash: dc68e974c98405f03c4bbfb45f02fdf78bf65127
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225788"
---
# <a name="takeownership-method-of-the-cim_directory-class"></a><span data-ttu-id="21856-103">Metodo TakeOwnerShip della classe di \_ directory CIM</span><span class="sxs-lookup"><span data-stu-id="21856-103">TakeOwnerShip method of the CIM\_Directory class</span></span>

<span data-ttu-id="21856-104">Il metodo **TakeOwnership** ottiene la proprietà del file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="21856-104">The **TakeOwnerShip** method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="21856-105">Se il file logico è una directory, questo metodo agisce in modo ricorsivo, assumendo la proprietà di tutti i file e le sottodirectory contenuti nella directory.</span><span class="sxs-lookup"><span data-stu-id="21856-105">If the logical file is a directory, this method acts recursively, taking ownership of all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="21856-106">Questo metodo viene ereditato da [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="21856-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="21856-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="21856-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="21856-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="21856-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="21856-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="21856-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="21856-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="21856-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="21856-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21856-111">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="21856-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="21856-112">Parameters</span></span>

<span data-ttu-id="21856-113">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="21856-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="21856-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21856-114">Return value</span></span>

<span data-ttu-id="21856-115">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="21856-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="21856-116">**0**</span><span class="sxs-lookup"><span data-stu-id="21856-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="21856-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="21856-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="21856-118">**2**</span><span class="sxs-lookup"><span data-stu-id="21856-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="21856-119">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="21856-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="21856-120">**8**</span><span class="sxs-lookup"><span data-stu-id="21856-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="21856-121">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="21856-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="21856-122">**9**</span><span class="sxs-lookup"><span data-stu-id="21856-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="21856-123">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="21856-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="21856-124">**10**</span><span class="sxs-lookup"><span data-stu-id="21856-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="21856-125">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="21856-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="21856-126">**11**</span><span class="sxs-lookup"><span data-stu-id="21856-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="21856-127">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="21856-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="21856-128">**12**</span><span class="sxs-lookup"><span data-stu-id="21856-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="21856-129">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="21856-129">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="21856-130">**13**</span><span class="sxs-lookup"><span data-stu-id="21856-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="21856-131">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="21856-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="21856-132">**14**</span><span class="sxs-lookup"><span data-stu-id="21856-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="21856-133">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="21856-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="21856-134">**15**</span><span class="sxs-lookup"><span data-stu-id="21856-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="21856-135">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="21856-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="21856-136">**16**</span><span class="sxs-lookup"><span data-stu-id="21856-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="21856-137">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="21856-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="21856-138">**17**</span><span class="sxs-lookup"><span data-stu-id="21856-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="21856-139">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="21856-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="21856-140">**21**</span><span class="sxs-lookup"><span data-stu-id="21856-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="21856-141">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="21856-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="21856-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="21856-142">Remarks</span></span>

<span data-ttu-id="21856-143">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="21856-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="21856-144">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="21856-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="21856-145">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="21856-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="21856-146">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="21856-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="examples"></a><span data-ttu-id="21856-147">Esempio</span><span class="sxs-lookup"><span data-stu-id="21856-147">Examples</span></span>

<span data-ttu-id="21856-148">Il codice di script seguente Visual Basic chiama il metodo **TakeOwnership** per assumere la proprietà della cartella C: \\ Temp.</span><span class="sxs-lookup"><span data-stu-id="21856-148">The following Visual Basic Script code calls the **TakeOwnerShip** method to take ownership of the C:\\temp folder.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="21856-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21856-149">Requirements</span></span>



| <span data-ttu-id="21856-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="21856-150">Requirement</span></span> | <span data-ttu-id="21856-151">Valore</span><span class="sxs-lookup"><span data-stu-id="21856-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21856-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21856-152">Minimum supported client</span></span><br/> | <span data-ttu-id="21856-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21856-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="21856-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21856-154">Minimum supported server</span></span><br/> | <span data-ttu-id="21856-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21856-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="21856-156">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="21856-156">Namespace</span></span><br/>                | <span data-ttu-id="21856-157">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="21856-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="21856-158">MOF</span><span class="sxs-lookup"><span data-stu-id="21856-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="21856-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="21856-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="21856-160">DLL</span><span class="sxs-lookup"><span data-stu-id="21856-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21856-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21856-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21856-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21856-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21856-163">\_Directory CIM</span><span class="sxs-lookup"><span data-stu-id="21856-163">CIM\_Directory</span></span>](takeownership-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="21856-164">**\_Directory CIM**</span><span class="sxs-lookup"><span data-stu-id="21856-164">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

