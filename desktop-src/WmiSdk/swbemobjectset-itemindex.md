---
description: Restituisce l'oggetto SWbemObject associato all'indice specificato nella raccolta.
ms.assetid: 75830f78-0489-4fae-bf9c-2eee8526232e
ms.tgt_platform: multiple
title: Metodo SWbemObjectSet. ItemIndex (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.ItemIndex
- ISWbemObjectSet.ItemIndex
- ISWbemObjectSet.ItemIndex
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 606a09ebf54f0a31dbe14e10abd52a7e92d815d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316986"
---
# <a name="swbemobjectsetitemindex-method"></a><span data-ttu-id="853f7-103">SWbemObjectSet. ItemIndex, metodo</span><span class="sxs-lookup"><span data-stu-id="853f7-103">SWbemObjectSet.ItemIndex method</span></span>

<span data-ttu-id="853f7-104">Il metodo **ItemIndex** restituisce l' [**SWbemObject**](swbemobject.md) associato all'indice specificato nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="853f7-104">The **ItemIndex** method returns the [**SWbemObject**](swbemobject.md) associated with the specified index into the collection.</span></span> <span data-ttu-id="853f7-105">L'indice indica la posizione dell'elemento all'interno dell'insieme.</span><span class="sxs-lookup"><span data-stu-id="853f7-105">The index indicates the position of the element within the collection.</span></span> <span data-ttu-id="853f7-106">La numerazione della raccolta inizia da zero.</span><span class="sxs-lookup"><span data-stu-id="853f7-106">Collection numbering starts at zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="853f7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="853f7-107">Syntax</span></span>


```VB
objWbemObject = .ItemIndex( _
  ByVal lIndex _
)
```



## <a name="parameters"></a><span data-ttu-id="853f7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="853f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="853f7-109">*lIndex*</span><span class="sxs-lookup"><span data-stu-id="853f7-109">*lIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="853f7-110">Indice dell'elemento nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="853f7-110">Index of the item in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="853f7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="853f7-111">Return value</span></span>

<span data-ttu-id="853f7-112">In caso di esito positivo, l'oggetto [**SWbemObject**](swbemobject.md) richiesto restituisce.</span><span class="sxs-lookup"><span data-stu-id="853f7-112">If successful, the requested [**SWbemObject**](swbemobject.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="853f7-113">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="853f7-113">Error codes</span></span>

<span data-ttu-id="853f7-114">Al termine del metodo [**Item**](swbemobjectset-item.md) , l'oggetto **Err** può contenere uno dei codici di errore riportati di seguito.</span><span class="sxs-lookup"><span data-stu-id="853f7-114">Upon completion of the [**Item**](swbemobjectset-item.md) method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="853f7-115">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="853f7-115">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="853f7-116">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="853f7-116">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="853f7-117">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="853f7-117">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="853f7-118">È stato specificato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="853f7-118">Invalid parameter was specified.</span></span> <span data-ttu-id="853f7-119">Questo errore viene restituito se viene specificato un numero di indice negativo.</span><span class="sxs-lookup"><span data-stu-id="853f7-119">This error is returned if a negative index number is supplied.</span></span>

</dd> <dt>

<span data-ttu-id="853f7-120">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="853f7-120">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="853f7-121">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="853f7-121">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="853f7-122">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="853f7-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="853f7-123">L'elemento richiesto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="853f7-123">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="853f7-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="853f7-124">Remarks</span></span>

<span data-ttu-id="853f7-125">Il metodo **ItemIndex** consente agli script e alle applicazioni dei client WMI scritti in qualsiasi linguaggio un modo uniforme per modificare una raccolta come una matrice.</span><span class="sxs-lookup"><span data-stu-id="853f7-125">The **ItemIndex** method allows WMI clients scripts and applications written in any language a uniform way to manipulate a collection like an array.</span></span> <span data-ttu-id="853f7-126">Questo metodo può essere utilizzato con le raccolte [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="853f7-126">This method can be used with [**SWbemObjectSet**](swbemobjectset.md) collections.</span></span> <span data-ttu-id="853f7-127">Le query, ad esempio [**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md), [**SWbemServices. ReferencesTo**](swbemservices-referencesto.md), [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)o [**SWbemServices.ExecQuery**](swbemservices-execquery.md) restituiscono le raccolte **SWbemObjectSet** .</span><span class="sxs-lookup"><span data-stu-id="853f7-127">Queries, such as [**SWbemServices.AssociatorsOf**](swbemservices-associatorsof.md), [**SWbemServices.ReferencesTo**](swbemservices-referencesto.md), [**SWbemServices.InstancesOf**](swbemservices-instancesof.md), or [**SWbemServices.ExecQuery**](swbemservices-execquery.md) return **SWbemObjectSet** collections.</span></span> <span data-ttu-id="853f7-128">Il metodo **ItemIndex** non funziona con le raccolte che non contengono [**SWbemObjects**](swbemobject.md), ad esempio [**SWbemMethodSet**](swbemmethodset.md), [**SWbemNamedValueSet**](swbemnamedvalueset.md), [**SWbemPrivilegeSet**](swbemprivilegeset.md), [**SWbemPropertySet**](swbempropertyset.md)e [**dell'SWbemQualifierSet**](swbemqualifierset.md).</span><span class="sxs-lookup"><span data-stu-id="853f7-128">The **ItemIndex** method does not work with collections which do not contain [**SWbemObjects**](swbemobject.md), such as [**SWbemMethodSet**](swbemmethodset.md), [**SWbemNamedValueSet**](swbemnamedvalueset.md), [**SWbemPrivilegeSet**](swbemprivilegeset.md), [**SWbemPropertySet**](swbempropertyset.md), and [**SWbemQualifierSet**](swbemqualifierset.md).</span></span>

<span data-ttu-id="853f7-129">**ItemIndex** può essere utilizzato anche per ottenere la singola istanza di una classe singleton.</span><span class="sxs-lookup"><span data-stu-id="853f7-129">**ItemIndex** can also be used to obtain the single instance of a singleton class.</span></span>

## <a name="examples"></a><span data-ttu-id="853f7-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="853f7-130">Examples</span></span>

<span data-ttu-id="853f7-131">Nell'esempio di codice VBScript seguente viene eseguita una query per una raccolta di tutte le istanze del [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) , quindi vengono visualizzati i nomi dei primi tre processi.</span><span class="sxs-lookup"><span data-stu-id="853f7-131">The following VBScript code example queries for a collection of all the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) instances then displays the names of the first three processes.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colProcesses = _
    objWMIService.Execquery("Select * from Win32_Process")
Wscript.Echo  colProcesses.ItemIndex(0).Name
Wscript.Echo  colProcesses.ItemIndex(1).Name
Wscript.Echo  colProcesses.ItemIndex(2).Name
```



<span data-ttu-id="853f7-132">Per ogni installazione del sistema operativo esiste una sola istanza di [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) .</span><span class="sxs-lookup"><span data-stu-id="853f7-132">Only one instance of [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) exists for each operating system installation.</span></span> <span data-ttu-id="853f7-133">La creazione del percorso [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) per ottenere la singola istanza è imbarazzante, quindi gli script enumerano normalmente **Win32 \_ OperatingSystem** anche se è disponibile una sola istanza.</span><span class="sxs-lookup"><span data-stu-id="853f7-133">Creating the [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) path to obtain the single instance is awkward so scripts normally enumerate **Win32\_OperatingSystem** even though only one instance is available.</span></span> <span data-ttu-id="853f7-134">Nell'esempio di codice VBScript riportato di seguito viene illustrato come utilizzare il metodo **ItemIndex** per ottenere **un \_ OperatingSystem Win32** senza utilizzare un ciclo **for each** .</span><span class="sxs-lookup"><span data-stu-id="853f7-134">The following VBScript code example shows how to use the **ItemIndex** method to get to the one **Win32\_OperatingSystem** without using a **For Each** loop.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery _
    ("Select * from Win32_OperatingSystem")

Wscript.Echo "Caption: " & colOperatingSystems.ItemIndex(0).Caption
```



<span data-ttu-id="853f7-135">Nell'esempio di codice VBScript seguente vengono ottenute le istanze associate a [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem), ad esempio [**\_ SystemOperatingSystem Win32**](/windows/desktop/CIMWin32Prov/win32-systemoperatingsystem).</span><span class="sxs-lookup"><span data-stu-id="853f7-135">The following VBScript code example gets instances associated with [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem), such as [**Win32\_SystemOperatingSystem**](/windows/desktop/CIMWin32Prov/win32-systemoperatingsystem).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colOS = _
    objWMIService.Execquery("Select * from Win32_OperatingSystem")
    Wscript.Echo  colOS.ItemIndex(0).Name

set colAssociators = colOS.ItemIndex(0).Associators_
    For Each Associator in colAssociators 
        Wscript.Echo Associator.Path_.RelPath  
    Next
```



<span data-ttu-id="853f7-136">Nell'output di esempio di codice riportato di seguito vengono mostrate le istanze associate a [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span><span class="sxs-lookup"><span data-stu-id="853f7-136">The following code example output shows instances associated with [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span></span>

``` syntax
Windows Server 2008 
    |C:\Windows|\Device\Harddisk0\Partition1
Win32_ComputerSystem.Name="Test1"
Win32_AutochkSetting.SettingID="Windows Server 2008 
    |C:\\Windows|\\Device\\Harddisk0\\Partition1"
```

## <a name="requirements"></a><span data-ttu-id="853f7-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="853f7-137">Requirements</span></span>



| <span data-ttu-id="853f7-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="853f7-138">Requirement</span></span> | <span data-ttu-id="853f7-139">Valore</span><span class="sxs-lookup"><span data-stu-id="853f7-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="853f7-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="853f7-140">Minimum supported client</span></span><br/> | <span data-ttu-id="853f7-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="853f7-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="853f7-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="853f7-142">Minimum supported server</span></span><br/> | <span data-ttu-id="853f7-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="853f7-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="853f7-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="853f7-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="853f7-145"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="853f7-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="853f7-146">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="853f7-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="853f7-147"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="853f7-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="853f7-148">DLL</span><span class="sxs-lookup"><span data-stu-id="853f7-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="853f7-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="853f7-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="853f7-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="853f7-150">CLSID</span></span><br/>                    | <span data-ttu-id="853f7-151">\_SWBEMOBJECTSET CLSID</span><span class="sxs-lookup"><span data-stu-id="853f7-151">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="853f7-152">IID</span><span class="sxs-lookup"><span data-stu-id="853f7-152">IID</span></span><br/>                      | <span data-ttu-id="853f7-153">\_ISWBEMOBJECTSET IID</span><span class="sxs-lookup"><span data-stu-id="853f7-153">IID\_ISWbemObjectSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="853f7-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="853f7-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="853f7-155">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="853f7-155">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

