---
description: Consente di visualizzare o nascondere il desktop.
title: Metodo IShellDispatch4. ToggleDesktop (shldisp. h)
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
ms.openlocfilehash: ccca7769363ad4dcf967611aad1b8ee5d7e28deb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977983"
---
# <a name="ishelldispatch4toggledesktop-method"></a><span data-ttu-id="4049a-103">IShellDispatch4. ToggleDesktop, metodo</span><span class="sxs-lookup"><span data-stu-id="4049a-103">IShellDispatch4.ToggleDesktop method</span></span>

<span data-ttu-id="4049a-104">Consente di visualizzare o nascondere il desktop.</span><span class="sxs-lookup"><span data-stu-id="4049a-104">Displays or hides the desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="4049a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4049a-105">Syntax</span></span>


```JScript
IShellDispatch4.ToggleDesktop()
```


```VB

IShellDispatch4.ToggleDesktop()
```





## <a name="parameters"></a><span data-ttu-id="4049a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4049a-106">Parameters</span></span>

<span data-ttu-id="4049a-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="4049a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4049a-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4049a-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="4049a-109">JScript</span><span class="sxs-lookup"><span data-stu-id="4049a-109">JScript</span></span>

<span data-ttu-id="4049a-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="4049a-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="4049a-111">VB</span><span class="sxs-lookup"><span data-stu-id="4049a-111">VB</span></span>

<span data-ttu-id="4049a-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="4049a-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4049a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4049a-113">Remarks</span></span>

<span data-ttu-id="4049a-114">Questo metodo ha lo stesso effetto del pulsante **Mostra desktop** sulla barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="4049a-114">This method has the same effect as the **Show Desktop** button on the taskbar.</span></span> <span data-ttu-id="4049a-115">Nasconde tutte le finestre aperte per visualizzare il desktop o nasconde il desktop visualizzando tutte le finestre aperte.</span><span class="sxs-lookup"><span data-stu-id="4049a-115">It either hides all open windows to show the desktop or it hides the desktop by showing all open windows.</span></span> <span data-ttu-id="4049a-116">Il metodo **ToggleDesktop** non visualizza un'interfaccia utente, richiama semplicemente l'azione di attivazione/disattivazione.</span><span class="sxs-lookup"><span data-stu-id="4049a-116">The **ToggleDesktop** method does not display a user interface, it just invokes the toggle action.</span></span>

## <a name="examples"></a><span data-ttu-id="4049a-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="4049a-117">Examples</span></span>

<span data-ttu-id="4049a-118">Gli esempi seguenti illustrano l'uso corretto di **ToggleDesktop** per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4049a-118">The following examples show the proper use of **ToggleDesktop** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="4049a-119">JScript</span><span class="sxs-lookup"><span data-stu-id="4049a-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ToggleDesktopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ToggleDesktop();
    }
</script>
```



<span data-ttu-id="4049a-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="4049a-120">VBScript:</span></span>


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



<span data-ttu-id="4049a-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="4049a-121">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ToggleDesktopVB()
    Dim objShell As Shell
            
    Set objShell = New Shell
        objShell.ToggleDesktop
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="4049a-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4049a-122">Requirements</span></span>



| <span data-ttu-id="4049a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4049a-123">Requirement</span></span> | <span data-ttu-id="4049a-124">Valore</span><span class="sxs-lookup"><span data-stu-id="4049a-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4049a-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4049a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4049a-126">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4049a-126">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="4049a-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4049a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4049a-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4049a-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4049a-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4049a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4049a-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4049a-130"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="4049a-131">IDL</span><span class="sxs-lookup"><span data-stu-id="4049a-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4049a-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4049a-132"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="4049a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4049a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4049a-134"><dt>Shell32.dll (versione 6,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="4049a-134"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




