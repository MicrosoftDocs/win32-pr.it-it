---
description: Espelle il computer dalla relativa stazione di ancoraggio. Questa operazione equivale a fare clic sul menu Start e selezionare Eject PC (Rimuovi PC) se il computer supporta questo comando.
ms.assetid: 34448D82-187C-40aa-90B4-A4111B33048B
title: Metodo IShellDispatch. EjectPC (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.EjectPC
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d85dd8c007338dca3d68183bc9ba3fbd333195ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226368"
---
# <a name="ishelldispatchejectpc-method"></a><span data-ttu-id="809d2-104">IShellDispatch. EjectPC, metodo</span><span class="sxs-lookup"><span data-stu-id="809d2-104">IShellDispatch.EjectPC method</span></span>

<span data-ttu-id="809d2-105">Espelle il computer dalla relativa stazione di ancoraggio.</span><span class="sxs-lookup"><span data-stu-id="809d2-105">Ejects the computer from its docking station.</span></span> <span data-ttu-id="809d2-106">Questa operazione equivale a fare clic sul menu **Start** e selezionare **eject PC (Rimuovi PC**) se il computer supporta questo comando.</span><span class="sxs-lookup"><span data-stu-id="809d2-106">This is the same as clicking the **Start** menu and selecting **Eject PC**, if your computer supports this command.</span></span>

## <a name="syntax"></a><span data-ttu-id="809d2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="809d2-107">Syntax</span></span>


```JScript
IShellDispatch.EjectPC()
```


```VB

IShellDispatch.EjectPC()
```





## <a name="parameters"></a><span data-ttu-id="809d2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="809d2-108">Parameters</span></span>

<span data-ttu-id="809d2-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="809d2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="809d2-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="809d2-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="809d2-111">JScript</span><span class="sxs-lookup"><span data-stu-id="809d2-111">JScript</span></span>

<span data-ttu-id="809d2-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="809d2-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="809d2-113">VB</span><span class="sxs-lookup"><span data-stu-id="809d2-113">VB</span></span>

<span data-ttu-id="809d2-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="809d2-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="809d2-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="809d2-115">Remarks</span></span>

<span data-ttu-id="809d2-116">Questo metodo viene implementato e accessibile tramite il metodo [**Shell. EjectPC**](shell-ejectpc.md) .</span><span class="sxs-lookup"><span data-stu-id="809d2-116">This method is implemented and accessed through the [**Shell.EjectPC**](shell-ejectpc.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="809d2-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="809d2-117">Examples</span></span>

<span data-ttu-id="809d2-118">Negli esempi seguenti viene illustrato l'utilizzo di **EjectPC** in JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="809d2-118">The following examples show the use of **EjectPC** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="809d2-119">JScript</span><span class="sxs-lookup"><span data-stu-id="809d2-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellEjectPCJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.EjectPC();
    }
</script>
```



<span data-ttu-id="809d2-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="809d2-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellEjectPCVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.EjectPC

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="809d2-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="809d2-121">Visual Basic:</span></span>


```VB
Private Sub fnShellEjectPCVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.EjectPC

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="809d2-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="809d2-122">Requirements</span></span>



| <span data-ttu-id="809d2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="809d2-123">Requirement</span></span> | <span data-ttu-id="809d2-124">Valore</span><span class="sxs-lookup"><span data-stu-id="809d2-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="809d2-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="809d2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="809d2-126">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="809d2-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="809d2-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="809d2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="809d2-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="809d2-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="809d2-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="809d2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="809d2-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="809d2-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="809d2-131">IDL</span><span class="sxs-lookup"><span data-stu-id="809d2-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="809d2-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="809d2-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="809d2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="809d2-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="809d2-134"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="809d2-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




