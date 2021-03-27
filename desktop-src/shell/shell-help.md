---
description: Visualizza la guida e il supporto tecnico di Windows. Questo metodo ha lo stesso effetto di quando si fa clic sul menu Start e si seleziona Guida e supporto.
ms.assetid: fc13fef8-dac8-4c59-936d-8da0e63e06d4
title: Metodo Shell. Help (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Help
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: bfb4e9b3272355c41d13526d2e526515ff65d42b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231570"
---
# <a name="shellhelp-method"></a><span data-ttu-id="a9d7d-104">Shell. Help (metodo)</span><span class="sxs-lookup"><span data-stu-id="a9d7d-104">Shell.Help method</span></span>

<span data-ttu-id="a9d7d-105">Visualizza la guida e il supporto tecnico di Windows.</span><span class="sxs-lookup"><span data-stu-id="a9d7d-105">Displays the Windows Help and Support Center.</span></span> <span data-ttu-id="a9d7d-106">Questo metodo ha lo stesso effetto di quando si fa clic sul menu **Start** e si seleziona **Guida e supporto**.</span><span class="sxs-lookup"><span data-stu-id="a9d7d-106">This method has the same effect as clicking the **Start** menu and selecting **Help and Support**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9d7d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9d7d-107">Syntax</span></span>


```JScript
Shell.Help()
```


```VB

Shell.Help()
```





## <a name="parameters"></a><span data-ttu-id="a9d7d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a9d7d-108">Parameters</span></span>

<span data-ttu-id="a9d7d-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a9d7d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a9d7d-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a9d7d-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="a9d7d-111">JScript</span><span class="sxs-lookup"><span data-stu-id="a9d7d-111">JScript</span></span>

<span data-ttu-id="a9d7d-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a9d7d-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="a9d7d-113">VB</span><span class="sxs-lookup"><span data-stu-id="a9d7d-113">VB</span></span>

<span data-ttu-id="a9d7d-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a9d7d-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="a9d7d-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="a9d7d-115">Examples</span></span>

<span data-ttu-id="a9d7d-116">Nell'esempio seguente viene illustrata la **Guida** in uso.</span><span class="sxs-lookup"><span data-stu-id="a9d7d-116">The following example shows **Help** in use.</span></span> <span data-ttu-id="a9d7d-117">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a9d7d-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="a9d7d-118">JScript</span><span class="sxs-lookup"><span data-stu-id="a9d7d-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellHelpJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Help();
    }
</script>
```



<span data-ttu-id="a9d7d-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="a9d7d-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellHelpVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.Help

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="a9d7d-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="a9d7d-120">Visual Basic:</span></span>


```VB
Private Sub fnShellHelpVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.Help

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="a9d7d-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9d7d-121">Requirements</span></span>



| <span data-ttu-id="a9d7d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9d7d-122">Requirement</span></span> | <span data-ttu-id="a9d7d-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a9d7d-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9d7d-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9d7d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a9d7d-125">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a9d7d-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a9d7d-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9d7d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a9d7d-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a9d7d-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a9d7d-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9d7d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9d7d-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9d7d-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a9d7d-130">IDL</span><span class="sxs-lookup"><span data-stu-id="a9d7d-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a9d7d-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a9d7d-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a9d7d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a9d7d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9d7d-133"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="a9d7d-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




