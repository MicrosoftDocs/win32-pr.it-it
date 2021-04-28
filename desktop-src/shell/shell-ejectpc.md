---
description: 'Metodo Shell.EjectPC: espulse il computer dalla relativa stazione di ancoraggio. Questa operazione è identica a quando si fa clic menu Start e si seleziona Espulsa PC, se il computer supporta questo comando.'
ms.assetid: eaba3dce-8fea-453f-90c2-4a9b5cb05ecc
title: Metodo Shell.EjectPC (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.EjectPC
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5ec08aaa82d2f752fa06537434adede86b9d5a3a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104349"
---
# <a name="shellejectpc-method"></a><span data-ttu-id="a8df0-104">Metodo Shell.EjectPC</span><span class="sxs-lookup"><span data-stu-id="a8df0-104">Shell.EjectPC method</span></span>

<span data-ttu-id="a8df0-105">Espulsa il computer dalla relativa stazione di ancoraggio.</span><span class="sxs-lookup"><span data-stu-id="a8df0-105">Ejects the computer from its docking station.</span></span> <span data-ttu-id="a8df0-106">Questa operazione è identica a quando si fa clic sul menu **Start** e si **seleziona Eject PC (Espila PC),** se il computer supporta questo comando.</span><span class="sxs-lookup"><span data-stu-id="a8df0-106">This is the same as clicking the **Start** menu and selecting **Eject PC**, if your computer supports this command.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8df0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a8df0-107">Syntax</span></span>


```JScript
Shell.EjectPC()
```


```VB

Shell.EjectPC()
```





## <a name="parameters"></a><span data-ttu-id="a8df0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a8df0-108">Parameters</span></span>

<span data-ttu-id="a8df0-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a8df0-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a8df0-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a8df0-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="a8df0-111">JScript</span><span class="sxs-lookup"><span data-stu-id="a8df0-111">JScript</span></span>

<span data-ttu-id="a8df0-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a8df0-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="a8df0-113">VB</span><span class="sxs-lookup"><span data-stu-id="a8df0-113">VB</span></span>

<span data-ttu-id="a8df0-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a8df0-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="a8df0-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="a8df0-115">Examples</span></span>

<span data-ttu-id="a8df0-116">L'esempio seguente **mostra EjectPC** in uso.</span><span class="sxs-lookup"><span data-stu-id="a8df0-116">The following example shows **EjectPC** in use.</span></span> <span data-ttu-id="a8df0-117">Viene illustrato l'utilizzo corretto per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a8df0-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="a8df0-118">Jscript:</span><span class="sxs-lookup"><span data-stu-id="a8df0-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellEjectPCJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.EjectPC();
    }
</script>
```



<span data-ttu-id="a8df0-119">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="a8df0-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellEjectPCVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.EjectPC

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="a8df0-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="a8df0-120">Visual Basic:</span></span>


```VB
Private Sub fnShellEjectPCVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.EjectPC

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="a8df0-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8df0-121">Requirements</span></span>



| <span data-ttu-id="a8df0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8df0-122">Requirement</span></span> | <span data-ttu-id="a8df0-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a8df0-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8df0-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8df0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a8df0-125">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a8df0-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a8df0-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8df0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a8df0-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a8df0-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a8df0-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a8df0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8df0-129"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="a8df0-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a8df0-130">Idl</span><span class="sxs-lookup"><span data-stu-id="a8df0-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a8df0-131"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="a8df0-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a8df0-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a8df0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8df0-133"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="a8df0-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




