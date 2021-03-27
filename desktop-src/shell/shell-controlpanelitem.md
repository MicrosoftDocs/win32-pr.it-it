---
description: Esegue l'applicazione del pannello di controllo ( \* . cpl) specificata.
title: Metodo Shell. ControlPanelItem (shldisp. h)
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
ms.openlocfilehash: dec27dab8bd37cc9c15e603c24a54d528cea331a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979914"
---
# <a name="shellcontrolpanelitem-method"></a><span data-ttu-id="67099-103">Shell. ControlPanelItem, metodo</span><span class="sxs-lookup"><span data-stu-id="67099-103">Shell.ControlPanelItem method</span></span>

<span data-ttu-id="67099-104">Esegue l'applicazione del pannello di controllo ( \* . cpl) specificata.</span><span class="sxs-lookup"><span data-stu-id="67099-104">Runs the specified Control Panel (\*.cpl) application.</span></span> <span data-ttu-id="67099-105">Se l'applicazione è già aperta, attiverà l'istanza in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="67099-105">If the application is already open, it will activate the running instance.</span></span>

> [!Note]  
> <span data-ttu-id="67099-106">A partire da Windows Vista, la maggior parte delle applicazioni del pannello di controllo sono elementi della shell e non possono essere aperti con questa funzione.</span><span class="sxs-lookup"><span data-stu-id="67099-106">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="67099-107">Per aprire le applicazioni del pannello di controllo, passare il nome canonico a control.exe.</span><span class="sxs-lookup"><span data-stu-id="67099-107">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="67099-108">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="67099-108">For example:</span></span>
>
> ``` syntax
> control.exe /name Microsoft.Personalization
> ```

 

## <a name="syntax"></a><span data-ttu-id="67099-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="67099-109">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="67099-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="67099-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67099-111">*bstrDir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67099-111">*bstrDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67099-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="67099-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="67099-113">Nome del file dell'applicazione del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="67099-113">The Control Panel application's file name.</span></span> <span data-ttu-id="67099-114">Tutte le applicazioni del pannello di controllo hanno estensione CPL.</span><span class="sxs-lookup"><span data-stu-id="67099-114">All Control Panel applications have the .cpl extension.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67099-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="67099-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="67099-116">JScript</span><span class="sxs-lookup"><span data-stu-id="67099-116">JScript</span></span>

<span data-ttu-id="67099-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="67099-117">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="67099-118">VB</span><span class="sxs-lookup"><span data-stu-id="67099-118">VB</span></span>

<span data-ttu-id="67099-119">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="67099-119">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="67099-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="67099-120">Examples</span></span>

<span data-ttu-id="67099-121">Nell'esempio seguente viene usato **ControlPanelItem** per eseguire l'elemento delle **proprietà di visualizzazione** del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="67099-121">The following example uses **ControlPanelItem** to run the Control Panel's **Display Properties** item.</span></span> <span data-ttu-id="67099-122">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="67099-122">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="67099-123">JScript</span><span class="sxs-lookup"><span data-stu-id="67099-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ControlPanelItem("desk.cpl");
    }
</script>
```



<span data-ttu-id="67099-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="67099-124">VBScript:</span></span>


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



<span data-ttu-id="67099-125">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="67099-125">Visual Basic:</span></span>


```VB
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.ControlPanelItem ("desk.cpl")
    
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="67099-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67099-126">Requirements</span></span>



| <span data-ttu-id="67099-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="67099-127">Requirement</span></span> | <span data-ttu-id="67099-128">Valore</span><span class="sxs-lookup"><span data-stu-id="67099-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67099-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67099-129">Minimum supported client</span></span><br/> | <span data-ttu-id="67099-130">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="67099-130">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="67099-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67099-131">Minimum supported server</span></span><br/> | <span data-ttu-id="67099-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="67099-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="67099-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="67099-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="67099-134"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="67099-134"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="67099-135">IDL</span><span class="sxs-lookup"><span data-stu-id="67099-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="67099-136"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="67099-136"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="67099-137">DLL</span><span class="sxs-lookup"><span data-stu-id="67099-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67099-138"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="67099-138"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
