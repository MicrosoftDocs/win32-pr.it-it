---
description: Espelle il computer dalla relativa stazione di ancoraggio. Questa operazione equivale a fare clic sul menu Start e selezionare Eject PC (Rimuovi PC) se il computer supporta questo comando.
ms.assetid: eaba3dce-8fea-453f-90c2-4a9b5cb05ecc
title: Metodo Shell. EjectPC (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.EjectPC
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 355d75b2ffaca9c9f90e66fbc535333a84bfa45d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979906"
---
# <a name="shellejectpc-method"></a><span data-ttu-id="95506-104">Shell. EjectPC, metodo</span><span class="sxs-lookup"><span data-stu-id="95506-104">Shell.EjectPC method</span></span>

<span data-ttu-id="95506-105">Espelle il computer dalla relativa stazione di ancoraggio.</span><span class="sxs-lookup"><span data-stu-id="95506-105">Ejects the computer from its docking station.</span></span> <span data-ttu-id="95506-106">Questa operazione equivale a fare clic sul menu **Start** e selezionare **eject PC (Rimuovi PC**) se il computer supporta questo comando.</span><span class="sxs-lookup"><span data-stu-id="95506-106">This is the same as clicking the **Start** menu and selecting **Eject PC**, if your computer supports this command.</span></span>

## <a name="syntax"></a><span data-ttu-id="95506-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="95506-107">Syntax</span></span>


```JScript
Shell.EjectPC()
```


```VB

Shell.EjectPC()
```





## <a name="parameters"></a><span data-ttu-id="95506-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="95506-108">Parameters</span></span>

<span data-ttu-id="95506-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="95506-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="95506-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="95506-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="95506-111">JScript</span><span class="sxs-lookup"><span data-stu-id="95506-111">JScript</span></span>

<span data-ttu-id="95506-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="95506-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="95506-113">VB</span><span class="sxs-lookup"><span data-stu-id="95506-113">VB</span></span>

<span data-ttu-id="95506-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="95506-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="95506-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="95506-115">Examples</span></span>

<span data-ttu-id="95506-116">Nell'esempio seguente viene illustrato **EjectPC** in uso.</span><span class="sxs-lookup"><span data-stu-id="95506-116">The following example shows **EjectPC** in use.</span></span> <span data-ttu-id="95506-117">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="95506-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="95506-118">JScript</span><span class="sxs-lookup"><span data-stu-id="95506-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellEjectPCJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.EjectPC();
    }
</script>
```



<span data-ttu-id="95506-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="95506-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellEjectPCVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.EjectPC

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="95506-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="95506-120">Visual Basic:</span></span>


```VB
Private Sub fnShellEjectPCVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.EjectPC

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="95506-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95506-121">Requirements</span></span>



| <span data-ttu-id="95506-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="95506-122">Requirement</span></span> | <span data-ttu-id="95506-123">Valore</span><span class="sxs-lookup"><span data-stu-id="95506-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95506-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95506-124">Minimum supported client</span></span><br/> | <span data-ttu-id="95506-125">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="95506-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="95506-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95506-126">Minimum supported server</span></span><br/> | <span data-ttu-id="95506-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="95506-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="95506-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="95506-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="95506-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="95506-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="95506-130">IDL</span><span class="sxs-lookup"><span data-stu-id="95506-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="95506-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="95506-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="95506-132">DLL</span><span class="sxs-lookup"><span data-stu-id="95506-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95506-133"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="95506-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




