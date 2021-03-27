---
description: Consente di visualizzare la finestra di dialogo Esegui all'utente. Questo metodo ha lo stesso effetto di quando si fa clic sul menu Start e si seleziona Esegui.
ms.assetid: bb984777-e09f-41e6-8359-51c5291654f7
title: Metodo Shell. FileRun (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FileRun
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ebccf11ea21fdd4ceba2563a6110c1eb2494947b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980655"
---
# <a name="shellfilerun-method"></a><span data-ttu-id="584ba-104">Shell. FileRun, metodo</span><span class="sxs-lookup"><span data-stu-id="584ba-104">Shell.FileRun method</span></span>

<span data-ttu-id="584ba-105">Consente di visualizzare la finestra di dialogo **Esegui** all'utente.</span><span class="sxs-lookup"><span data-stu-id="584ba-105">Displays the **Run** dialog to the user.</span></span> <span data-ttu-id="584ba-106">Questo metodo ha lo stesso effetto di quando si fa clic sul menu **Start** e si seleziona **Esegui**.</span><span class="sxs-lookup"><span data-stu-id="584ba-106">This method has the same effect as clicking the **Start** menu and selecting **Run**.</span></span>

## <a name="syntax"></a><span data-ttu-id="584ba-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="584ba-107">Syntax</span></span>


```JScript
Shell.FileRun()
```


```VB

Shell.FileRun()
```





## <a name="parameters"></a><span data-ttu-id="584ba-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="584ba-108">Parameters</span></span>

<span data-ttu-id="584ba-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="584ba-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="584ba-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="584ba-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="584ba-111">JScript</span><span class="sxs-lookup"><span data-stu-id="584ba-111">JScript</span></span>

<span data-ttu-id="584ba-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="584ba-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="584ba-113">VB</span><span class="sxs-lookup"><span data-stu-id="584ba-113">VB</span></span>

<span data-ttu-id="584ba-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="584ba-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="584ba-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="584ba-115">Examples</span></span>

<span data-ttu-id="584ba-116">Nell'esempio seguente viene illustrato **FileRun** in uso.</span><span class="sxs-lookup"><span data-stu-id="584ba-116">The following example shows **FileRun** in use.</span></span> <span data-ttu-id="584ba-117">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="584ba-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="584ba-118">JScript</span><span class="sxs-lookup"><span data-stu-id="584ba-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFileRunJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FileRun();
    }
</script>
```



<span data-ttu-id="584ba-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="584ba-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFileRunVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.FileRun

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="584ba-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="584ba-120">Visual Basic:</span></span>


```VB
Private Sub fnShellFileRunVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FileRun

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="584ba-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="584ba-121">Requirements</span></span>



| <span data-ttu-id="584ba-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="584ba-122">Requirement</span></span> | <span data-ttu-id="584ba-123">Valore</span><span class="sxs-lookup"><span data-stu-id="584ba-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="584ba-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="584ba-124">Minimum supported client</span></span><br/> | <span data-ttu-id="584ba-125">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="584ba-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="584ba-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="584ba-126">Minimum supported server</span></span><br/> | <span data-ttu-id="584ba-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="584ba-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="584ba-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="584ba-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="584ba-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="584ba-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="584ba-130">IDL</span><span class="sxs-lookup"><span data-stu-id="584ba-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="584ba-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="584ba-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="584ba-132">DLL</span><span class="sxs-lookup"><span data-stu-id="584ba-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="584ba-133"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="584ba-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




