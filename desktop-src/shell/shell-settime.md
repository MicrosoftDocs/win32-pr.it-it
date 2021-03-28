---
description: Consente di visualizzare la finestra di dialogo Proprietà data e ora. Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sull'orologio nell'area stato della barra delle applicazioni e scegliere Regola data/ora.
ms.assetid: 01694607-3fc2-4d0d-ba48-5bdbb40da000
title: Metodo Shell. setime (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.SetTime
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b610effe87bd9e4ab33a6e8396e90f79e7bbbe9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979762"
---
# <a name="shellsettime-method"></a><span data-ttu-id="18463-104">Shell. setime (metodo)</span><span class="sxs-lookup"><span data-stu-id="18463-104">Shell.SetTime method</span></span>

<span data-ttu-id="18463-105">Consente di visualizzare la finestra di dialogo **Proprietà data e ora** .</span><span class="sxs-lookup"><span data-stu-id="18463-105">Displays the **Date and Time Properties** dialog box.</span></span> <span data-ttu-id="18463-106">Questo metodo ha lo stesso effetto di fare clic con il pulsante destro del mouse sull'orologio nell'area stato della barra delle applicazioni e scegliere **regola Data/ora**.</span><span class="sxs-lookup"><span data-stu-id="18463-106">This method has the same effect as right-clicking the clock in the taskbar status area and selecting **Adjust Date/Time**.</span></span>

## <a name="syntax"></a><span data-ttu-id="18463-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="18463-107">Syntax</span></span>


```JScript
iRetVal = Shell.SetTime()
```


```VB

Shell.SetTime() As Integer
```





## <a name="parameters"></a><span data-ttu-id="18463-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="18463-108">Parameters</span></span>

<span data-ttu-id="18463-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="18463-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="18463-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="18463-110">Examples</span></span>

<span data-ttu-id="18463-111">Nell'esempio seguente viene illustrato l'utilizzo di **Time** .</span><span class="sxs-lookup"><span data-stu-id="18463-111">The following example shows **SetTime** in use.</span></span> <span data-ttu-id="18463-112">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="18463-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="18463-113">JScript</span><span class="sxs-lookup"><span data-stu-id="18463-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellSetTimeJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.SetTime();
    }
</script>
```



<span data-ttu-id="18463-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="18463-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellSetTimeVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.SetTime
 
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="18463-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="18463-115">Visual Basic:</span></span>


```VB
Private Sub fnShellSetTimeVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.SetTime
 
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="18463-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18463-116">Requirements</span></span>



| <span data-ttu-id="18463-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="18463-117">Requirement</span></span> | <span data-ttu-id="18463-118">Valore</span><span class="sxs-lookup"><span data-stu-id="18463-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18463-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18463-119">Minimum supported client</span></span><br/> | <span data-ttu-id="18463-120">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="18463-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="18463-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18463-121">Minimum supported server</span></span><br/> | <span data-ttu-id="18463-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="18463-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="18463-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="18463-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="18463-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="18463-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="18463-125">IDL</span><span class="sxs-lookup"><span data-stu-id="18463-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="18463-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="18463-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="18463-127">DLL</span><span class="sxs-lookup"><span data-stu-id="18463-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18463-128"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="18463-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




