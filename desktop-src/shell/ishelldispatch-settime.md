---
description: Consente di visualizzare la finestra di dialogo Data e ora. Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sull'orologio nell'area stato della barra delle applicazioni e scegliere Regola data/ora.
ms.assetid: D4B949F6-5508-4624-9706-491184703DC6
title: Metodo IShellDispatch. setime (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.SetTime
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9c9e687ea89cad4715aeacf72a2a33792fba9f7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879786"
---
# <a name="ishelldispatchsettime-method"></a><span data-ttu-id="81dd8-104">IShellDispatch. setime (metodo)</span><span class="sxs-lookup"><span data-stu-id="81dd8-104">IShellDispatch.SetTime method</span></span>

<span data-ttu-id="81dd8-105">Consente di visualizzare la finestra di dialogo **data e ora** .</span><span class="sxs-lookup"><span data-stu-id="81dd8-105">Displays the **Date and Time** dialog box.</span></span> <span data-ttu-id="81dd8-106">Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sull'orologio nell'area stato della barra delle applicazioni e scegliere **regola Data/ora**.</span><span class="sxs-lookup"><span data-stu-id="81dd8-106">This method has the same effect as right-clicking the clock in the taskbar status area and selecting **Adjust date/time**.</span></span>

## <a name="syntax"></a><span data-ttu-id="81dd8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81dd8-107">Syntax</span></span>


```JScript
IShellDispatch.SetTime()
```


```VB

IShellDispatch.SetTime()
```





## <a name="parameters"></a><span data-ttu-id="81dd8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="81dd8-108">Parameters</span></span>

<span data-ttu-id="81dd8-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="81dd8-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="81dd8-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="81dd8-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="81dd8-111">JScript</span><span class="sxs-lookup"><span data-stu-id="81dd8-111">JScript</span></span>

<span data-ttu-id="81dd8-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="81dd8-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="81dd8-113">VB</span><span class="sxs-lookup"><span data-stu-id="81dd8-113">VB</span></span>

<span data-ttu-id="81dd8-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="81dd8-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="81dd8-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="81dd8-115">Remarks</span></span>

<span data-ttu-id="81dd8-116">Questo metodo viene implementato e accessibile tramite il metodo [**Shell. setime**](shell-settime.md) .</span><span class="sxs-lookup"><span data-stu-id="81dd8-116">This method is implemented and accessed through the [**Shell.SetTime**](shell-settime.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="81dd8-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="81dd8-117">Examples</span></span>

<span data-ttu-id="81dd8-118">Negli esempi seguenti viene illustrato l'utilizzo di **setime** in JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="81dd8-118">The following examples show the use of **SetTime** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="81dd8-119">JScript</span><span class="sxs-lookup"><span data-stu-id="81dd8-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellSetTimeJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.SetTime();
    }
</script>
```



<span data-ttu-id="81dd8-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="81dd8-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellSetTimeVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.SetTime
 
        set objShell = nothing
    end function
```



<span data-ttu-id="81dd8-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="81dd8-121">Visual Basic:</span></span>


```VB
Private Sub fnShellSetTimeVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.SetTime
 
    Set objShell = Nothing
```



## <a name="requirements"></a><span data-ttu-id="81dd8-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81dd8-122">Requirements</span></span>



| <span data-ttu-id="81dd8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="81dd8-123">Requirement</span></span> | <span data-ttu-id="81dd8-124">Valore</span><span class="sxs-lookup"><span data-stu-id="81dd8-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81dd8-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81dd8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="81dd8-126">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="81dd8-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="81dd8-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81dd8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="81dd8-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="81dd8-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="81dd8-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="81dd8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="81dd8-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="81dd8-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="81dd8-131">IDL</span><span class="sxs-lookup"><span data-stu-id="81dd8-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="81dd8-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="81dd8-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="81dd8-133">DLL</span><span class="sxs-lookup"><span data-stu-id="81dd8-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81dd8-134"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="81dd8-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




