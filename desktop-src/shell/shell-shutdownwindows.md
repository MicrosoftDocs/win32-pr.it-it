---
description: 'Metodo Shell.ShutdownWindows : visualizza la finestra di dialogo Arresta Windows. Questo è lo stesso che fare clic sul menu Start e selezionare Arresta.'
ms.assetid: 6fa8e2e0-a58f-4837-89f5-898cece2d80a
title: Metodo Shell.ShutdownWindows (Shldisp.h)
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
ms.openlocfilehash: 2a3c0746caccb360f6f7f0156b72a57ed0a2d2b8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083669"
---
# <a name="shellshutdownwindows-method"></a><span data-ttu-id="65b12-104">Metodo Shell.ShutdownWindows</span><span class="sxs-lookup"><span data-stu-id="65b12-104">Shell.ShutdownWindows method</span></span>

<span data-ttu-id="65b12-105">Consente di visualizzare **la finestra di dialogo Arresta** Windows .</span><span class="sxs-lookup"><span data-stu-id="65b12-105">Displays the **Shut Down Windows** dialog box.</span></span> <span data-ttu-id="65b12-106">Si tratta di un'operazione identica a quando si fa clic sul menu **Start** e si **sceglie Arresta**.</span><span class="sxs-lookup"><span data-stu-id="65b12-106">This is the same as clicking the **Start** menu and selecting **Shut Down**.</span></span>

## <a name="syntax"></a><span data-ttu-id="65b12-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="65b12-107">Syntax</span></span>


```JScript
iRetVal = Shell.ShutdownWindows()
```


```VB

Shell.ShutdownWindows() As Integer
```





## <a name="parameters"></a><span data-ttu-id="65b12-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="65b12-108">Parameters</span></span>

<span data-ttu-id="65b12-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="65b12-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="65b12-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="65b12-110">Examples</span></span>

<span data-ttu-id="65b12-111">L'esempio seguente **mostra ShutdownWindows** in uso.</span><span class="sxs-lookup"><span data-stu-id="65b12-111">The following example shows **ShutdownWindows** in use.</span></span> <span data-ttu-id="65b12-112">Viene illustrato l'utilizzo corretto per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="65b12-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="65b12-113">Jscript:</span><span class="sxs-lookup"><span data-stu-id="65b12-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShutdownWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShutdownWindows();
    }
</script>
```



<span data-ttu-id="65b12-114">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="65b12-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellShutdownWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.ShutdownWindows

        set objShell = nothing
    end function
```



<span data-ttu-id="65b12-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="65b12-115">Visual Basic:</span></span>


```VB
Private Sub fnShellShutdownWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.ShutdownWindows

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="65b12-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65b12-116">Requirements</span></span>



| <span data-ttu-id="65b12-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="65b12-117">Requirement</span></span> | <span data-ttu-id="65b12-118">Valore</span><span class="sxs-lookup"><span data-stu-id="65b12-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65b12-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65b12-119">Minimum supported client</span></span><br/> | <span data-ttu-id="65b12-120">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="65b12-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="65b12-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65b12-121">Minimum supported server</span></span><br/> | <span data-ttu-id="65b12-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="65b12-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="65b12-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="65b12-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="65b12-124"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="65b12-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="65b12-125">Idl</span><span class="sxs-lookup"><span data-stu-id="65b12-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="65b12-126"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="65b12-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="65b12-127">DLL</span><span class="sxs-lookup"><span data-stu-id="65b12-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65b12-128"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="65b12-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




