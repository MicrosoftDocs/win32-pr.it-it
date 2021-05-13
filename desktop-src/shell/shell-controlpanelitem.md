---
description: Esegue l'applicazione Pannello di controllo \* (.cpl) specificata.
title: Metodo Shell.ControlPanelItem (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ControlPanelItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 54979bbd-b36b-4b5b-a8a0-5f63e9526fa5
ms.openlocfilehash: 04d2493f5d0ec5b86d19689cb8e7c2a02a82e536
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841802"
---
# <a name="shellcontrolpanelitem-method"></a><span data-ttu-id="b0540-103">Metodo Shell.ControlPanelItem</span><span class="sxs-lookup"><span data-stu-id="b0540-103">Shell.ControlPanelItem method</span></span>

<span data-ttu-id="b0540-104">Esegue l'applicazione Pannello di controllo \* (.cpl) specificata.</span><span class="sxs-lookup"><span data-stu-id="b0540-104">Runs the specified Control Panel (\*.cpl) application.</span></span> <span data-ttu-id="b0540-105">Se l'applicazione è già aperta, attiverà l'istanza in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b0540-105">If the application is already open, it will activate the running instance.</span></span>

> [!Note]  
> <span data-ttu-id="b0540-106">A causa di Windows Vista, la maggior Pannello di controllo applicazioni sono elementi della shell e non possono essere aperte con questa funzione.</span><span class="sxs-lookup"><span data-stu-id="b0540-106">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="b0540-107">Per aprire queste Pannello di controllo applicazioni, passare il nome canonico a control.exe.</span><span class="sxs-lookup"><span data-stu-id="b0540-107">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="b0540-108">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="b0540-108">For example:</span></span>
>
> ``` syntax
> control.exe /name Microsoft.Personalization
> ```

 

## <a name="syntax"></a><span data-ttu-id="b0540-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b0540-109">Syntax</span></span>


```JScript
Shell.ControlPanelItem(
  bstrDir
)
```


```VB

Shell.ControlPanelItem( _
  ByVal bstrDir As BSTR _
)
```





## <a name="parameters"></a><span data-ttu-id="b0540-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b0540-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0540-111">*bstrDir* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b0540-111">*bstrDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0540-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="b0540-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="b0540-113">Nome Pannello di controllo file dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b0540-113">The Control Panel application's file name.</span></span> <span data-ttu-id="b0540-114">Tutte Pannello di controllo applicazioni hanno l'estensione .cpl.</span><span class="sxs-lookup"><span data-stu-id="b0540-114">All Control Panel applications have the .cpl extension.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0540-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b0540-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b0540-116">JScript</span><span class="sxs-lookup"><span data-stu-id="b0540-116">JScript</span></span>

<span data-ttu-id="b0540-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="b0540-117">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="b0540-118">VB</span><span class="sxs-lookup"><span data-stu-id="b0540-118">VB</span></span>

<span data-ttu-id="b0540-119">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="b0540-119">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="b0540-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="b0540-120">Examples</span></span>

<span data-ttu-id="b0540-121">L'esempio seguente usa **ControlPanelItem** per eseguire  l'Pannello di controllo'Proprietà dello schermo elemento.</span><span class="sxs-lookup"><span data-stu-id="b0540-121">The following example uses **ControlPanelItem** to run the Control Panel's **Display Properties** item.</span></span> <span data-ttu-id="b0540-122">Viene illustrato l'utilizzo corretto per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b0540-122">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b0540-123">Jscript:</span><span class="sxs-lookup"><span data-stu-id="b0540-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ControlPanelItem("desk.cpl");
    }
</script>
```



<span data-ttu-id="b0540-124">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="b0540-124">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellControlPanelItemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.ControlPanelItem("desk.cpl")
       
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="b0540-125">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b0540-125">Visual Basic:</span></span>


```VB
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.ControlPanelItem ("desk.cpl")
    
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b0540-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b0540-126">Requirements</span></span>



| <span data-ttu-id="b0540-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0540-127">Requirement</span></span> | <span data-ttu-id="b0540-128">Valore</span><span class="sxs-lookup"><span data-stu-id="b0540-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0540-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b0540-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b0540-130">Solo app desktop di Windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b0540-130">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b0540-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b0540-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b0540-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b0540-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b0540-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b0540-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0540-134"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="b0540-134"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b0540-135">Idl</span><span class="sxs-lookup"><span data-stu-id="b0540-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b0540-136"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="b0540-136"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b0540-137">DLL</span><span class="sxs-lookup"><span data-stu-id="b0540-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0540-138"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="b0540-138"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
