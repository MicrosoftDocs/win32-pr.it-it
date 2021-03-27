---
description: Riduce al minimo tutte le finestre sul desktop.
ms.assetid: 3af98a16-27d1-4c93-ac72-7c9e24e68c23
title: Metodo Shell. MinimizeAll (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.MinimizeAll
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 55b615cfed8813f5567b13d58648fef36aaedda3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980623"
---
# <a name="shellminimizeall-method"></a><span data-ttu-id="b9275-103">Shell. MinimizeAll, metodo</span><span class="sxs-lookup"><span data-stu-id="b9275-103">Shell.MinimizeAll method</span></span>

<span data-ttu-id="b9275-104">Riduce al minimo tutte le finestre sul desktop.</span><span class="sxs-lookup"><span data-stu-id="b9275-104">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="b9275-105">Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sulla barra delle applicazioni e selezionare **Riduci a icona tutte le finestre** nei sistemi meno recenti oppure fare clic sull'icona **Mostra desktop** nell'area avvio veloce della barra delle applicazioni in Windows 2000 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b9275-105">This method has the same effect as right-clicking the taskbar and selecting **Minimize All Windows** on older systems or clicking the **Show Desktop** icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9275-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9275-106">Syntax</span></span>


```JScript
iRetVal = Shell.MinimizeAll()
```


```VB

Shell.MinimizeAll() As Integer
```





## <a name="parameters"></a><span data-ttu-id="b9275-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b9275-107">Parameters</span></span>

<span data-ttu-id="b9275-108">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b9275-108">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="b9275-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="b9275-109">Examples</span></span>

<span data-ttu-id="b9275-110">Nell'esempio seguente viene illustrato **MinimizeAll** in uso.</span><span class="sxs-lookup"><span data-stu-id="b9275-110">The following example shows **MinimizeAll** in use.</span></span> <span data-ttu-id="b9275-111">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b9275-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b9275-112">JScript</span><span class="sxs-lookup"><span data-stu-id="b9275-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellMinimizeAllJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.MinimizeAll();
    }
</script>
```



<span data-ttu-id="b9275-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="b9275-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellMinimizeAllVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.MinimizeAll

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="b9275-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b9275-114">Visual Basic:</span></span>


```VB
Private Sub fnShellMinimizeAllVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.MinimizeAll

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b9275-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9275-115">Requirements</span></span>



| <span data-ttu-id="b9275-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9275-116">Requirement</span></span> | <span data-ttu-id="b9275-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b9275-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9275-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9275-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b9275-119">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b9275-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b9275-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9275-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b9275-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b9275-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b9275-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9275-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9275-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9275-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b9275-124">IDL</span><span class="sxs-lookup"><span data-stu-id="b9275-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b9275-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b9275-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b9275-126">DLL</span><span class="sxs-lookup"><span data-stu-id="b9275-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9275-127"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="b9275-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9275-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9275-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9275-129">**Shell**</span><span class="sxs-lookup"><span data-stu-id="b9275-129">**Shell**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="b9275-130">**UndoMinimizeALL**</span><span class="sxs-lookup"><span data-stu-id="b9275-130">**UndoMinimizeALL**</span></span>](shell-undominimizeall.md)
</dt> </dl>

 

 




