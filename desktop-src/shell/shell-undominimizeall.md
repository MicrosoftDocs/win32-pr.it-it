---
description: Ripristina tutte le finestre desktop nello stesso stato in cui si trovavano prima dell'ultimo comando MinimizeAll.
ms.assetid: dcedfa18-6dde-4fb8-9679-4d6ff80249e4
title: Metodo Shell. UndoMinimizeALL (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.UndoMinimizeALL
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4a5010e4ac6b4fca42689f7c80db50c55ab2cb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232099"
---
# <a name="shellundominimizeall-method"></a><span data-ttu-id="3c2ce-103">Shell. UndoMinimizeALL, metodo</span><span class="sxs-lookup"><span data-stu-id="3c2ce-103">Shell.UndoMinimizeALL method</span></span>

<span data-ttu-id="3c2ce-104">Ripristina tutte le finestre desktop nello stesso stato in cui si trovavano prima dell'ultimo comando [**MinimizeAll**](shell-minimizeall.md) .</span><span class="sxs-lookup"><span data-stu-id="3c2ce-104">Restores all desktop windows to the same state they were in before the last [**MinimizeAll**](shell-minimizeall.md) command.</span></span> <span data-ttu-id="3c2ce-105">Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e selezionare **Annulla Riduci** a icona tutte le finestre nei sistemi meno recenti o un secondo clic sull'icona **Mostra desktop** nell'area avvio veloce della barra delle applicazioni in Windows 2000 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3c2ce-105">This method has the same effect as right-clicking the taskbar and selecting **Undo Minimize All Windows** on older systems or a second clicking of the **Show Desktop** icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c2ce-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c2ce-106">Syntax</span></span>


```JScript
iRetVal = Shell.UndoMinimizeALL()
```


```VB

Shell.UndoMinimizeALL() As Integer
```





## <a name="parameters"></a><span data-ttu-id="3c2ce-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c2ce-107">Parameters</span></span>

<span data-ttu-id="3c2ce-108">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="3c2ce-108">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="3c2ce-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="3c2ce-109">Examples</span></span>

<span data-ttu-id="3c2ce-110">Nell'esempio seguente viene illustrato **UndoMinimizeALL** in uso.</span><span class="sxs-lookup"><span data-stu-id="3c2ce-110">The following example shows **UndoMinimizeALL** in use.</span></span> <span data-ttu-id="3c2ce-111">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3c2ce-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="3c2ce-112">JScript</span><span class="sxs-lookup"><span data-stu-id="3c2ce-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellUndoMinimizeALLJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.UndoMinimizeALL();
    }
</script>
```



<span data-ttu-id="3c2ce-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="3c2ce-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellUndoMinimizeALLVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.UndoMinimizeALL

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="3c2ce-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="3c2ce-114">Visual Basic:</span></span>


```VB
Private Sub fnShellUndoMinimizeAllVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.UndoMinimizeALL

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="3c2ce-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c2ce-115">Requirements</span></span>



| <span data-ttu-id="3c2ce-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c2ce-116">Requirement</span></span> | <span data-ttu-id="3c2ce-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3c2ce-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c2ce-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c2ce-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3c2ce-119">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3c2ce-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3c2ce-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c2ce-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3c2ce-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3c2ce-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3c2ce-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c2ce-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c2ce-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c2ce-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="3c2ce-124">IDL</span><span class="sxs-lookup"><span data-stu-id="3c2ce-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3c2ce-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3c2ce-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="3c2ce-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3c2ce-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c2ce-127"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="3c2ce-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




