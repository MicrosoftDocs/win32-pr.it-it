---
description: Ottiene la proprietà del file di voce della directory logica specificato nel percorso dell'oggetto. Questo metodo è una versione estesa del metodo TakeOwnerShip e viene ereditato da CIM \_ LogicalFile.
ms.assetid: a13acaa2-2203-470a-b989-15f8276e46c6
ms.tgt_platform: multiple
title: Metodo TakeOwnerShipEx della classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b02a6c40e99405c150a372f8eb15fe648f2df60a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126003"
---
# <a name="takeownershipex-method-of-the-cim_directory-class"></a><span data-ttu-id="05d76-104">Metodo TakeOwnerShipEx della classe di \_ directory CIM</span><span class="sxs-lookup"><span data-stu-id="05d76-104">TakeOwnerShipEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="05d76-105">Il metodo **TakeOwnerShipEx** ottiene la proprietà del file di voce della directory logica specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="05d76-105">The **TakeOwnerShipEx** method obtains ownership of the logical directory entry file specified in the object path.</span></span> <span data-ttu-id="05d76-106">Questo metodo è una versione estesa del metodo [**TakeOwnership**](takeownership-method-in-class-cim-directory.md) e viene ereditato da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="05d76-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span> <span data-ttu-id="05d76-107">Se il file logico è una directory, questo metodo agisce in modo ricorsivo, assumendo la proprietà di tutti i file e le sottodirectory contenuti nella directory.</span><span class="sxs-lookup"><span data-stu-id="05d76-107">If the logical file is a directory, then this method acts recursively, taking ownership of all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="05d76-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="05d76-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="05d76-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="05d76-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="05d76-110">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="05d76-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="05d76-111">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="05d76-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="05d76-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="05d76-112">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="05d76-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="05d76-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05d76-114">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="05d76-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05d76-115">Stringa che rappresenta il nome del file o della directory in cui il metodo ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="05d76-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="05d76-116">Questo parametro è null se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="05d76-116">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="05d76-117">*StartFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="05d76-117">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05d76-118">Stringa che rappresenta il file o la directory figlio da utilizzare come punto di partenza per questo metodo.</span><span class="sxs-lookup"><span data-stu-id="05d76-118">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="05d76-119">In genere, questo parametro è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="05d76-119">Typically, this parameter is the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="05d76-120">Se questo parametro è null, l'operazione viene eseguita sul file o sulla directory specificati nella chiamata [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="05d76-120">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="05d76-121">*Ricorsivo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="05d76-121">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05d76-122">Se **true**, il metodo viene applicato in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza di [**\_ directory CIM**](cim-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="05d76-122">If **True**, the method is applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="05d76-123">Per le istanze di file, questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="05d76-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05d76-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="05d76-124">Return value</span></span>

<span data-ttu-id="05d76-125">Restituisce un valore pari a 0 in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="05d76-125">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="05d76-126">0</span><span class="sxs-lookup"><span data-stu-id="05d76-126">0</span></span>

<span data-ttu-id="05d76-127">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="05d76-127">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="05d76-128">2</span><span class="sxs-lookup"><span data-stu-id="05d76-128">2</span></span>

<span data-ttu-id="05d76-129">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="05d76-129">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="05d76-130">8</span><span class="sxs-lookup"><span data-stu-id="05d76-130">8</span></span>

<span data-ttu-id="05d76-131">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="05d76-131">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="05d76-132">9</span><span class="sxs-lookup"><span data-stu-id="05d76-132">9</span></span>

<span data-ttu-id="05d76-133">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="05d76-133">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="05d76-134">10</span><span class="sxs-lookup"><span data-stu-id="05d76-134">10</span></span>

<span data-ttu-id="05d76-135">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="05d76-135">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="05d76-136">11</span><span class="sxs-lookup"><span data-stu-id="05d76-136">11</span></span>

<span data-ttu-id="05d76-137">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="05d76-137">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="05d76-138">12</span><span class="sxs-lookup"><span data-stu-id="05d76-138">12</span></span>

<span data-ttu-id="05d76-139">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="05d76-139">The platform is not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="05d76-140">13</span><span class="sxs-lookup"><span data-stu-id="05d76-140">13</span></span>

<span data-ttu-id="05d76-141">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="05d76-141">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="05d76-142">14</span><span class="sxs-lookup"><span data-stu-id="05d76-142">14</span></span>

<span data-ttu-id="05d76-143">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="05d76-143">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="05d76-144">15</span><span class="sxs-lookup"><span data-stu-id="05d76-144">15</span></span>

<span data-ttu-id="05d76-145">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="05d76-145">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="05d76-146">16</span><span class="sxs-lookup"><span data-stu-id="05d76-146">16</span></span>

<span data-ttu-id="05d76-147">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="05d76-147">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="05d76-148">17</span><span class="sxs-lookup"><span data-stu-id="05d76-148">17</span></span>

<span data-ttu-id="05d76-149">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="05d76-149">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="05d76-150">21</span><span class="sxs-lookup"><span data-stu-id="05d76-150">21</span></span>

<span data-ttu-id="05d76-151">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="05d76-151">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05d76-152">Commenti</span><span class="sxs-lookup"><span data-stu-id="05d76-152">Remarks</span></span>

<span data-ttu-id="05d76-153">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="05d76-153">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="05d76-154">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="05d76-154">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="05d76-155">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="05d76-155">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="05d76-156">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="05d76-156">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="examples"></a><span data-ttu-id="05d76-157">Esempio</span><span class="sxs-lookup"><span data-stu-id="05d76-157">Examples</span></span>

<span data-ttu-id="05d76-158">Il codice di script seguente Visual Basic chiama il metodo **TakeOwnerShipEx** per assumere la proprietà della cartella C: \\ Temp.</span><span class="sxs-lookup"><span data-stu-id="05d76-158">The following Visual Basic Script code calls the **TakeOwnerShipEx** method to take ownership of the C:\\temp folder.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject( _
    "winmgmts:\\" & strComputer & "\root\CIMV2") 
' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")
' Obtain an InParameters object specific
' to the method.
Set objInParam = objShare.Methods_("TakeOwnerShipEx"). _
    inParameters.SpawnInstance_()

' Add the input parameters.
objInParam.Properties_.Item("Recursive") =  true

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\Temp'", "TakeOwnerShipEx", objInParam)
wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a><span data-ttu-id="05d76-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05d76-159">Requirements</span></span>



| <span data-ttu-id="05d76-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="05d76-160">Requirement</span></span> | <span data-ttu-id="05d76-161">Valore</span><span class="sxs-lookup"><span data-stu-id="05d76-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05d76-162">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05d76-162">Minimum supported client</span></span><br/> | <span data-ttu-id="05d76-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="05d76-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="05d76-164">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05d76-164">Minimum supported server</span></span><br/> | <span data-ttu-id="05d76-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05d76-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="05d76-166">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="05d76-166">Namespace</span></span><br/>                | <span data-ttu-id="05d76-167">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="05d76-167">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="05d76-168">MOF</span><span class="sxs-lookup"><span data-stu-id="05d76-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05d76-169"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="05d76-169"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="05d76-170">DLL</span><span class="sxs-lookup"><span data-stu-id="05d76-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05d76-171"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05d76-171"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05d76-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="05d76-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05d76-173">\_Directory CIM</span><span class="sxs-lookup"><span data-stu-id="05d76-173">CIM\_Directory</span></span>](takeownershipex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="05d76-174">**\_Directory CIM**</span><span class="sxs-lookup"><span data-stu-id="05d76-174">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

