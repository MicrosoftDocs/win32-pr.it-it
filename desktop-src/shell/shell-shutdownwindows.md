---
description: Consente di visualizzare la finestra di dialogo arresta Windows. Equivale a fare clic sul menu Start e selezionare Arresta.
ms.assetid: 6fa8e2e0-a58f-4837-89f5-898cece2d80a
title: Metodo Shell. ShutdownWindows (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShutdownWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 804a1e211e191206d20f83d85dee2202492bfd27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232102"
---
# <a name="shellshutdownwindows-method"></a><span data-ttu-id="e8ff1-104">Shell. ShutdownWindows, metodo</span><span class="sxs-lookup"><span data-stu-id="e8ff1-104">Shell.ShutdownWindows method</span></span>

<span data-ttu-id="e8ff1-105">Consente di visualizzare la finestra di dialogo **arresta Windows** .</span><span class="sxs-lookup"><span data-stu-id="e8ff1-105">Displays the **Shut Down Windows** dialog box.</span></span> <span data-ttu-id="e8ff1-106">Equivale a fare clic sul menu **Start** e selezionare **Arresta**.</span><span class="sxs-lookup"><span data-stu-id="e8ff1-106">This is the same as clicking the **Start** menu and selecting **Shut Down**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8ff1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8ff1-107">Syntax</span></span>


```JScript
iRetVal = Shell.ShutdownWindows()
```


```VB

Shell.ShutdownWindows() As Integer
```





## <a name="parameters"></a><span data-ttu-id="e8ff1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8ff1-108">Parameters</span></span>

<span data-ttu-id="e8ff1-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e8ff1-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="e8ff1-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="e8ff1-110">Examples</span></span>

<span data-ttu-id="e8ff1-111">Nell'esempio seguente viene illustrato **ShutdownWindows** in uso.</span><span class="sxs-lookup"><span data-stu-id="e8ff1-111">The following example shows **ShutdownWindows** in use.</span></span> <span data-ttu-id="e8ff1-112">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e8ff1-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="e8ff1-113">JScript</span><span class="sxs-lookup"><span data-stu-id="e8ff1-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShutdownWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShutdownWindows();
    }
</script>
```



<span data-ttu-id="e8ff1-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="e8ff1-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellShutdownWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.ShutdownWindows

        set objShell = nothing
    end function
```



<span data-ttu-id="e8ff1-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="e8ff1-115">Visual Basic:</span></span>


```VB
Private Sub fnShellShutdownWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.ShutdownWindows

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="e8ff1-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8ff1-116">Requirements</span></span>



| <span data-ttu-id="e8ff1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8ff1-117">Requirement</span></span> | <span data-ttu-id="e8ff1-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e8ff1-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8ff1-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8ff1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e8ff1-120">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e8ff1-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e8ff1-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8ff1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e8ff1-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e8ff1-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e8ff1-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8ff1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8ff1-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8ff1-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e8ff1-125">IDL</span><span class="sxs-lookup"><span data-stu-id="e8ff1-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e8ff1-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e8ff1-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e8ff1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e8ff1-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8ff1-128"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="e8ff1-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




