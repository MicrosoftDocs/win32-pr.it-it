---
description: Riduce al minimo tutte le finestre sul desktop. Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e selezionare Riduci a icona tutte le finestre nei sistemi meno recenti o facendo clic sull'icona Mostra desktop sulla barra delle applicazioni.
ms.assetid: 25DD56B0-221E-44a2-9FAD-FB358ADD7FF1
title: Metodo IShellDispatch. MinimizeAll (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.MinimizeAll
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b8b8f20ab82a6216a03d772151f852fd9c69b917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527342"
---
# <a name="ishelldispatchminimizeall-method"></a><span data-ttu-id="96d67-104">IShellDispatch. MinimizeAll, metodo</span><span class="sxs-lookup"><span data-stu-id="96d67-104">IShellDispatch.MinimizeAll method</span></span>

<span data-ttu-id="96d67-105">Riduce al minimo tutte le finestre sul desktop.</span><span class="sxs-lookup"><span data-stu-id="96d67-105">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="96d67-106">Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e selezionare **Riduci a icona tutte le finestre** nei sistemi meno recenti o facendo clic sull'icona **Mostra desktop** sulla barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="96d67-106">This method has the same effect as right-clicking the taskbar and selecting **Minimize All Windows** on older systems or clicking the **Show Desktop** icon on the taskbar.</span></span>

## <a name="syntax"></a><span data-ttu-id="96d67-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96d67-107">Syntax</span></span>


```JScript
IShellDispatch.MinimizeAll()
```


```VB

IShellDispatch.MinimizeAll()
```





## <a name="parameters"></a><span data-ttu-id="96d67-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="96d67-108">Parameters</span></span>

<span data-ttu-id="96d67-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="96d67-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="96d67-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96d67-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="96d67-111">JScript</span><span class="sxs-lookup"><span data-stu-id="96d67-111">JScript</span></span>

<span data-ttu-id="96d67-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="96d67-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="96d67-113">VB</span><span class="sxs-lookup"><span data-stu-id="96d67-113">VB</span></span>

<span data-ttu-id="96d67-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="96d67-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="96d67-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="96d67-115">Remarks</span></span>

<span data-ttu-id="96d67-116">Questo metodo viene implementato e accessibile tramite il metodo [**Shell. MinimizeAll**](shell-minimizeall.md) .</span><span class="sxs-lookup"><span data-stu-id="96d67-116">This method is implemented and accessed through the [**Shell.MinimizeAll**](shell-minimizeall.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="96d67-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="96d67-117">Examples</span></span>

<span data-ttu-id="96d67-118">Gli esempi seguenti illustrano l'uso di **MinimizeAll** in uso per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="96d67-118">The following examples show the use of **MinimizeAll** in use for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="96d67-119">JScript</span><span class="sxs-lookup"><span data-stu-id="96d67-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellMinimizeAllJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.MinimizeAll();
    }
</script>
```



<span data-ttu-id="96d67-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="96d67-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellMinimizeAllVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.MinimizeAll

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="96d67-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="96d67-121">Visual Basic:</span></span>


```VB
Private Sub fnShellMinimizeAllVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.MinimizeAll

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="96d67-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96d67-122">Requirements</span></span>



| <span data-ttu-id="96d67-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="96d67-123">Requirement</span></span> | <span data-ttu-id="96d67-124">Valore</span><span class="sxs-lookup"><span data-stu-id="96d67-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96d67-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96d67-125">Minimum supported client</span></span><br/> | <span data-ttu-id="96d67-126">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="96d67-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="96d67-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96d67-127">Minimum supported server</span></span><br/> | <span data-ttu-id="96d67-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="96d67-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="96d67-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96d67-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="96d67-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="96d67-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="96d67-131">IDL</span><span class="sxs-lookup"><span data-stu-id="96d67-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="96d67-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="96d67-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="96d67-133">DLL</span><span class="sxs-lookup"><span data-stu-id="96d67-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96d67-134"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="96d67-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96d67-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96d67-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96d67-136">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="96d67-136">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="96d67-137">**UndoMinimizeALL**</span><span class="sxs-lookup"><span data-stu-id="96d67-137">**UndoMinimizeALL**</span></span>](shell-undominimizeall.md)
</dt> </dl>

 

 




