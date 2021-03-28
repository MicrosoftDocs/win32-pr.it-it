---
description: Si sovrappone a tutte le finestre sul desktop. Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e selezionare Cascade Windows.
ms.assetid: f73d2066-4626-455b-8ee6-f7004cc9e699
title: Metodo Shell. CascadeWindows (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.CascadeWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 751182ec53e0495021f4a6e2fad355c2c700ad66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529418"
---
# <a name="shellcascadewindows-method"></a><span data-ttu-id="e353f-104">Shell. CascadeWindows, metodo</span><span class="sxs-lookup"><span data-stu-id="e353f-104">Shell.CascadeWindows method</span></span>

<span data-ttu-id="e353f-105">Si sovrappone a tutte le finestre sul desktop.</span><span class="sxs-lookup"><span data-stu-id="e353f-105">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="e353f-106">Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e selezionare **Cascade Windows**.</span><span class="sxs-lookup"><span data-stu-id="e353f-106">This method has the same effect as right-clicking the taskbar and selecting **Cascade Windows**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e353f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e353f-107">Syntax</span></span>


```JScript
Shell.CascadeWindows()
```


```VB

Shell.CascadeWindows()
```





## <a name="parameters"></a><span data-ttu-id="e353f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e353f-108">Parameters</span></span>

<span data-ttu-id="e353f-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e353f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e353f-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e353f-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="e353f-111">JScript</span><span class="sxs-lookup"><span data-stu-id="e353f-111">JScript</span></span>

<span data-ttu-id="e353f-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e353f-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="e353f-113">VB</span><span class="sxs-lookup"><span data-stu-id="e353f-113">VB</span></span>

<span data-ttu-id="e353f-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e353f-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="e353f-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="e353f-115">Examples</span></span>

<span data-ttu-id="e353f-116">Nell'esempio seguente viene illustrato **CascadeWindows** in uso.</span><span class="sxs-lookup"><span data-stu-id="e353f-116">The following example shows **CascadeWindows** in use.</span></span> <span data-ttu-id="e353f-117">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e353f-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="e353f-118">JScript</span><span class="sxs-lookup"><span data-stu-id="e353f-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellCascadeWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.CascadeWindows();
    }
</script>
```



<span data-ttu-id="e353f-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="e353f-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellCascadeWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.CascadeWindows
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="e353f-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="e353f-120">Visual Basic:</span></span>


```VB
Private Sub fnShellCascadeWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.CascadeWindows
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="e353f-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e353f-121">Requirements</span></span>



| <span data-ttu-id="e353f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e353f-122">Requirement</span></span> | <span data-ttu-id="e353f-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e353f-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e353f-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e353f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e353f-125">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e353f-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e353f-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e353f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e353f-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e353f-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e353f-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e353f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e353f-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e353f-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e353f-130">IDL</span><span class="sxs-lookup"><span data-stu-id="e353f-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e353f-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e353f-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e353f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e353f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e353f-133"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="e353f-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




