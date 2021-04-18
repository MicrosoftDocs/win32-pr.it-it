---
description: Simula un clic del pulsante del dispositivo specificato.
ms.assetid: 1153BF91-F1F6-4E0A-8100-7625A3C73BB3
title: Metodo ClickButton della classe Msvm_SyntheticMouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.ClickButton
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2f5ea8e1f5984bd7e4b77222d6cbd8a05d1ed40b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313373"
---
# <a name="clickbutton-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="c825f-103">Metodo ClickButton della classe MSVM \_ SyntheticMouse</span><span class="sxs-lookup"><span data-stu-id="c825f-103">ClickButton method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="c825f-104">Simula un clic del pulsante del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="c825f-104">Simulates a button click of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="c825f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c825f-105">Syntax</span></span>


```mof
uint32 ClickButton(
  [in] uint32 buttonIndex
);
```



## <a name="parameters"></a><span data-ttu-id="c825f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c825f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c825f-107">*ButtonIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c825f-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c825f-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c825f-108">Type: **uint32**</span></span>

<span data-ttu-id="c825f-109">Indice in base 1 del pulsante.</span><span class="sxs-lookup"><span data-stu-id="c825f-109">The 1-based index of the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c825f-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c825f-110">Return value</span></span>

<span data-ttu-id="c825f-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c825f-111">Type: **uint32**</span></span>

<span data-ttu-id="c825f-112">Un valore restituito pari a zero indica esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c825f-112">A return value of zero indicates success.</span></span> <span data-ttu-id="c825f-113">Un valore diverso da zero indica un errore di modifica dello stato del pulsante.</span><span class="sxs-lookup"><span data-stu-id="c825f-113">A nonzero value indicates a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="c825f-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="c825f-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c825f-115">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="c825f-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c825f-116">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="c825f-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c825f-117">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="c825f-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c825f-118">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="c825f-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c825f-119">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="c825f-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c825f-120">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="c825f-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c825f-121">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="c825f-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c825f-122">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="c825f-122">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c825f-123">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="c825f-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c825f-124">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="c825f-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c825f-125">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="c825f-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c825f-126">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="c825f-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="c825f-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="c825f-127">Remarks</span></span>

<span data-ttu-id="c825f-128">L'accesso alla [**classe \_ SyntheticMouse di MSVM**](msvm-syntheticmouse.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="c825f-128">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c825f-129">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c825f-129">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="c825f-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="c825f-130">Examples</span></span>

<span data-ttu-id="c825f-131">L'esempio C# seguente simula un clic su un pulsante.</span><span class="sxs-lookup"><span data-stu-id="c825f-131">The following C# sample simulates a button click.</span></span> <span data-ttu-id="c825f-132">Le utilità a cui si fa riferimento sono disponibili in [utilità comuni per gli esempi di virtualizzazione (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="c825f-132">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class ClickButtonClass
    {
        static ManagementObject GetComputerMouse(ManagementObject vm)
        {
            ManagementObjectCollection mouseCollection = vm.GetRelated
            (
                "Msvm_SyntheticMouse",
                "Msvm_SystemDevice",
                null,
                null,
                "PartComponent",
                "GroupComponent",
                false,
                null
            );

            ManagementObject mouse = null;

            foreach (ManagementObject instance in mouseCollection)
            {
                mouse = instance;
                break;
            }

            return mouse;
        }

        static ManagementObject GetVideoHead(ManagementObject vm)
        {
            ManagementObjectCollection videoControllers = vm.GetRelated
             (
                 "Msvm_SyntheticDisplayController",
                 "Msvm_SystemDevice",
                 null,
                 null,
                 "PartComponent",
                 "GroupComponent",
                 false,
                 null
             );

            ManagementObject videoController = null;

            foreach (ManagementObject instance in videoControllers)
            {
                videoController = instance;
                break;
            }

            ManagementObjectCollection videoHeads = videoController.GetRelated
             (
                 "Msvm_VideoHead",
                 "Msvm_VideoHeadOnController",
                 null,
                 null,
                 "Dependent",
                 "Antecedent",
                 false,
                 null
             );

            ManagementObject videoHead = null;

            foreach (ManagementObject instance in videoHeads)
            {
                videoHead = instance;
                break;
            }

            videoController.Dispose();

            return videoHead;
        }

        static bool SetMousePosition(ManagementObject mouse, ManagementObject video)
        {
            bool passed = false;
            
            ManagementBaseObject inParams = mouse.GetMethodParameters("setAbsolutePosition");

            inParams["horizontalPosition"] = 1;
            inParams["verticalPosition"] = Convert.ToInt32(video["CurrentVerticalResolution"]) - 1;

            ManagementBaseObject outParams = mouse.InvokeMethod("setAbsolutePosition", inParams, null);

            if ((UInt16)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                Console.WriteLine("Mouse position is set at (1,{0})", inParams["verticalPosition"]);
                passed = true;
            }
            else
            {
                Console.WriteLine("setAbsolutePosition operation failed with {0} error.", outParams["ReturnValue"]);
            }

            inParams.Dispose();
            outParams.Dispose();

            return passed;

        }

        static void ClickButton(string vmName, int buttonIndex)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
            ManagementObject videoHead = GetVideoHead(vm);
            ManagementObject mouse = GetComputerMouse(vm);

            if (!SetMousePosition(mouse, videoHead))
            {
                return;
            }

            ManagementBaseObject inParams = mouse.GetMethodParameters("ClickButton");

            inParams["buttonIndex"] = buttonIndex;

            ManagementBaseObject outParams = mouse.InvokeMethod("ClickButton", inParams, null);

            if ((UInt16)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                string.Format("Button {0} was clicked on {1}", buttonIndex, vm["ElementName"]);
            }
            else
            {
                string.Format("Unable to click button {0}' on {1}", buttonIndex, vm["ElementName"]);
            }

            inParams.Dispose();
            outParams.Dispose();
            mouse.Dispose();
            vm.Dispose();
        }

        static void Main(string[] args)
        {
            if (args != null && args.Length != 2)
            {
                Console.WriteLine("Usage: ClickButton vmName buttonIndex");
                return;
            }
            ClickButton(args[0], Convert.ToInt32(args[1]));
        }
    }
}
```



<span data-ttu-id="c825f-133">Il seguente esempio di Visual Basic Scripting Edition (VBScript) simula un clic su un pulsante.</span><span class="sxs-lookup"><span data-stu-id="c825f-133">The following Visual Basic Scripting Edition (VBScript) sample simulates a button click.</span></span>


```VB
option explicit 

dim objWMIService
dim fileSystem

const wmiSuccessful = 0

Main()

'-----------------------------------------------------------------
' Main routine
'-----------------------------------------------------------------
Sub Main()
    
    dim vmName, computer, objArgs, mouse, video, computerSystem, buttonIndex
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 2 then
       vmName= objArgs.Unnamed.Item(0)
       buttonIndex = objArgs.Unnamed.Item(1)
    else
       WScript.Echo "usage: cscript ClickButton.vbs vmName buttonIndex"
       WScript.Quit
    end if
    
    set computerSystem = GetComputerSystem(vmName)
    set mouse = GetComputerMouse(computerSystem)
    set video = GetComputerVideoHead(computerSystem)

    if ClickButton(mouse, buttonIndex, video) then

        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "ClickButton failed"
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
' Retrieve Msvm_SyntheticMouse from given computer system
'-----------------------------------------------------------------
Function GetComputerMouse(computerSystem)
    On Error Resume Next
    dim query
    query = Format1("ASSOCIATORS OF {{0}} WHERE resultClass = Msvm_SyntheticMouse", computerSystem.Path_.Path)
    set GetComputerMouse = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function


'-----------------------------------------------------------------
' Retrieve Msvm_VideoHead from given computer system
'-----------------------------------------------------------------
Function GetComputerVideoHead(computerSystem)
    On Error Resume Next
    dim query, controller
    query = Format1("ASSOCIATORS OF {{0}} WHERE resultClass = Msvm_SyntheticDisplayController", computerSystem.Path_.Path)
    set controller = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
    
    query = Format1("ASSOCIATORS OF {{0}} WHERE resultClass = Msvm_VideoHead", controller.Path_.Path)
    set GetComputerVideoHead = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if    
End Function
'-----------------------------------------------------------------
' set mouse relative position on a virtual machine
'-----------------------------------------------------------------
Function setAbsolutePosition(mouse, video)
    WriteLog Format1("setAbsolutePosition({0})", mouse.ElementName)
    
    dim objInParam, objOutParams
    
    setAbsolutePosition = false
    set objInParam = mouse.Methods_("setAbsolutePosition").InParameters.SpawnInstance_()
    objInParam.horizontalPosition = 1
    objInParam.verticalPosition = video.CurrentVerticalResolution - 1

    set objOutParams = mouse.ExecMethod_("setAbsolutePosition", objInParam)

    if objOutParams.ReturnValue = wmiSuccessful then
        WriteLog Format1("Mouse position is set at (1,{0})", objInParam.verticalPosition)
        setAbsolutePosition = true
    end if

End Function

'-----------------------------------------------------------------
' Click mouse on a virtual machine
'-----------------------------------------------------------------
Function ClickButton(mouse, buttonIndex, video)
    WriteLog Format2("ClickButton({0}, {1})", mouse.ElementName, buttonIndex)
    
    dim objInParam, objOutParams
    
    ClickButton = false
    if Not setAbsolutePosition(mouse, video) then
        Exit Function
    end if


    set objInParam = mouse.Methods_("ClickButton").InParameters.SpawnInstance_()
    objInParam.buttonIndex = buttonIndex

    set objOutParams = mouse.ExecMethod_("ClickButton", objInParam)

    if objOutParams.ReturnValue = wmiSuccessful then
        WriteLog Format2("{0} button {1} was clicked.", mouse.ElementName, buttonIndex)
        ClickButton = true
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\clickButton.log", 8, true)
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



## <a name="requirements"></a><span data-ttu-id="c825f-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c825f-134">Requirements</span></span>



| <span data-ttu-id="c825f-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="c825f-135">Requirement</span></span> | <span data-ttu-id="c825f-136">Valore</span><span class="sxs-lookup"><span data-stu-id="c825f-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c825f-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c825f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c825f-138">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c825f-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c825f-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c825f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c825f-140">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c825f-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c825f-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c825f-141">Namespace</span></span><br/>                | <span data-ttu-id="c825f-142">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c825f-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c825f-143">MOF</span><span class="sxs-lookup"><span data-stu-id="c825f-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c825f-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c825f-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c825f-145">DLL</span><span class="sxs-lookup"><span data-stu-id="c825f-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c825f-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c825f-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c825f-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c825f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c825f-148">**\_SyntheticMouse MSVM**</span><span class="sxs-lookup"><span data-stu-id="c825f-148">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

