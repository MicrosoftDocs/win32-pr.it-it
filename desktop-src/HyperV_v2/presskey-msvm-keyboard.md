---
description: Simula la pressione di un tasto.
ms.assetid: 42C11F92-6143-40D7-9C07-56A6514EB4D1
title: Metodo pulsanteper della classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.PressKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5e9f196c5af3f8946460564e56bb425ffc24b51c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319504"
---
# <a name="presskey-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="61dda-103">Metodo pulsanteper della classe della \_ tastiera MSVM</span><span class="sxs-lookup"><span data-stu-id="61dda-103">PressKey method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="61dda-104">Simula la pressione di un tasto.</span><span class="sxs-lookup"><span data-stu-id="61dda-104">Simulates a key press.</span></span> <span data-ttu-id="61dda-105">In caso di esito positivo, la chiave sarà nello stato di inattività.</span><span class="sxs-lookup"><span data-stu-id="61dda-105">When successful the key will be in the down state.</span></span>

## <a name="syntax"></a><span data-ttu-id="61dda-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="61dda-106">Syntax</span></span>


```mof
uint32 PressKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a><span data-ttu-id="61dda-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="61dda-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61dda-108">*codice* \[ di stato in\]</span><span class="sxs-lookup"><span data-stu-id="61dda-108">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61dda-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="61dda-109">Type: **uint32**</span></span>

<span data-ttu-id="61dda-110">Codice della chiave virtuale della chiave da premere.</span><span class="sxs-lookup"><span data-stu-id="61dda-110">The virtual-key code of the key to press.</span></span> <span data-ttu-id="61dda-111">Per l'elenco dei codici delle chiavi virtuali, vedere [**codici a chiave virtuale**](../inputdev/virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="61dda-111">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61dda-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="61dda-112">Return value</span></span>

<span data-ttu-id="61dda-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="61dda-113">Type: **uint32**</span></span>

<span data-ttu-id="61dda-114">Un valore restituito pari a zero indica esito positivo.</span><span class="sxs-lookup"><span data-stu-id="61dda-114">A return value of zero indicates success.</span></span> <span data-ttu-id="61dda-115">Un valore diverso da zero indica un errore di modifica dello stato della chiave.</span><span class="sxs-lookup"><span data-stu-id="61dda-115">A nonzero value indicates a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="61dda-116">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="61dda-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="61dda-117">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="61dda-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="61dda-118">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="61dda-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="61dda-119">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="61dda-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="61dda-120">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="61dda-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="61dda-121">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="61dda-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="61dda-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="61dda-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="61dda-123">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="61dda-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="61dda-124">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="61dda-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="61dda-125">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="61dda-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="61dda-126">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="61dda-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="61dda-127">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="61dda-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="61dda-128">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="61dda-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="61dda-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="61dda-129">Remarks</span></span>

<span data-ttu-id="61dda-130">Il metodo **pulsanteper** esegue il mapping dei riferimenti al **\_ menu VK** (18), al **\_ controllo VK** (17) e al **\_ passaggio VK** (16) a **VK \_ LMENU** (164), **VK \_ LCONTROL** (162) e **VK \_ LSHIFT** (160), rispettivamente, perché i codici della chiave virtuale del **\_ menu VK**, del **\_ controllo** VK e del **VK \_ Shift** non rappresentano chiavi reali su una tastiera.</span><span class="sxs-lookup"><span data-stu-id="61dda-130">The **PressKey** method maps references to the **VK\_MENU** (18), **VK\_CONTROL** (17), and **VK\_SHIFT** (16) to **VK\_LMENU** (164), **VK\_LCONTROL** (162), and **VK\_LSHIFT** (160), respectively, because the **VK\_MENU**, **VK\_CONTROL**, and **VK\_SHIFT** virtual key codes do not represent real keys on a keyboard.</span></span>

<span data-ttu-id="61dda-131">L'accesso alla classe della [**\_ tastiera MSVM**](msvm-keyboard.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="61dda-131">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="61dda-132">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="61dda-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="61dda-133">Esempio</span><span class="sxs-lookup"><span data-stu-id="61dda-133">Examples</span></span>

<span data-ttu-id="61dda-134">L'esempio C# seguente simula la pressione di un tasto.</span><span class="sxs-lookup"><span data-stu-id="61dda-134">The following C# sample simulates a key press.</span></span> <span data-ttu-id="61dda-135">Le utilità a cui si fa riferimento sono disponibili in [utilità comuni per gli esempi di virtualizzazione (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="61dda-135">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class PressKeyClass
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

        static void PressKey(string vmName, int keyCode)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
            ManagementObject keyboard = GetComputerKeyboard(vm);

            ManagementBaseObject inParams = keyboard.GetMethodParameters("PressKey");

            inParams["keyCode"] = keyCode;

            ManagementBaseObject outParams = keyboard.InvokeMethod("PressKey", inParams, null);

            if ((UInt16)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                string.Format("Key {0} was pressed on {1}", keyCode, vm["ElementName"]);
            }
            else
            {
                string.Format("Unable to press key {0}' on {1}", keyCode, vm["ElementName"]);
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
                Console.WriteLine("Usage: PressKey vmName keyCode");
                return;
            }
            string vmName = args[0];
            int keyCode = int.Parse(args[1]);
            PressKey(args[0], keyCode);
        }

    }
}

```



<span data-ttu-id="61dda-136">Il seguente esempio di Visual Basic Scripting Edition (VBScript) simula una pressione di tasto.</span><span class="sxs-lookup"><span data-stu-id="61dda-136">The following Visual Basic Scripting Edition (VBScript) sample simulates a key press.</span></span>


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
    
    dim computer, objArgs, vmName, computerSystem, keycode, keyboard
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 2 then
       vmName= objArgs.Unnamed.Item(0)
       keycode = objArgs.Unnamed.Item(1)
    else
       WScript.Echo "usage: cscript PressKey.vbs vmName keycode"
       WScript.Quit
    end if
    
    set computerSystem = GetComputerSystem(vmName)
    set keyboard = GetComputerKeyboard(computerSystem)

    if PressKey(keyboard, keycode) then

        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "PressKey failed"
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
' Press the key with the given key code on the given keyboard
'-----------------------------------------------------------------
Function PressKey(keyboard, keyCode)
    WriteLog Format2("PressKey({0}, {1})", keyboard.ElementName, keyCode)
    
    dim objInParam, objOutParams
    
    PressKey = false
    set objInParam = keyboard.Methods_("PressKey").InParameters.SpawnInstance_()
    objInParam.keyCode = keyCode

    set objOutParams = keyboard.ExecMethod_("PressKey", objInParam)

    if objOutParams.ReturnValue = wmiSuccessful then
        WriteLog Format2("The key with code '{0}' is typed on {1}.", keyCode, keyboard.ElementName)
        PressKey = true
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\PressKey.log", 8, true)
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



## <a name="requirements"></a><span data-ttu-id="61dda-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61dda-137">Requirements</span></span>



| <span data-ttu-id="61dda-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="61dda-138">Requirement</span></span> | <span data-ttu-id="61dda-139">Valore</span><span class="sxs-lookup"><span data-stu-id="61dda-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61dda-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61dda-140">Minimum supported client</span></span><br/> | <span data-ttu-id="61dda-141">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="61dda-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="61dda-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61dda-142">Minimum supported server</span></span><br/> | <span data-ttu-id="61dda-143">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="61dda-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="61dda-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="61dda-144">Namespace</span></span><br/>                | <span data-ttu-id="61dda-145">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="61dda-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="61dda-146">MOF</span><span class="sxs-lookup"><span data-stu-id="61dda-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61dda-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61dda-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="61dda-148">DLL</span><span class="sxs-lookup"><span data-stu-id="61dda-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61dda-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="61dda-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="61dda-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61dda-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61dda-151">**\_Tastiera MSVM**</span><span class="sxs-lookup"><span data-stu-id="61dda-151">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="61dda-152">**Codici chiave virtuale**</span><span class="sxs-lookup"><span data-stu-id="61dda-152">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

