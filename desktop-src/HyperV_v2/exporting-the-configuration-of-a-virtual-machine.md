---
description: Negli esempi seguenti di C# e Visual Basic Scripting Edition (VBScript) viene illustrata l'esportazione della configurazione di una macchina virtuale.
ms.assetid: 0B503B85-7EC0-409A-B610-E1C7FFBF3192
title: Esportazione della configurazione di una macchina virtuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e74a9984490c74be907f96ab408c64aa233ed09b
ms.sourcegitcommit: 3d9eb6638763fee8b87c378657458f814182e36c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320430"
---
# <a name="exporting-the-configuration-of-a-virtual-machine"></a><span data-ttu-id="62d15-103">Esportazione della configurazione di una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="62d15-103">Exporting the configuration of a virtual machine</span></span>

<span data-ttu-id="62d15-104">Negli esempi seguenti di C# e Visual Basic Scripting Edition (VBScript) viene illustrata l'esportazione della configurazione di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="62d15-104">The following C# and Visual Basic Scripting Edition (VBScript) samples demonstrate exporting the configuration of a virtual machine.</span></span> <span data-ttu-id="62d15-105">Gli esempi che mostrano l'esportazione di una macchina virtuale sono reperibili nella [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) ed [esportazione di uno snapshot di una macchina virtuale](exporting-virtual-machines.md) argomenti.</span><span class="sxs-lookup"><span data-stu-id="62d15-105">Samples that show exporting a virtual machine can be found on the [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) and [Exporting a snapshot of a virtual machine](exporting-virtual-machines.md) topics.</span></span>

<span data-ttu-id="62d15-106">Le utilità C# a cui si fa riferimento sono disponibili in [utilità comuni per gli esempi di virtualizzazione (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="62d15-106">The referenced C# utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
using System;
using System.IO;
using System.Management;

namespace HyperVSamples
{
    class ExportSystemDefinitionConfigOnlyClass
    {
        static string GetConfigOnlyVirtualSystemExportSettingDataInstance(ManagementScope scope)
        {
            ManagementPath settingPath = new ManagementPath("Msvm_VirtualSystemExportSettingData");

            ManagementClass exportSettingDataClass = new ManagementClass(scope, settingPath, null);
            ManagementObject exportSettingData = exportSettingDataClass.CreateInstance();

            // Do not copy VHDs and AVHDs but copy the Snapshot configuration and Saved State information (Runtime information) if present
            exportSettingData["CopySnapshotConfiguration"] = 0;
            exportSettingData["CopyVmRuntimeInformation"] = true;
            exportSettingData["CopyVmStorage"] = false;
            exportSettingData["CreateVmExportSubdirectory"] = true;

            string settingData = exportSettingData.GetText(TextFormat.CimDtd20);

            exportSettingData.Dispose();
            exportSettingDataClass.Dispose();

            return settingData;
        }


        static void ExportSystemDefinitionConfigOnly(string vmName, string exportDirectory)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");

            ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("ExportSystemDefinition");

            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
            inParams["ComputerSystem"] = vm.Path.Path;
            
            if (!Directory.Exists(exportDirectory))
            {
                Directory.CreateDirectory(exportDirectory);
            }
            inParams["ExportDirectory"] = exportDirectory;
            inParams["ExportSettingData"] = GetConfigOnlyVirtualSystemExportSettingDataInstance(scope);

            ManagementBaseObject outParams = virtualSystemService.InvokeMethod("ExportSystemDefinition", inParams, null);

            if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
            {
                if (Utility.JobCompleted(outParams, scope))
                {
                    Console.WriteLine("VM '{0}' were exported successfully.", vm["ElementName"]);

                }
                else
                {
                    Console.WriteLine("Failed to export VM");
                }
            }
            else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                Console.WriteLine("VM '{0}' were exported successfully.", vm["ElementName"]);
            }
            else
            {
                Console.WriteLine("Export virtual system failed with error:{0}", outParams["ReturnValue"]);
            }

            inParams.Dispose();
            outParams.Dispose();
            vm.Dispose();
            virtualSystemService.Dispose();
        }

        static void Main(string[] args)
        {
            if (args != null && args.Length != 2)
            {
                Console.WriteLine("Usage: ExportSystemDefinition vmName exportDirectory");
                return;
            }
            ExportSystemDefinitionConfigOnly(args[0], args[1]);
        }
    }
}
```


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

    dim computer, objArgs, vmName, vm, exportDirectory
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")
    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")
    set managementService = objWMIService.ExecQuery("select * from Msvm_VirtualSystemManagementService").ItemIndex(0)
    
    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 2 then
        vmName = objArgs.Unnamed.Item(0)
        exportDirectory = objArgs.Unnamed.Item(1)
    else
        WScript.Echo "usage: cscript ExportSystemDefinition.vbs vmName exportDirectoryName"
        WScript.Quit(1)
    end if
    
    set vm = GetComputerSystem(vmName)

    if ExportSystemDefinition(vm, exportDirectory) then
        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "ExportSystemDefinition Failed."
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
' Export a virtual system
'-----------------------------------------------------------------
Function ExportSystemDefinition(computerSystem, exportDirectory)

    dim objInParam, objOutParams 
    dim query
    dim computer
    dim exportSettingData
 
    ExportSystemDefinition = false
    
    if Not fileSystem.FolderExists(exportDirectory) then
        fileSystem.CreateFolder(exportDirectory)
    end if
    
    set objInParam = managementService.Methods_("ExportSystemDefinition").InParameters.SpawnInstance_()
    objInParam.ComputerSystem = computerSystem.Path_.Path

    query = Format1("ASSOCIATORS OF {{0}} WHERE resultClass = Msvm_VirtualSystemExportSettingData", computerSystem.Path_.Path)
    set exportSettingData = objWMIService.ExecQuery(query).ItemIndex(0)

    'Do not copy the VHDs and AVHDs, but copy the Saved state information and Snapshot configurations if present
    exportSettingData.CopyVmStorage = false
    exportSettingData.CopyVmRuntimeInformation = true
    exportSettingData.CreateVmExportSubdirectory = true
    exportSettingData.CopySnapshotConfiguration = 0

    objInParam.ExportSettingData = exportSettingData.GetText_(1)

    objInParam.ExportDirectory = exportDirectory
    
    set objOutParams = managementService.ExecMethod_("ExportSystemDefinition", objInParam)

    if objOutParams.ReturnValue = wmiStarted then
        if (WMIJobCompleted(objOutParams)) then
            ExportSystemDefinition = true
        end if
    elseif (objOutParams.ReturnValue = wmiSuccessful) then
        ExportSystemDefinition = true
    else
        WriteLog Format1("ExportSystemDefinition failed with ReturnValue {0}", objOutParams.ReturnValue)
    end if

End Function

'-----------------------------------------------------------------
' Handle wmi Job object
'-----------------------------------------------------------------
Function WMIJobCompleted(outParam)
    
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
    set fileStream = fileSystem.OpenTextFile(".\ExportSystemDefinitionLog.log", 8, true)
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





## <a name="related-topics"></a><span data-ttu-id="62d15-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="62d15-107">Related topics</span></span>

[<span data-ttu-id="62d15-108">Esportazione di uno snapshot di una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="62d15-108">Exporting a snapshot of a virtual machine</span></span>](exporting-virtual-machines.md)

[<span data-ttu-id="62d15-109">**ExportSystemDefinition**</span><span class="sxs-lookup"><span data-stu-id="62d15-109">**ExportSystemDefinition**</span></span>](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)
