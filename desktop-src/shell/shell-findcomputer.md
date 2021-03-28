---
description: 'Consente di visualizzare la finestra di dialogo Risultati ricerca: computer. Nella finestra di dialogo viene visualizzato il risultato della ricerca di un computer specifico.'
ms.assetid: 0304b955-afde-4de4-824a-9ec9c9530360
title: Metodo Shell. FindComputer (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindComputer
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3824eeb98bfac11e007d1bf7dd9f89153a7b73ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980642"
---
# <a name="shellfindcomputer-method"></a><span data-ttu-id="46310-104">Shell. FindComputer, metodo</span><span class="sxs-lookup"><span data-stu-id="46310-104">Shell.FindComputer method</span></span>

<span data-ttu-id="46310-105">Consente di visualizzare la finestra di dialogo **Risultati ricerca: computer** .</span><span class="sxs-lookup"><span data-stu-id="46310-105">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="46310-106">Nella finestra di dialogo viene visualizzato il risultato della ricerca di un computer specifico.</span><span class="sxs-lookup"><span data-stu-id="46310-106">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="46310-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46310-107">Syntax</span></span>


```JScript
Shell.FindComputer()
```


```VB

Shell.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="46310-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="46310-108">Parameters</span></span>

<span data-ttu-id="46310-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="46310-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="46310-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46310-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="46310-111">JScript</span><span class="sxs-lookup"><span data-stu-id="46310-111">JScript</span></span>

<span data-ttu-id="46310-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="46310-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="46310-113">VB</span><span class="sxs-lookup"><span data-stu-id="46310-113">VB</span></span>

<span data-ttu-id="46310-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="46310-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="46310-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="46310-115">Examples</span></span>

<span data-ttu-id="46310-116">Nell'esempio seguente viene illustrato **FindComputer** in uso.</span><span class="sxs-lookup"><span data-stu-id="46310-116">The following example shows **FindComputer** in use.</span></span> <span data-ttu-id="46310-117">Il risultato di questo codice è identico a quello che si ottiene facendo clic sul pulsante **Start** , scegliendo **Cerca**, facendo clic sull'opzione **stampanti, computer o persone** , quindi facendo clic **su un computer in rete**.</span><span class="sxs-lookup"><span data-stu-id="46310-117">The result of this code is the same as pressing the **Start** button, clicking **Search**, clicking the **Printers, computers, or people** option, then clicking **A computer on the network**.</span></span> <span data-ttu-id="46310-118">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="46310-118">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="46310-119">JScript</span><span class="sxs-lookup"><span data-stu-id="46310-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindComputer();
    }
</script>
```



<span data-ttu-id="46310-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="46310-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objShell.FindComputer

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="46310-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="46310-121">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="46310-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46310-122">Requirements</span></span>



| <span data-ttu-id="46310-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="46310-123">Requirement</span></span> | <span data-ttu-id="46310-124">Valore</span><span class="sxs-lookup"><span data-stu-id="46310-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46310-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46310-125">Minimum supported client</span></span><br/> | <span data-ttu-id="46310-126">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="46310-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="46310-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46310-127">Minimum supported server</span></span><br/> | <span data-ttu-id="46310-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="46310-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="46310-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46310-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="46310-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="46310-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="46310-131">IDL</span><span class="sxs-lookup"><span data-stu-id="46310-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="46310-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="46310-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="46310-133">DLL</span><span class="sxs-lookup"><span data-stu-id="46310-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46310-134"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="46310-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




