---
description: Consente di visualizzare la finestra di dialogo arresta Windows. Equivale a fare clic sul menu Start e selezionare Arresta.
ms.assetid: 3C4F6579-6398-4af4-8911-FE22555B0ABC
title: Metodo IShellDispatch. ShutdownWindows (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.ShutdownWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9c111e1b740857337953cdcdf81735a8c0568ba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993840"
---
# <a name="ishelldispatchshutdownwindows-method"></a><span data-ttu-id="cdc2a-104">IShellDispatch. ShutdownWindows, metodo</span><span class="sxs-lookup"><span data-stu-id="cdc2a-104">IShellDispatch.ShutdownWindows method</span></span>

<span data-ttu-id="cdc2a-105">Consente di visualizzare la finestra di dialogo **arresta Windows** .</span><span class="sxs-lookup"><span data-stu-id="cdc2a-105">Displays the **Shut Down Windows** dialog box.</span></span> <span data-ttu-id="cdc2a-106">Equivale a fare clic sul menu **Start** e selezionare **Arresta**.</span><span class="sxs-lookup"><span data-stu-id="cdc2a-106">This is the same as clicking the **Start** menu and selecting **Shut Down**.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdc2a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cdc2a-107">Syntax</span></span>


```JScript
IShellDispatch.ShutdownWindows()
```


```VB

IShellDispatch.ShutdownWindows()
```





## <a name="parameters"></a><span data-ttu-id="cdc2a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cdc2a-108">Parameters</span></span>

<span data-ttu-id="cdc2a-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="cdc2a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cdc2a-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cdc2a-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="cdc2a-111">JScript</span><span class="sxs-lookup"><span data-stu-id="cdc2a-111">JScript</span></span>

<span data-ttu-id="cdc2a-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="cdc2a-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="cdc2a-113">VB</span><span class="sxs-lookup"><span data-stu-id="cdc2a-113">VB</span></span>

<span data-ttu-id="cdc2a-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="cdc2a-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdc2a-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="cdc2a-115">Remarks</span></span>

<span data-ttu-id="cdc2a-116">Questo metodo viene implementato e accessibile tramite il metodo [**Shell. ShutdownWindows**](shell-shutdownwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="cdc2a-116">This method is implemented and accessed through the [**Shell.ShutdownWindows**](shell-shutdownwindows.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="cdc2a-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="cdc2a-117">Examples</span></span>

<span data-ttu-id="cdc2a-118">Nell'esempio seguente viene illustrato l'utilizzo di **ShutdownWindows** in JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="cdc2a-118">The following example shows the use of **ShutdownWindows** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="cdc2a-119">JScript</span><span class="sxs-lookup"><span data-stu-id="cdc2a-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShutdownWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.ShutdownWindows();
    }
</script>
```



<span data-ttu-id="cdc2a-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="cdc2a-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellShutdownWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.ShutdownWindows

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="cdc2a-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="cdc2a-121">Visual Basic:</span></span>


```VB
Private Sub fnShellShutdownWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.ShutdownWindows

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="cdc2a-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cdc2a-122">Requirements</span></span>



| <span data-ttu-id="cdc2a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdc2a-123">Requirement</span></span> | <span data-ttu-id="cdc2a-124">Valore</span><span class="sxs-lookup"><span data-stu-id="cdc2a-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdc2a-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdc2a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cdc2a-126">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cdc2a-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cdc2a-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdc2a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cdc2a-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cdc2a-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cdc2a-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cdc2a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdc2a-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdc2a-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="cdc2a-131">IDL</span><span class="sxs-lookup"><span data-stu-id="cdc2a-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cdc2a-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cdc2a-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="cdc2a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="cdc2a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdc2a-134"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="cdc2a-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




