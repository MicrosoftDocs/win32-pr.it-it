---
description: 'Metodo IShellDispatch4.ToggleDesktop: visualizza o nasconde il desktop.'
title: Metodo IShellDispatch4.ToggleDesktop (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.ToggleDesktop
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 60199e18-b8da-48a6-b316-e7f07ff44b78
ms.openlocfilehash: e78c14e2aa7f918ff27b21bdab0ce71bed08a84a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840932"
---
# <a name="ishelldispatch4toggledesktop-method"></a><span data-ttu-id="fa825-103">Metodo IShellDispatch4.ToggleDesktop</span><span class="sxs-lookup"><span data-stu-id="fa825-103">IShellDispatch4.ToggleDesktop method</span></span>

<span data-ttu-id="fa825-104">Visualizza o nasconde il desktop.</span><span class="sxs-lookup"><span data-stu-id="fa825-104">Displays or hides the desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa825-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa825-105">Syntax</span></span>


```JScript
IShellDispatch4.ToggleDesktop()
```


```VB

IShellDispatch4.ToggleDesktop()
```





## <a name="parameters"></a><span data-ttu-id="fa825-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fa825-106">Parameters</span></span>

<span data-ttu-id="fa825-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="fa825-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa825-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fa825-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="fa825-109">JScript</span><span class="sxs-lookup"><span data-stu-id="fa825-109">JScript</span></span>

<span data-ttu-id="fa825-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="fa825-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="fa825-111">VB</span><span class="sxs-lookup"><span data-stu-id="fa825-111">VB</span></span>

<span data-ttu-id="fa825-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="fa825-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa825-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="fa825-113">Remarks</span></span>

<span data-ttu-id="fa825-114">Questo metodo ha lo stesso effetto del **pulsante Mostra desktop** sulla barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="fa825-114">This method has the same effect as the **Show Desktop** button on the taskbar.</span></span> <span data-ttu-id="fa825-115">Nasconde tutte le finestre aperte per visualizzare il desktop oppure nasconde il desktop visualizzando tutte le finestre aperte.</span><span class="sxs-lookup"><span data-stu-id="fa825-115">It either hides all open windows to show the desktop or it hides the desktop by showing all open windows.</span></span> <span data-ttu-id="fa825-116">Il **metodo ToggleDesktop** non visualizza un'interfaccia utente, ma richiama solo l'azione toggle.</span><span class="sxs-lookup"><span data-stu-id="fa825-116">The **ToggleDesktop** method does not display a user interface, it just invokes the toggle action.</span></span>

## <a name="examples"></a><span data-ttu-id="fa825-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="fa825-117">Examples</span></span>

<span data-ttu-id="fa825-118">Gli esempi seguenti illustrano l'uso corretto di **ToggleDesktop** per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="fa825-118">The following examples show the proper use of **ToggleDesktop** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="fa825-119">Jscript:</span><span class="sxs-lookup"><span data-stu-id="fa825-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ToggleDesktopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ToggleDesktop();
    }
</script>
```



<span data-ttu-id="fa825-120">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="fa825-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIShellDispatch4ToggleDesktopVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objShell.ToggleDesktop
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="fa825-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="fa825-121">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ToggleDesktopVB()
    Dim objShell As Shell
            
    Set objShell = New Shell
        objShell.ToggleDesktop
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="fa825-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa825-122">Requirements</span></span>



| <span data-ttu-id="fa825-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa825-123">Requirement</span></span> | <span data-ttu-id="fa825-124">Valore</span><span class="sxs-lookup"><span data-stu-id="fa825-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa825-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa825-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fa825-126">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="fa825-126">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="fa825-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa825-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fa825-128">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fa825-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fa825-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fa825-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa825-130"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="fa825-130"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="fa825-131">Idl</span><span class="sxs-lookup"><span data-stu-id="fa825-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fa825-132"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="fa825-132"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="fa825-133">DLL</span><span class="sxs-lookup"><span data-stu-id="fa825-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa825-134"><dt>Shell32.dll (versione 6.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="fa825-134"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




