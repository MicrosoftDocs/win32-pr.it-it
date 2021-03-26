---
description: Visualizza la finestra Guida e supporto tecnico di Windows. Questo metodo ha lo stesso effetto di quando si fa clic sul menu Start e si seleziona Guida e supporto.
ms.assetid: 9460C87E-6703-4df6-A84C-8D394E0E6703
title: Metodo IShellDispatch. Help (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Help
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b58bcc97748cecf6ab4064ecccf3ba5bbe190b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978098"
---
# <a name="ishelldispatchhelp-method"></a><span data-ttu-id="e7b1f-104">Metodo IShellDispatch. Help</span><span class="sxs-lookup"><span data-stu-id="e7b1f-104">IShellDispatch.Help method</span></span>

<span data-ttu-id="e7b1f-105">Visualizza la finestra Guida e supporto tecnico di Windows.</span><span class="sxs-lookup"><span data-stu-id="e7b1f-105">Displays the Windows Help and Support window.</span></span> <span data-ttu-id="e7b1f-106">Questo metodo ha lo stesso effetto di quando si fa clic sul menu **Start** e si seleziona **Guida e supporto**.</span><span class="sxs-lookup"><span data-stu-id="e7b1f-106">This method has the same effect as clicking the **Start** menu and selecting **Help and Support**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7b1f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7b1f-107">Syntax</span></span>


```JScript
IShellDispatch.Help()
```


```VB

IShellDispatch.Help()
```





## <a name="parameters"></a><span data-ttu-id="e7b1f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7b1f-108">Parameters</span></span>

<span data-ttu-id="e7b1f-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e7b1f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e7b1f-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e7b1f-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="e7b1f-111">JScript</span><span class="sxs-lookup"><span data-stu-id="e7b1f-111">JScript</span></span>

<span data-ttu-id="e7b1f-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e7b1f-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="e7b1f-113">VB</span><span class="sxs-lookup"><span data-stu-id="e7b1f-113">VB</span></span>

<span data-ttu-id="e7b1f-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e7b1f-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7b1f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7b1f-115">Remarks</span></span>

<span data-ttu-id="e7b1f-116">Questo metodo viene implementato e accessibile tramite il metodo [**Shell. Help**](shell-help.md) .</span><span class="sxs-lookup"><span data-stu-id="e7b1f-116">This method is implemented and accessed through the [**Shell.Help**](shell-help.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="e7b1f-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="e7b1f-117">Examples</span></span>

<span data-ttu-id="e7b1f-118">Negli esempi seguenti viene illustrato l'utilizzo della **Guida** in JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e7b1f-118">The following examples show the use of **Help** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="e7b1f-119">JScript</span><span class="sxs-lookup"><span data-stu-id="e7b1f-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellHelpJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Help();
    }
</script>
```



<span data-ttu-id="e7b1f-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="e7b1f-120">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnShellHelpVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Help

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="e7b1f-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="e7b1f-121">Visual Basic:</span></span>


```VB
Private Sub fnShellHelpVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.Help

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="e7b1f-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7b1f-122">Requirements</span></span>



| <span data-ttu-id="e7b1f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7b1f-123">Requirement</span></span> | <span data-ttu-id="e7b1f-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e7b1f-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7b1f-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7b1f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e7b1f-126">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e7b1f-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e7b1f-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7b1f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e7b1f-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e7b1f-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e7b1f-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7b1f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7b1f-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7b1f-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e7b1f-131">IDL</span><span class="sxs-lookup"><span data-stu-id="e7b1f-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e7b1f-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e7b1f-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e7b1f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e7b1f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7b1f-134"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="e7b1f-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




