---
description: Consente di creare un file di disco floppy virtuale.
ms.assetid: C7B5712C-55DD-4784-8B2E-A8DE02E4CFD8
title: Metodo CreateVirtualFloppyDisk della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.CreateVirtualFloppyDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 98781a4f72218ee61a4966dc76b21f7417353e0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315919"
---
# <a name="createvirtualfloppydisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="72924-103">Metodo CreateVirtualFloppyDisk della classe MSVM \_ servizio</span><span class="sxs-lookup"><span data-stu-id="72924-103">CreateVirtualFloppyDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="72924-104">Consente di creare un file di disco floppy virtuale.</span><span class="sxs-lookup"><span data-stu-id="72924-104">Creates a virtual floppy disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="72924-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72924-105">Syntax</span></span>


```mof
uint32 CreateVirtualFloppyDisk(
  [in]  string              Path,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="72924-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="72924-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72924-107">*Percorso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72924-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72924-108">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="72924-108">Type: **string**</span></span>

<span data-ttu-id="72924-109">Percorso completo che specifica il percorso del nuovo file.</span><span class="sxs-lookup"><span data-stu-id="72924-109">A fully qualified path that specifies the location of the new file.</span></span>

</dd> <dt>

<span data-ttu-id="72924-110">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="72924-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72924-111">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="72924-111">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="72924-112">Riferimento al processo (può essere **null** se l'attività è stata completata).</span><span class="sxs-lookup"><span data-stu-id="72924-112">A reference to the job (can be **Null** if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72924-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="72924-113">Return value</span></span>

<span data-ttu-id="72924-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72924-114">Type: **uint32**</span></span>

<span data-ttu-id="72924-115">Questo metodo può restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="72924-115">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="72924-116">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="72924-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="72924-117">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="72924-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="72924-118">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="72924-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="72924-119">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="72924-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="72924-120">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="72924-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="72924-121">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="72924-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="72924-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="72924-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="72924-123">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="72924-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="72924-124">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="72924-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="72924-125">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="72924-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="72924-126">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="72924-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="72924-127">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="72924-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="72924-128">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="72924-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="72924-129">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="72924-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="72924-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="72924-130">Remarks</span></span>

<span data-ttu-id="72924-131">L'accesso alla [**classe \_ servizio di MSVM**](msvm-imagemanagementservice.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="72924-131">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="72924-132">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="72924-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="72924-133">Esempio</span><span class="sxs-lookup"><span data-stu-id="72924-133">Examples</span></span>

<span data-ttu-id="72924-134">Nell'esempio C# seguente viene creato un file di disco floppy virtuale.</span><span class="sxs-lookup"><span data-stu-id="72924-134">The following C# example creates a virtual floppy disk file.</span></span> <span data-ttu-id="72924-135">Le utilità a cui si fa riferimento sono disponibili in [utilità comuni per gli esempi di virtualizzazione (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="72924-135">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class CreateVFD
    {
        static void CreateVirtualFlopy(string vhdPath)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

            ManagementBaseObject inParams = imageService.GetMethodParameters("CreateVirtualFloppyDisk");
            inParams["Path"] = vhdPath;
            ManagementBaseObject outParams = imageService.InvokeMethod("CreateVirtualFloppyDisk", inParams, null);
            if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
            {
                if (Utility.JobCompleted(outParams, scope))
                {
                    Console.WriteLine("{0} was created successfully.", inParams["Path"]);
                }
                else
                {
                    Console.WriteLine("Unable to create {0}", inParams["Path"]);
                }
            }

            inParams.Dispose();
            outParams.Dispose();
            imageService.Dispose();
        }

        static void Main(string[] args)
        {
            if (args != null && args.Length != 1)
            {
                Console.WriteLine("Usage: CreateVFD path");
                return;
            }
            CreateVirtualFlopy(args[0]);
        }
    }
}

```



<span data-ttu-id="72924-136">Nell'esempio seguente Visual Basic Scripting Edition (VBScript) viene creato un file di disco floppy virtuale.</span><span class="sxs-lookup"><span data-stu-id="72924-136">The following Visual Basic Scripting Edition (VBScript) example creates a virtual floppy disk file.</span></span>


```VB
option explicit 

dim objWMIService
dim managementService
dim fileSystem


const JobStarting = 3
const JobRunning = 4
const JobCompleted = 7
const wmiStarted = 4096

const method = "CreateVirtualFloppyDisk"
Main()

'-----------------------------------------------------------------
' Main
'-----------------------------------------------------------------
Sub Main()

    dim computer, objArgs, vfdPath

    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")
    set managementService = objWMIService.ExecQuery("Select * from Msvm_ImageManagementService").ItemIndex(0)

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 1 then
       vfdPath = objArgs.Unnamed.Item(0)
    else
       WScript.Echo "usage: cscript CreateVFD.vbs VFDFilePath "
       WScript.Quit(1)
    end if

    if CreateVirtualFloppyDisk(vfdPath) then
        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "CreateVFD failed"
        WScript.Quit(1)
    end if

End Sub

'-----------------------------------------------------------------
' Execute CreateVirtualFloppyDisk method
'-----------------------------------------------------------------
Function CreateVirtualFloppyDisk(vfdPath)
    WriteLog Format1("Function CreateVirtualFloppyDisk({0})",  vfdPath)
    
    dim objInParam, objOutParams

    CreateVirtualFloppyDisk = false

    set objInParam = managementService.Methods_("CreateVirtualFloppyDisk").InParameters.SpawnInstance_()
    objInParam.Path = vfdPath

    set objOutParams = managementService.ExecMethod_("CreateVirtualFloppyDisk", objInParam)

    if (WMIMethodStarted(objOutParams)) then
        if (WMIJobCompleted(objOutParams)) then
            WriteLog Format1("VHD {0} was created successfully", vfdPath)
            CreateVirtualFloppyDisk = true
        end if
    end if

End Function


'-----------------------------------------------------------------
' Handle wmi return values
'-----------------------------------------------------------------
Function WMIMethodStarted(outParam)
    WriteLog "Function WMIMethodStarted"
    
    dim wmiStatus
    
    WMIMethodStarted = false

    if Not IsNull(outParam) then
        wmiStatus = outParam.ReturnValue

        if  wmiStatus = wmiStarted then
            WMIMethodStarted = true
        else
            WriteLog Format2("Failed to create VFD {0} ConcreteJob with error {1}", vfdPath, wmiStatus)
        end if
   end if

End Function

'-----------------------------------------------------------------
' Handle wmi Job object
'-----------------------------------------------------------------
Function WMIJobCompleted(outParam)
    WriteLog "Function WMIJobCompleted"
    dim WMIJob, jobState

    set WMIJob = objWMIService.Get(outParam.Job)

    WMIJobCompleted = true

    jobState = WMIJob.JobState

    while jobState = JobRunning or jobState = JobStarting
        WriteLog Format1("In progress... {0}% completed.",WMIJob.PercentComplete)
        WScript.Sleep(1000)
        set WMIJob = objWMIService.Get(outParam.Job)
        jobState = WMIJob.JobState
    wend

    if (jobState <> JobCompleted) then
        WriteLog Format1("ErrorCode:{0}", WMIJob.ErrorCode)
        WriteLog Format1("ErrorDescription:{0}", WMIJob.ErrorDescription)
        WMIJobCompleted = false
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\CreateVFD.log", 8, true)
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



## <a name="requirements"></a><span data-ttu-id="72924-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72924-137">Requirements</span></span>



| <span data-ttu-id="72924-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="72924-138">Requirement</span></span> | <span data-ttu-id="72924-139">Valore</span><span class="sxs-lookup"><span data-stu-id="72924-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72924-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72924-140">Minimum supported client</span></span><br/> | <span data-ttu-id="72924-141">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="72924-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="72924-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72924-142">Minimum supported server</span></span><br/> | <span data-ttu-id="72924-143">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="72924-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="72924-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="72924-144">Namespace</span></span><br/>                | <span data-ttu-id="72924-145">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="72924-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="72924-146">MOF</span><span class="sxs-lookup"><span data-stu-id="72924-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72924-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72924-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="72924-148">DLL</span><span class="sxs-lookup"><span data-stu-id="72924-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72924-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="72924-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="72924-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72924-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="72924-151">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="72924-151">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="72924-152">**\_Servizio MSVM**</span><span class="sxs-lookup"><span data-stu-id="72924-152">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

