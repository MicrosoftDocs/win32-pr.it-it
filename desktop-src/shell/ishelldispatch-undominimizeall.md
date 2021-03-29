---
description: Ripristina tutte le finestre desktop nello stato in cui si trovavano prima dell'ultimo comando MinimizeAll.
ms.assetid: 32BDE544-C4FF-4a64-99AF-F8960AEC4690
title: Metodo IShellDispatch. UndoMinimizeALL (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.UndoMinimizeALL
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1b11fdd7a0a82a11baa20b0f3a63a31a8a46b701
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527331"
---
# <a name="ishelldispatchundominimizeall-method"></a><span data-ttu-id="5180e-103">IShellDispatch. UndoMinimizeALL, metodo</span><span class="sxs-lookup"><span data-stu-id="5180e-103">IShellDispatch.UndoMinimizeALL method</span></span>

<span data-ttu-id="5180e-104">Ripristina tutte le finestre desktop nello stato in cui si trovavano prima dell'ultimo comando [**MinimizeAll**](shell-minimizeall.md) .</span><span class="sxs-lookup"><span data-stu-id="5180e-104">Restores all desktop windows to the state they were in before the last [**MinimizeAll**](shell-minimizeall.md) command.</span></span> <span data-ttu-id="5180e-105">Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e selezionare **Annulla Riduci a icona tutte le finestre** (nei sistemi meno recenti) o un secondo clic sull'icona **Mostra desktop** sulla barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="5180e-105">This method has the same effect as right-clicking the taskbar and selecting **Undo Minimize All Windows** (on older systems) or a second clicking of the **Show Desktop** icon in the taskbar.</span></span>

## <a name="syntax"></a><span data-ttu-id="5180e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5180e-106">Syntax</span></span>


```JScript
IShellDispatch.UndoMinimizeALL()
```


```VB

IShellDispatch.UndoMinimizeALL()
```





## <a name="parameters"></a><span data-ttu-id="5180e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5180e-107">Parameters</span></span>

<span data-ttu-id="5180e-108">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="5180e-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5180e-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5180e-109">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="5180e-110">JScript</span><span class="sxs-lookup"><span data-stu-id="5180e-110">JScript</span></span>

<span data-ttu-id="5180e-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="5180e-111">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="5180e-112">VB</span><span class="sxs-lookup"><span data-stu-id="5180e-112">VB</span></span>

<span data-ttu-id="5180e-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="5180e-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5180e-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5180e-114">Remarks</span></span>

<span data-ttu-id="5180e-115">Questo metodo viene implementato e accessibile tramite il metodo [**Shell. UndoMinimizeAll**](./shell-undominimizeall.md) .</span><span class="sxs-lookup"><span data-stu-id="5180e-115">This method is implemented and accessed through the [**Shell.UndoMinimizeAll**](./shell-undominimizeall.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="5180e-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="5180e-116">Examples</span></span>

<span data-ttu-id="5180e-117">Negli esempi seguenti viene illustrato l'utilizzo di **UndoMinimizeALL** in JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5180e-117">The following examples show the use of **UndoMinimizeALL** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="5180e-118">JScript</span><span class="sxs-lookup"><span data-stu-id="5180e-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellUndoMinimizeALLJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.UndoMinimizeALL();
    }
</script>
```



<span data-ttu-id="5180e-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="5180e-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellUndoMinimizeALLVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.UndoMinimizeALL

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="5180e-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="5180e-120">Visual Basic:</span></span>


```VB
Private Sub fnShellUndoMinimizeAllVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.UndoMinimizeALL

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="5180e-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5180e-121">Requirements</span></span>



| <span data-ttu-id="5180e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5180e-122">Requirement</span></span> | <span data-ttu-id="5180e-123">Valore</span><span class="sxs-lookup"><span data-stu-id="5180e-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5180e-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5180e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5180e-125">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5180e-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5180e-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5180e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5180e-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5180e-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5180e-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5180e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5180e-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5180e-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="5180e-130">IDL</span><span class="sxs-lookup"><span data-stu-id="5180e-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5180e-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5180e-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="5180e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5180e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5180e-133"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="5180e-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
