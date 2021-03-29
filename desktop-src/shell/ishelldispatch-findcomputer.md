---
description: 'Consente di visualizzare la finestra di dialogo Risultati ricerca: computer. Nella finestra di dialogo viene visualizzato il risultato della ricerca di un computer specifico.'
ms.assetid: 9B687A8A-BB29-49a0-8AE3-11A75FAF3257
title: Metodo IShellDispatch. FindComputer (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FindComputer
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3ad928b6860a85126a714a08f3bc3df9d4aff67c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978111"
---
# <a name="ishelldispatchfindcomputer-method"></a><span data-ttu-id="0fd8f-104">IShellDispatch. FindComputer, metodo</span><span class="sxs-lookup"><span data-stu-id="0fd8f-104">IShellDispatch.FindComputer method</span></span>

<span data-ttu-id="0fd8f-105">Consente di visualizzare la finestra di dialogo **Risultati ricerca: computer** .</span><span class="sxs-lookup"><span data-stu-id="0fd8f-105">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="0fd8f-106">Nella finestra di dialogo viene visualizzato il risultato della ricerca di un computer specifico.</span><span class="sxs-lookup"><span data-stu-id="0fd8f-106">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fd8f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0fd8f-107">Syntax</span></span>


```JScript
IShellDispatch.FindComputer()
```


```VB

IShellDispatch.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="0fd8f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0fd8f-108">Parameters</span></span>

<span data-ttu-id="0fd8f-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0fd8f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0fd8f-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0fd8f-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="0fd8f-111">JScript</span><span class="sxs-lookup"><span data-stu-id="0fd8f-111">JScript</span></span>

<span data-ttu-id="0fd8f-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="0fd8f-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="0fd8f-113">VB</span><span class="sxs-lookup"><span data-stu-id="0fd8f-113">VB</span></span>

<span data-ttu-id="0fd8f-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="0fd8f-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fd8f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="0fd8f-115">Remarks</span></span>

<span data-ttu-id="0fd8f-116">Questo metodo viene implementato e accessibile tramite il metodo [**Shell. FindComputer**](shell-findcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="0fd8f-116">This method is implemented and accessed through the [**Shell.FindComputer**](shell-findcomputer.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="0fd8f-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="0fd8f-117">Examples</span></span>

<span data-ttu-id="0fd8f-118">Negli esempi seguenti viene illustrato l'utilizzo di **FindComputer** in JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0fd8f-118">The following examples show the use of **FindComputer** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="0fd8f-119">JScript</span><span class="sxs-lookup"><span data-stu-id="0fd8f-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FindComputer();
    }
</script>
```



<span data-ttu-id="0fd8f-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="0fd8f-120">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.FindComputer

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="0fd8f-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="0fd8f-121">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="0fd8f-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0fd8f-122">Requirements</span></span>



| <span data-ttu-id="0fd8f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fd8f-123">Requirement</span></span> | <span data-ttu-id="0fd8f-124">Valore</span><span class="sxs-lookup"><span data-stu-id="0fd8f-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fd8f-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0fd8f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0fd8f-126">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0fd8f-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0fd8f-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0fd8f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0fd8f-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0fd8f-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0fd8f-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0fd8f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fd8f-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fd8f-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="0fd8f-131">IDL</span><span class="sxs-lookup"><span data-stu-id="0fd8f-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0fd8f-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0fd8f-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="0fd8f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0fd8f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fd8f-134"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="0fd8f-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




