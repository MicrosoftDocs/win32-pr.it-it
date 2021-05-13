---
description: Esegue l'applicazione Pannello di controllo specificata.
title: Metodo IShellDispatch.ControlPanelItem (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.ControlPanelItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9A9B6B3F-FBBC-4e76-8018-8858B6392276
ms.openlocfilehash: 1a1c024b316472be00f119485326b704a4fe8dd0
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842842"
---
# <a name="ishelldispatchcontrolpanelitem-method"></a><span data-ttu-id="6f71c-103">Metodo IShellDispatch.ControlPanelItem</span><span class="sxs-lookup"><span data-stu-id="6f71c-103">IShellDispatch.ControlPanelItem method</span></span>

<span data-ttu-id="6f71c-104">Esegue l'applicazione Pannello di controllo specificata.</span><span class="sxs-lookup"><span data-stu-id="6f71c-104">Runs the specified Control Panel application.</span></span> <span data-ttu-id="6f71c-105">Se l'applicazione è già aperta, attiverà l'istanza in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6f71c-105">If the application is already open, it will activate the running instance.</span></span>

> [!Note]  
> <span data-ttu-id="6f71c-106">A data di Windows Vista, la maggior Pannello di controllo applicazioni sono elementi della shell e non possono essere aperte con questa funzione.</span><span class="sxs-lookup"><span data-stu-id="6f71c-106">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="6f71c-107">Per aprire tali Pannello di controllo applicazioni, passare il nome canonico a control.exe.</span><span class="sxs-lookup"><span data-stu-id="6f71c-107">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="6f71c-108">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="6f71c-108">For example:</span></span>
>
> ``` syntax
> control.exe /name Microsoft.Personalization
> ```

 

## <a name="syntax"></a><span data-ttu-id="6f71c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f71c-109">Syntax</span></span>


```JScript
IShellDispatch.ControlPanelItem(
  bstrDir
)
```


```VB

IShellDispatch.ControlPanelItem( _
  ByVal bstrDir As BSTR _
)
```





## <a name="parameters"></a><span data-ttu-id="6f71c-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="6f71c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f71c-111">*bstrDir* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6f71c-111">*bstrDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f71c-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="6f71c-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="6f71c-113">Nome Pannello di controllo file dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6f71c-113">The Control Panel application's file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f71c-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6f71c-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="6f71c-115">JScript</span><span class="sxs-lookup"><span data-stu-id="6f71c-115">JScript</span></span>

<span data-ttu-id="6f71c-116">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="6f71c-116">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="6f71c-117">VB</span><span class="sxs-lookup"><span data-stu-id="6f71c-117">VB</span></span>

<span data-ttu-id="6f71c-118">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="6f71c-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f71c-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f71c-119">Remarks</span></span>

<span data-ttu-id="6f71c-120">Questo metodo viene implementato e accessibile tramite il [**metodo Shell.ControlPanelItem.**](shell-controlpanelitem.md)</span><span class="sxs-lookup"><span data-stu-id="6f71c-120">This method is implemented and accessed through the [**Shell.ControlPanelItem**](shell-controlpanelitem.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="6f71c-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="6f71c-121">Examples</span></span>

<span data-ttu-id="6f71c-122">Gli esempi seguenti usano [**ControlPanelItem**](shell-controlpanelitem.md) per eseguire l'Pannello di controllo **dell'Proprietà dello schermo** elemento.</span><span class="sxs-lookup"><span data-stu-id="6f71c-122">The following examples use [**ControlPanelItem**](shell-controlpanelitem.md) to run the Control Panel's **Display Properties** item.</span></span> <span data-ttu-id="6f71c-123">L'utilizzo viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6f71c-123">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="6f71c-124">Jscript:</span><span class="sxs-lookup"><span data-stu-id="6f71c-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Shell_ControlPanelItem("desk.cpl");
    }
</script>
```



<span data-ttu-id="6f71c-125">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="6f71c-125">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellControlPanelItemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Shell_ControlPanelItem("desk.cpl")
       
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="6f71c-126">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="6f71c-126">Visual Basic:</span></span>


```VB
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Shell_ControlPanelItem ("desk.cpl")
    
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="6f71c-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f71c-127">Requirements</span></span>



| <span data-ttu-id="6f71c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f71c-128">Requirement</span></span> | <span data-ttu-id="6f71c-129">Valore</span><span class="sxs-lookup"><span data-stu-id="6f71c-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f71c-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f71c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6f71c-131">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6f71c-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6f71c-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f71c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6f71c-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6f71c-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6f71c-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f71c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f71c-135"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="6f71c-135"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="6f71c-136">Idl</span><span class="sxs-lookup"><span data-stu-id="6f71c-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6f71c-137"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="6f71c-137"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="6f71c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6f71c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f71c-139"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="6f71c-139"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
