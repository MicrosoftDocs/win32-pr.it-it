---
description: Simula una serie di caratteri tipizzati.
ms.assetid: 5D4C9F27-84AA-4131-A9A3-2C72DB2E8909
title: Metodo TypeText della classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeText
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 37e8227a545975a6193be63a8bd363e10e9805f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317181"
---
# <a name="typetext-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="67a64-103">Metodo TypeText della classe della \_ tastiera MSVM</span><span class="sxs-lookup"><span data-stu-id="67a64-103">TypeText method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="67a64-104">Simula una serie di caratteri tipizzati.</span><span class="sxs-lookup"><span data-stu-id="67a64-104">Simulates a series of typed characters.</span></span> <span data-ttu-id="67a64-105">Equivale a chiamare [**pulsanteper**](presskey-msvm-keyboard.md) seguito da [**ReleaseKey**](releasekey-msvm-keyboard.md) per ogni carattere della stringa.</span><span class="sxs-lookup"><span data-stu-id="67a64-105">This is equivalent to calling [**PressKey**](presskey-msvm-keyboard.md) followed by [**ReleaseKey**](releasekey-msvm-keyboard.md) for each character in the string.</span></span>

## <a name="syntax"></a><span data-ttu-id="67a64-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="67a64-106">Syntax</span></span>


```mof
uint32 TypeText(
  [in] string asciiText
);
```



## <a name="parameters"></a><span data-ttu-id="67a64-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="67a64-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67a64-108">*asciiText* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67a64-108">*asciiText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67a64-109">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="67a64-109">Type: **string**</span></span>

<span data-ttu-id="67a64-110">Serie di caratteri ASCII o Unicode da digitare.</span><span class="sxs-lookup"><span data-stu-id="67a64-110">The series of ASCII or Unicode characters to type.</span></span> <span data-ttu-id="67a64-111">La lunghezza massima di questa stringa dipende dal tipo di caratteri nella stringa.</span><span class="sxs-lookup"><span data-stu-id="67a64-111">The maximum length of this string depends on the type of characters in the string.</span></span>



| <span data-ttu-id="67a64-112">Tipo stringa</span><span class="sxs-lookup"><span data-stu-id="67a64-112">String type</span></span>        | <span data-ttu-id="67a64-113">Numero massimo di caratteri</span><span class="sxs-lookup"><span data-stu-id="67a64-113">Maximum characters</span></span>                                                               |
|--------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="67a64-114">ASCII</span><span class="sxs-lookup"><span data-stu-id="67a64-114">ASCII</span></span><br/>   | <span data-ttu-id="67a64-115">512</span><span class="sxs-lookup"><span data-stu-id="67a64-115">512</span></span><br/>                                                                   |
| <span data-ttu-id="67a64-116">Unicode</span><span class="sxs-lookup"><span data-stu-id="67a64-116">Unicode</span></span><br/> | <span data-ttu-id="67a64-117">da 256 a 512, a seconda del numero di coppie di surrogati nella stringa.</span><span class="sxs-lookup"><span data-stu-id="67a64-117">256 to 512, depending on the number of surrogate pairs in the string.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67a64-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="67a64-118">Return value</span></span>

<span data-ttu-id="67a64-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67a64-119">Type: **uint32**</span></span>

<span data-ttu-id="67a64-120">Un valore restituito pari a zero indica esito positivo.</span><span class="sxs-lookup"><span data-stu-id="67a64-120">A return value of zero indicates success.</span></span> <span data-ttu-id="67a64-121">Un valore restituito di uno indica un errore causato da caratteri non traducibili nella stringa di input.</span><span class="sxs-lookup"><span data-stu-id="67a64-121">A return value of one indicates a failure caused by nontranslatable characters in the input string.</span></span> <span data-ttu-id="67a64-122">Tutti gli altri valori diversi da zero indicano un errore di modifica dello stato della chiave.</span><span class="sxs-lookup"><span data-stu-id="67a64-122">All other nonzero values indicate a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="67a64-123">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="67a64-123">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="67a64-124">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="67a64-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="67a64-125">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="67a64-125">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="67a64-126">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="67a64-126">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="67a64-127">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="67a64-127">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="67a64-128">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="67a64-128">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="67a64-129">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="67a64-129">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="67a64-130">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="67a64-130">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="67a64-131">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="67a64-131">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="67a64-132">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="67a64-132">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="67a64-133">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="67a64-133">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="67a64-134">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="67a64-134">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="67a64-135">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="67a64-135">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="67a64-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="67a64-136">Remarks</span></span>

<span data-ttu-id="67a64-137">L'accesso alla classe della [**\_ tastiera MSVM**](msvm-keyboard.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="67a64-137">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="67a64-138">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="67a64-138">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="67a64-139">Esempio</span><span class="sxs-lookup"><span data-stu-id="67a64-139">Examples</span></span>

<span data-ttu-id="67a64-140">L'esempio C# seguente simula la digitazione di testo.</span><span class="sxs-lookup"><span data-stu-id="67a64-140">The following C# sample simulates typing text.</span></span> <span data-ttu-id="67a64-141">Le utilità a cui si fa riferimento sono disponibili in [utilità comuni per gli esempi di virtualizzazione (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="67a64-141">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class TypeTextClass
    {
        static ManagementObject GetComputerKeyboard(ManagementObject vm)
        {
            ManagementObjectCollection keyboardCollection = vm.GetRelated
            (
                "Msvm_Keyboard",
                "Msvm_SystemDevice",
                null,
                null,
                "PartComponent",
                "GroupComponent",
                false,
                null
            );

            ManagementObject keyboard = null;

            foreach (ManagementObject instance in keyboardCollection)
            {
                keyboard = instance;
                break;
            }

            return keyboard;
        }

        static void TypeText(string vmName, string text)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
            ManagementObject keyboard = GetComputerKeyboard(vm);

            ManagementBaseObject inParams = keyboard.GetMethodParameters("TypeText");

            inParams["asciiText"] = text;

            ManagementBaseObject outParams = keyboard.InvokeMethod("TypeText", inParams, null);

            if ((UInt16)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                string.Format("Text {0} was typed on {1}", text, vm["ElementName"]);
            }
            else
            {
                string.Format("Unable to type '{0}' on {1}", text, vm["ElementName"]);
            }

            inParams.Dispose();
            outParams.Dispose();
            keyboard.Dispose();
            vm.Dispose();
        }

        static void Main(string[] args)
        {
            if (args != null && args.Length != 2)
            {
                Console.WriteLine("Usage: TypeText vmName Text");
                return;
            }
            TypeText(args[0], args[1]);
        }
    }
}

```



<span data-ttu-id="67a64-142">Il seguente esempio di Visual Basic Scripting Edition (VBScript) simula la digitazione di testo.</span><span class="sxs-lookup"><span data-stu-id="67a64-142">The following Visual Basic Scripting Edition (VBScript) sample simulates typing text.</span></span>


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
    dim computer, objArgs, vmName, computerSystem, text, keyboard
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 2 then
       vmName= objArgs.Unnamed.Item(0)
       text = objArgs.Unnamed.Item(1)
    else
       WScript.Echo "usage: cscript TypeText.vbs vmName text"
       WScript.Quit
    end if
    
    set computerSystem = GetComputerSystem(vmName)
    set keyboard = GetComputerKeyboard(computerSystem)

    if TypeText(keyboard, text) then

        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "TypeText operation failed"
        WScript.Quit(1)
    end if

End Sub

'-----------------------------------------------------------------
' Retrieve Msvm_VirtualComputerSystem from base on its ElementName
' 
'-----------------------------------------------------------------
Function GetComputerSystem(vmElementName)
    dim query
    On Error Resume Next
    query = Format1("select * from Msvm_ComputerSystem where ElementName = '{0}'", vmElementName)
    set GetComputerSystem = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function


'-----------------------------------------------------------------
' Retrieve Msvm_Keyboard from given computer system
' 
'-----------------------------------------------------------------
Function GetComputerKeyboard(computerSystem)
    dim query
    On Error Resume Next
    query = Format1("ASSOCIATORS OF {{0}} WHERE resultClass = Msvm_Keyboard", computerSystem.Path_.Path)
    set GetComputerKeyboard = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function

'-----------------------------------------------------------------
' Type the given text to the given keyboard
'-----------------------------------------------------------------
Function TypeText(keyboard, text)
    WriteLog Format2("TypeText({0}, {1})", keyboard.ElementName, text)
    
    dim objInParam, objOutParams

    TypeText = false
    set objInParam = keyboard.Methods_("TypeText").InParameters.SpawnInstance_()
    objInParam.asciiText = text

    set objOutParams = keyboard.ExecMethod_("TypeText", objInParam)

    if objOutParams.ReturnValue = wmiSuccessful then
        WriteLog Format2("'{0}' was typed on {1}", text, keyboard.ElementName)
        TypeText = true
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\Typetext.log", 8, true)
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



## <a name="requirements"></a><span data-ttu-id="67a64-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67a64-143">Requirements</span></span>



| <span data-ttu-id="67a64-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="67a64-144">Requirement</span></span> | <span data-ttu-id="67a64-145">Valore</span><span class="sxs-lookup"><span data-stu-id="67a64-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67a64-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67a64-146">Minimum supported client</span></span><br/> | <span data-ttu-id="67a64-147">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="67a64-147">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="67a64-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67a64-148">Minimum supported server</span></span><br/> | <span data-ttu-id="67a64-149">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="67a64-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="67a64-150">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="67a64-150">Namespace</span></span><br/>                | <span data-ttu-id="67a64-151">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="67a64-151">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="67a64-152">MOF</span><span class="sxs-lookup"><span data-stu-id="67a64-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67a64-153"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67a64-153"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="67a64-154">DLL</span><span class="sxs-lookup"><span data-stu-id="67a64-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67a64-155"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="67a64-155"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="67a64-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67a64-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67a64-157">**\_Tastiera MSVM**</span><span class="sxs-lookup"><span data-stu-id="67a64-157">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

