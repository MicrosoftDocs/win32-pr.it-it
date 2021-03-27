---
description: Consente di visualizzare la finestra di dialogo Esegui all'utente.
ms.assetid: BC7C4C26-593D-4467-A2AA-4F2DF835C989
title: Metodo IShellDispatch. FileRun (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FileRun
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 56806edf06d334d90ad038886d955c00876f8f0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753095"
---
# <a name="ishelldispatchfilerun-method"></a><span data-ttu-id="6c494-103">IShellDispatch. FileRun, metodo</span><span class="sxs-lookup"><span data-stu-id="6c494-103">IShellDispatch.FileRun method</span></span>

<span data-ttu-id="6c494-104">Consente di visualizzare la finestra di dialogo **Esegui** all'utente.</span><span class="sxs-lookup"><span data-stu-id="6c494-104">Displays the **Run** dialog to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c494-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c494-105">Syntax</span></span>


```JScript
IShellDispatch.FileRun()
```


```VB

IShellDispatch.FileRun()
```





## <a name="parameters"></a><span data-ttu-id="6c494-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c494-106">Parameters</span></span>

<span data-ttu-id="6c494-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="6c494-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6c494-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6c494-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="6c494-109">JScript</span><span class="sxs-lookup"><span data-stu-id="6c494-109">JScript</span></span>

<span data-ttu-id="6c494-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="6c494-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="6c494-111">VB</span><span class="sxs-lookup"><span data-stu-id="6c494-111">VB</span></span>

<span data-ttu-id="6c494-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="6c494-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c494-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c494-113">Remarks</span></span>

<span data-ttu-id="6c494-114">Questo metodo viene implementato e accessibile tramite il metodo [**Shell. FileRun**](shell-filerun.md) .</span><span class="sxs-lookup"><span data-stu-id="6c494-114">This method is implemented and accessed through the [**Shell.FileRun**](shell-filerun.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="6c494-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="6c494-115">Examples</span></span>

<span data-ttu-id="6c494-116">Negli esempi seguenti viene illustrato l'utilizzo di **FileRun** in JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6c494-116">The following examples show the use of **FileRun** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="6c494-117">JScript</span><span class="sxs-lookup"><span data-stu-id="6c494-117">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFileRunJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FileRun();
    }
</script>
```



<span data-ttu-id="6c494-118">VBScript</span><span class="sxs-lookup"><span data-stu-id="6c494-118">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFileRunVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.FileRun

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="6c494-119">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="6c494-119">Visual Basic:</span></span>


```VB
Private Sub fnShellFileRunVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FileRun

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="6c494-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c494-120">Requirements</span></span>



| <span data-ttu-id="6c494-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c494-121">Requirement</span></span> | <span data-ttu-id="6c494-122">Valore</span><span class="sxs-lookup"><span data-stu-id="6c494-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c494-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c494-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6c494-124">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6c494-124">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6c494-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c494-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6c494-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6c494-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6c494-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6c494-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c494-128"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c494-128"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="6c494-129">IDL</span><span class="sxs-lookup"><span data-stu-id="6c494-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6c494-130"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6c494-130"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="6c494-131">DLL</span><span class="sxs-lookup"><span data-stu-id="6c494-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c494-132"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="6c494-132"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




