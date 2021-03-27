---
description: Aggiorna il contenuto del menu Start. Utilizzato solo con i sistemi precedenti a Windows XP.
ms.assetid: 1269c66d-61df-432d-9220-5ac975e3ad58
title: Metodo Shell. RefreshMenu (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.RefreshMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a5812312c846026f4e0c7d2a4f6a5f857a572a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979767"
---
# <a name="shellrefreshmenu-method"></a><span data-ttu-id="7315f-104">Shell. RefreshMenu, metodo</span><span class="sxs-lookup"><span data-stu-id="7315f-104">Shell.RefreshMenu method</span></span>

<span data-ttu-id="7315f-105">Aggiorna il contenuto del menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="7315f-105">Refreshes the contents of the **Start** menu.</span></span> <span data-ttu-id="7315f-106">Utilizzato solo con i sistemi precedenti a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7315f-106">Used only with systems preceding Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="7315f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7315f-107">Syntax</span></span>


```JScript
iRetVal = Shell.RefreshMenu()
```


```VB

Shell.RefreshMenu() As Integer
```





## <a name="parameters"></a><span data-ttu-id="7315f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7315f-108">Parameters</span></span>

<span data-ttu-id="7315f-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7315f-109">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="7315f-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="7315f-110">Remarks</span></span>

<span data-ttu-id="7315f-111">La funzionalità fornita da **RefreshMenu** viene gestita automaticamente in Windows XP o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="7315f-111">The functionality that **RefreshMenu** provides is handled automatically under Windows XP or later.</span></span> <span data-ttu-id="7315f-112">Non chiamare questo metodo in quel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7315f-112">Do not call this method under that operating system.</span></span>

## <a name="examples"></a><span data-ttu-id="7315f-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="7315f-113">Examples</span></span>

<span data-ttu-id="7315f-114">Nell'esempio seguente viene illustrato **RefreshMenu** in uso.</span><span class="sxs-lookup"><span data-stu-id="7315f-114">The following example shows **RefreshMenu** in use.</span></span> <span data-ttu-id="7315f-115">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7315f-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="7315f-116">JScript</span><span class="sxs-lookup"><span data-stu-id="7315f-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.RefreshMenu();
    }
</script>
```



<span data-ttu-id="7315f-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="7315f-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellRefreshMenuVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.RefreshMenu

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="7315f-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="7315f-118">Visual Basic:</span></span>


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.RefreshMenu

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="7315f-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7315f-119">Requirements</span></span>



| <span data-ttu-id="7315f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7315f-120">Requirement</span></span> | <span data-ttu-id="7315f-121">Valore</span><span class="sxs-lookup"><span data-stu-id="7315f-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7315f-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7315f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7315f-123">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7315f-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7315f-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7315f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7315f-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7315f-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7315f-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7315f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7315f-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7315f-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7315f-128">IDL</span><span class="sxs-lookup"><span data-stu-id="7315f-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7315f-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7315f-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7315f-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7315f-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7315f-131"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="7315f-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




