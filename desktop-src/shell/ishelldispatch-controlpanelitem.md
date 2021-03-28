---
description: Esegue l'applicazione del pannello di controllo specificata.
title: Metodo IShellDispatch. ControlPanelItem (shldisp. h)
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
ms.openlocfilehash: 72164ff76cbcf15703bc91160e6211b38015f989
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527354"
---
# <a name="ishelldispatchcontrolpanelitem-method"></a><span data-ttu-id="6d019-103">IShellDispatch. ControlPanelItem, metodo</span><span class="sxs-lookup"><span data-stu-id="6d019-103">IShellDispatch.ControlPanelItem method</span></span>

<span data-ttu-id="6d019-104">Esegue l'applicazione del pannello di controllo specificata.</span><span class="sxs-lookup"><span data-stu-id="6d019-104">Runs the specified Control Panel application.</span></span> <span data-ttu-id="6d019-105">Se l'applicazione è già aperta, attiverà l'istanza in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6d019-105">If the application is already open, it will activate the running instance.</span></span>

> [!Note]  
> <span data-ttu-id="6d019-106">A partire da Windows Vista, la maggior parte delle applicazioni del pannello di controllo sono elementi della shell e non possono essere aperti con questa funzione.</span><span class="sxs-lookup"><span data-stu-id="6d019-106">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="6d019-107">Per aprire le applicazioni del pannello di controllo, passare il nome canonico a control.exe.</span><span class="sxs-lookup"><span data-stu-id="6d019-107">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="6d019-108">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="6d019-108">For example:</span></span>
>
> ``` syntax
> control.exe /name Microsoft.Personalization
> ```

 

## <a name="syntax"></a><span data-ttu-id="6d019-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6d019-109">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="6d019-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="6d019-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d019-111">*bstrDir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d019-111">*bstrDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d019-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="6d019-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="6d019-113">Nome del file dell'applicazione del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="6d019-113">The Control Panel application's file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d019-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6d019-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="6d019-115">JScript</span><span class="sxs-lookup"><span data-stu-id="6d019-115">JScript</span></span>

<span data-ttu-id="6d019-116">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="6d019-116">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="6d019-117">VB</span><span class="sxs-lookup"><span data-stu-id="6d019-117">VB</span></span>

<span data-ttu-id="6d019-118">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="6d019-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d019-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d019-119">Remarks</span></span>

<span data-ttu-id="6d019-120">Questo metodo viene implementato e accessibile tramite il metodo [**Shell. ControlPanelItem**](shell-controlpanelitem.md) .</span><span class="sxs-lookup"><span data-stu-id="6d019-120">This method is implemented and accessed through the [**Shell.ControlPanelItem**](shell-controlpanelitem.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="6d019-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="6d019-121">Examples</span></span>

<span data-ttu-id="6d019-122">Gli esempi seguenti usano [**ControlPanelItem**](shell-controlpanelitem.md) per eseguire l'elemento delle **proprietà di visualizzazione** del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="6d019-122">The following examples use [**ControlPanelItem**](shell-controlpanelitem.md) to run the Control Panel's **Display Properties** item.</span></span> <span data-ttu-id="6d019-123">L'utilizzo viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6d019-123">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="6d019-124">JScript</span><span class="sxs-lookup"><span data-stu-id="6d019-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Shell_ControlPanelItem("desk.cpl");
    }
</script>
```



<span data-ttu-id="6d019-125">VBScript</span><span class="sxs-lookup"><span data-stu-id="6d019-125">VBScript:</span></span>


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



<span data-ttu-id="6d019-126">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="6d019-126">Visual Basic:</span></span>


```VB
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Shell_ControlPanelItem ("desk.cpl")
    
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="6d019-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d019-127">Requirements</span></span>



| <span data-ttu-id="6d019-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d019-128">Requirement</span></span> | <span data-ttu-id="6d019-129">Valore</span><span class="sxs-lookup"><span data-stu-id="6d019-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d019-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d019-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6d019-131">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6d019-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6d019-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d019-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6d019-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6d019-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6d019-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6d019-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d019-135"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d019-135"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="6d019-136">IDL</span><span class="sxs-lookup"><span data-stu-id="6d019-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6d019-137"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6d019-137"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="6d019-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6d019-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d019-139"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="6d019-139"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
