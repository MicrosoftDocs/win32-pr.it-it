---
description: 'Metodo IShellDispatch.EjectPC: espelle il computer dalla relativa stazione di ancoraggio. Questo è lo stesso che si fa clic sul menu Start e si seleziona Espulsa PC, se il computer supporta questo comando.'
ms.assetid: 34448D82-187C-40aa-90B4-A4111B33048B
title: Metodo IShellDispatch.EjectPC (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.EjectPC
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ac42e1a4331a553a03bac3da50a187e06c90859c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086639"
---
# <a name="ishelldispatchejectpc-method"></a><span data-ttu-id="a126e-104">Metodo IShellDispatch.EjectPC</span><span class="sxs-lookup"><span data-stu-id="a126e-104">IShellDispatch.EjectPC method</span></span>

<span data-ttu-id="a126e-105">Espulse il computer dall'alloggiamento di espansione.</span><span class="sxs-lookup"><span data-stu-id="a126e-105">Ejects the computer from its docking station.</span></span> <span data-ttu-id="a126e-106">Questo è lo stesso che si fa clic sul menu **Start** e si seleziona **Espulsa PC**, se il computer supporta questo comando.</span><span class="sxs-lookup"><span data-stu-id="a126e-106">This is the same as clicking the **Start** menu and selecting **Eject PC**, if your computer supports this command.</span></span>

## <a name="syntax"></a><span data-ttu-id="a126e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a126e-107">Syntax</span></span>


```JScript
IShellDispatch.EjectPC()
```


```VB

IShellDispatch.EjectPC()
```





## <a name="parameters"></a><span data-ttu-id="a126e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a126e-108">Parameters</span></span>

<span data-ttu-id="a126e-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a126e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a126e-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a126e-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="a126e-111">JScript</span><span class="sxs-lookup"><span data-stu-id="a126e-111">JScript</span></span>

<span data-ttu-id="a126e-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a126e-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="a126e-113">VB</span><span class="sxs-lookup"><span data-stu-id="a126e-113">VB</span></span>

<span data-ttu-id="a126e-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a126e-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a126e-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a126e-115">Remarks</span></span>

<span data-ttu-id="a126e-116">Questo metodo viene implementato e accessibile tramite il [**metodo Shell.EjectPC.**](shell-ejectpc.md)</span><span class="sxs-lookup"><span data-stu-id="a126e-116">This method is implemented and accessed through the [**Shell.EjectPC**](shell-ejectpc.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="a126e-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="a126e-117">Examples</span></span>

<span data-ttu-id="a126e-118">Gli esempi seguenti illustrano l'uso di **EjectPC** in JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a126e-118">The following examples show the use of **EjectPC** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="a126e-119">Jscript:</span><span class="sxs-lookup"><span data-stu-id="a126e-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellEjectPCJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.EjectPC();
    }
</script>
```



<span data-ttu-id="a126e-120">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="a126e-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellEjectPCVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.EjectPC

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="a126e-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="a126e-121">Visual Basic:</span></span>


```VB
Private Sub fnShellEjectPCVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.EjectPC

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="a126e-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a126e-122">Requirements</span></span>



| <span data-ttu-id="a126e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a126e-123">Requirement</span></span> | <span data-ttu-id="a126e-124">Valore</span><span class="sxs-lookup"><span data-stu-id="a126e-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a126e-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a126e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a126e-126">Solo app desktop windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a126e-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a126e-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a126e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a126e-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a126e-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a126e-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a126e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a126e-130"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="a126e-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a126e-131">Idl</span><span class="sxs-lookup"><span data-stu-id="a126e-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a126e-132"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="a126e-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a126e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a126e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a126e-134"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="a126e-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




