---
description: Si sovrappone a tutte le finestre sul desktop. Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e selezionare Cascade Windows.
ms.assetid: 6A957D70-D6A3-4485-8DF3-7FD2C6DEFF78
title: Metodo IShellDispatch. CascadeWindows (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.CascadeWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4252e4df579bc73e9f082630f9f98b83e3b57f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130099"
---
# <a name="ishelldispatchcascadewindows-method"></a><span data-ttu-id="a905f-104">IShellDispatch. CascadeWindows, metodo</span><span class="sxs-lookup"><span data-stu-id="a905f-104">IShellDispatch.CascadeWindows method</span></span>

<span data-ttu-id="a905f-105">Si sovrappone a tutte le finestre sul desktop.</span><span class="sxs-lookup"><span data-stu-id="a905f-105">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="a905f-106">Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e selezionare **Cascade Windows**.</span><span class="sxs-lookup"><span data-stu-id="a905f-106">This method has the same effect as right-clicking the taskbar and selecting **Cascade windows**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a905f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a905f-107">Syntax</span></span>


```JScript
IShellDispatch.CascadeWindows()
```


```VB

IShellDispatch.CascadeWindows()
```





## <a name="parameters"></a><span data-ttu-id="a905f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a905f-108">Parameters</span></span>

<span data-ttu-id="a905f-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a905f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a905f-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a905f-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="a905f-111">JScript</span><span class="sxs-lookup"><span data-stu-id="a905f-111">JScript</span></span>

<span data-ttu-id="a905f-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a905f-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="a905f-113">VB</span><span class="sxs-lookup"><span data-stu-id="a905f-113">VB</span></span>

<span data-ttu-id="a905f-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a905f-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a905f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a905f-115">Remarks</span></span>

<span data-ttu-id="a905f-116">Questo metodo viene implementato e accessibile tramite il metodo [**Shell. CascadeWindows**](shell-cascadewindows.md) .</span><span class="sxs-lookup"><span data-stu-id="a905f-116">This method is implemented and accessed through the [**Shell.CascadeWindows**](shell-cascadewindows.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="a905f-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="a905f-117">Examples</span></span>

<span data-ttu-id="a905f-118">Negli esempi seguenti viene illustrato l'utilizzo di **CascadeWindows** in JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a905f-118">The following examples show the use of **CascadeWindows** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="a905f-119">JScript</span><span class="sxs-lookup"><span data-stu-id="a905f-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellCascadeWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.CascadeWindows();
    }
</script>
```



<span data-ttu-id="a905f-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="a905f-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellCascadeWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.CascadeWindows
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="a905f-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="a905f-121">Visual Basic:</span></span>


```VB
Private Sub fnShellCascadeWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.CascadeWindows
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="a905f-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a905f-122">Requirements</span></span>



| <span data-ttu-id="a905f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a905f-123">Requirement</span></span> | <span data-ttu-id="a905f-124">Valore</span><span class="sxs-lookup"><span data-stu-id="a905f-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a905f-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a905f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a905f-126">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a905f-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a905f-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a905f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a905f-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a905f-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a905f-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a905f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a905f-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a905f-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a905f-131">IDL</span><span class="sxs-lookup"><span data-stu-id="a905f-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a905f-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a905f-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a905f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a905f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a905f-134"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="a905f-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




