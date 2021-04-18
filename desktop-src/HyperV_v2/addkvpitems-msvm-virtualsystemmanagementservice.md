---
description: Aggiunge coppie chiave-valore a una macchina virtuale.
ms.assetid: D952EC3D-24EB-4A68-8527-5BF522957CB6
title: Metodo AddKvpItems della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddKvpItems
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e9e01a02615b8bb395a589160a765dec4e08526e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312343"
---
# <a name="addkvpitems-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="219ef-103">Metodo AddKvpItems della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="219ef-103">AddKvpItems method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="219ef-104">Aggiunge coppie chiave-valore a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="219ef-104">Adds key-value pairs to a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="219ef-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="219ef-105">Syntax</span></span>


```mof
uint32 AddKvpItems(
  [in]  CIM_ComputerSystem REF TargetSystem,
  [in]  string                 DataItems[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="219ef-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="219ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="219ef-107">*TargetSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="219ef-107">*TargetSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="219ef-108">Tipo: **[ **CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span><span class="sxs-lookup"><span data-stu-id="219ef-108">Type: **[**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span></span>

<span data-ttu-id="219ef-109">Riferimento a un oggetto [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale in cui verranno aggiunte le coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="219ef-109">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object that represents the virtual machine on which the key-value pairs will be added.</span></span>

</dd> <dt>

<span data-ttu-id="219ef-110">*Elementi DataItem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="219ef-110">*DataItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="219ef-111">Tipo: **stringa \[ \]**</span><span class="sxs-lookup"><span data-stu-id="219ef-111">Type: **string\[\]**</span></span>

<span data-ttu-id="219ef-112">Matrice di coppie chiave-valore da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="219ef-112">An array of key-value pairs to be added.</span></span> <span data-ttu-id="219ef-113">Ogni elemento della matrice è un'istanza incorporata della classe [**MSVM \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) .</span><span class="sxs-lookup"><span data-stu-id="219ef-113">Each element of the array is an embedded instance of the [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) class.</span></span> <span data-ttu-id="219ef-114">Questo metodo ha esito negativo se una delle coppie chiave-valore specificate esiste già nel sistema di destinazione.</span><span class="sxs-lookup"><span data-stu-id="219ef-114">This method fails if any of the specified key-value pairs already exists on the target system.</span></span> <span data-ttu-id="219ef-115">Questa matrice può contenere al massimo 128 elementi.</span><span class="sxs-lookup"><span data-stu-id="219ef-115">This array can contain at most 128 elements.</span></span>

</dd> <dt>

<span data-ttu-id="219ef-116">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="219ef-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="219ef-117">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="219ef-117">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="219ef-118">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="219ef-118">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="219ef-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="219ef-119">Return value</span></span>

<span data-ttu-id="219ef-120">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="219ef-120">Type: **uint32**</span></span>

<span data-ttu-id="219ef-121">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="219ef-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="219ef-122">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="219ef-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="219ef-123">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="219ef-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="219ef-124">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="219ef-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="219ef-125">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="219ef-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="219ef-126">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="219ef-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="219ef-127">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="219ef-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="219ef-128">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="219ef-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="219ef-129">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="219ef-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="219ef-130">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="219ef-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="219ef-131">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="219ef-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="219ef-132">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="219ef-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="219ef-133">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="219ef-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="219ef-134">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="219ef-134">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="219ef-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="219ef-135">Remarks</span></span>

<span data-ttu-id="219ef-136">L'accesso alla [**classe \_ VirtualSystemManagementService di MSVM**](msvm-virtualsystemmanagementservice.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="219ef-136">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="219ef-137">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="219ef-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="219ef-138">Esempio</span><span class="sxs-lookup"><span data-stu-id="219ef-138">Examples</span></span>

<span data-ttu-id="219ef-139">Nell'esempio C# seguente vengono aggiunte coppie chiave-valore a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="219ef-139">The following C# sample adds key-value pairs to a virtual machine.</span></span> <span data-ttu-id="219ef-140">Le utilità a cui si fa riferimento sono disponibili in [utilità comuni per gli esempi di virtualizzazione (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="219ef-140">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="219ef-141">Per funzionare correttamente, il codice seguente deve essere eseguito sul server host della macchina virtuale e deve essere eseguito con privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="219ef-141">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
public static void AddKvpItems(string vmName, string itemName, string itemValue)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
    ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("AddKvpItems");
    ManagementClass kvpExchangeDataItem = new ManagementClass(scope, new ManagementPath("Msvm_KvpExchangeDataItem"), null);

    ManagementObject dataItem = kvpExchangeDataItem.CreateInstance();

    dataItem["Data"] = itemValue;
    dataItem["Name"] = itemName;
    dataItem["Source"] = 0;

    string[] dataItems = new string[1];
    dataItems[0] = dataItem.GetText(TextFormat.CimDtd20);

    ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
    inParams["TargetSystem"] = vm.Path.Path;
    inParams["DataItems"] = dataItems;

    ManagementBaseObject outParams = virtualSystemService.InvokeMethod("AddKvpItems", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("Resources were added successfully.");

        }
        else
        {
            Console.WriteLine("Failed to add resources");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        Console.WriteLine("Resources were added successfully.");
    }
    else
    {
        Console.WriteLine("Add virtual system Kvp items failed with error {0}", outParams["ReturnValue"]);
    }

    if (inParams != null)
    {
        inParams.Dispose();
    }

    if (outParams != null)
    {
        outParams.Dispose();
    }
}
```



<span data-ttu-id="219ef-142">Il seguente esempio di Visual Basic Scripting Edition (VBScript) aggiunge coppie chiave-valore a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="219ef-142">The following Visual Basic Scripting Edition (VBScript) sample adds key-value pairs to a virtual machine.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="219ef-143">Per funzionare correttamente, il codice seguente deve essere eseguito sul server host della macchina virtuale e deve essere eseguito con privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="219ef-143">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```VB
option explicit 

dim objWMIService
dim managementService
dim fileSystem


const JobStarting = 3
const JobRunning = 4
const JobCompleted = 7
const wmiStarted = 4096
const wmiSuccessful = 0

Main()

'-----------------------------------------------------------------
' Main
'-----------------------------------------------------------------
Sub Main()

    dim computer, vmName, itemName, itemValue, myVm, objArgs
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."

    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")
    set managementService = objWMIService.ExecQuery("select * from Msvm_VirtualSystemManagementService").ItemIndex(0)

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 3 then
        vmName = objArgs.Unnamed.Item(0)
        itemName = objArgs.Unnamed.Item(1)
        itemValue = objArgs.Unnamed.Item(2)
    else
        WScript.Echo "usage: cscript AddKvpItems.vbs vmName itemName itemValue"
        WScript.Quit(1)
    end if

    set myVm = GetComputerSystem(vmName)

    if AddKvpItems(myVm, itemName, itemValue) then

        WriteLog "Done"
        WScript.Quit(0)

    else
        WriteLog "AddKvpItems failed"
        WScript.Quit(1)
    end if

End Sub

'-----------------------------------------------------------------
' Retrieve Msvm_VirtualComputerSystem from base on its ElementName
'-----------------------------------------------------------------
Function GetComputerSystem(vmElementName)
    On Error Resume Next
    dim query
    query = Format1("select * from Msvm_ComputerSystem where ElementName = '{0}'", vmElementName)
    set GetComputerSystem = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function


'-----------------------------------------------------------------
' AddKvpItems
'-----------------------------------------------------------------
Function AddKvpItems(computerSystem, itemName, itemValue)

    dim dataItem, dataItems, objInParam, objOutParams
    
    AddKvpItems = false
    
    set dataItem = objWMIService.Get("Msvm_KvpExchangeDataItem").SpawnInstance_()
    dataItem.Data = itemValue
    dataItem.Name = itemName
    dataItem.Source = 0
    
    dataItems = Array(1)
    dataItems(0) = dataItem.GetText_(1)
    
    set objInParam = managementService.Methods_("AddKvpItems").InParameters.SpawnInstance_()
    objInParam.TargetSystem = computerSystem.Path_.Path
    objInParam.DataItems = dataItems
    
    set objOutParams = managementService.ExecMethod_("AddKvpItems", objInParam)

    if objOutParams.ReturnValue = wmiStarted then
        if (WMIJobCompleted(objOutParams)) then
            AddKvpItems = true
        end if
    elseif (objOutParams.ReturnValue = wmiSuccessful) then
        AddKvpItems = true
    else
        WriteLog Format1("AddKvpItem failed with error {0}", objOutParams.ReturnValue)
    end if

End Function


'-----------------------------------------------------------------
' Handle wmi Job object
'-----------------------------------------------------------------
Function WMIJobCompleted(outParam)
    
    dim WMIJob, jobState
    WMIJobCompleted = true

    set WMIJob = objWMIService.Get(outParam.Job)
    
    jobState = WMIJob.JobState

    while jobState = JobRunning or jobState = JobStarting
        WriteLog Format1("In progress... {0}% completed.",WMIJob.PercentComplete)
        WScript.Sleep(1000)
        set WMIJob = objWMIService.Get(outParam.Job)
        jobState = WMIJob.JobState
    wend

    if (WMIJob.JobState <> JobCompleted) then
        WriteLog Format1("ErrorDescription:{0}", WMIJob.ErrorDescription)
        WriteLog Format1("ErrorCode:{0}", WMIJob.ErrorCode)
        WMIJobCompleted = false
    end if
    
End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\AddKvpItems.log", 8, true)
    WScript.Echo line
    fileStream.WriteLine line
    fileStream.Close

End Sub


'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format2(myString, arg0, arg1)
    Format2 = Format1(myString, arg0)
    Format2 = Replace(Format2, "{1}", arg1)
End Function

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format1(myString, arg0)
    Format1 = Replace(myString, "{0}", arg0)
End Function
```



## <a name="requirements"></a><span data-ttu-id="219ef-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="219ef-144">Requirements</span></span>



| <span data-ttu-id="219ef-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="219ef-145">Requirement</span></span> | <span data-ttu-id="219ef-146">Valore</span><span class="sxs-lookup"><span data-stu-id="219ef-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="219ef-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="219ef-147">Minimum supported client</span></span><br/> | <span data-ttu-id="219ef-148">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="219ef-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="219ef-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="219ef-149">Minimum supported server</span></span><br/> | <span data-ttu-id="219ef-150">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="219ef-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="219ef-151">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="219ef-151">Namespace</span></span><br/>                | <span data-ttu-id="219ef-152">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="219ef-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="219ef-153">MOF</span><span class="sxs-lookup"><span data-stu-id="219ef-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="219ef-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="219ef-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="219ef-155">DLL</span><span class="sxs-lookup"><span data-stu-id="219ef-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="219ef-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="219ef-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="219ef-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="219ef-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="219ef-158">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="219ef-158">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

