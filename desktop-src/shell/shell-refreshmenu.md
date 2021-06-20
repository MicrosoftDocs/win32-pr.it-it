---
description: Informazioni sul metodo Shell.RefreshMenu, che aggiorna il contenuto del menu Start. Usato solo con i sistemi precedenti a Windows XP.
ms.assetid: 1269c66d-61df-432d-9220-5ac975e3ad58
title: Metodo Shell.RefreshMenu (Shldisp.h)
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
ms.openlocfilehash: 90020cd128f5cbc585bd7bc9ab33a8a81c745f8e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404534"
---
# <a name="shellrefreshmenu-method"></a><span data-ttu-id="d2c0c-104">Metodo Shell.RefreshMenu</span><span class="sxs-lookup"><span data-stu-id="d2c0c-104">Shell.RefreshMenu method</span></span>

<span data-ttu-id="d2c0c-105">Aggiorna il contenuto del menu **Start.**</span><span class="sxs-lookup"><span data-stu-id="d2c0c-105">Refreshes the contents of the **Start** menu.</span></span> <span data-ttu-id="d2c0c-106">Usato solo con i sistemi precedenti a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d2c0c-106">Used only with systems preceding Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2c0c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2c0c-107">Syntax</span></span>


```JScript
iRetVal = Shell.RefreshMenu()
```


```VB

Shell.RefreshMenu() As Integer
```





## <a name="parameters"></a><span data-ttu-id="d2c0c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2c0c-108">Parameters</span></span>

<span data-ttu-id="d2c0c-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="d2c0c-109">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2c0c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2c0c-110">Remarks</span></span>

<span data-ttu-id="d2c0c-111">La funzionalità fornita **da RefreshMenu** viene gestita automaticamente in Windows XP o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="d2c0c-111">The functionality that **RefreshMenu** provides is handled automatically under Windows XP or later.</span></span> <span data-ttu-id="d2c0c-112">Non chiamare questo metodo in tale sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d2c0c-112">Do not call this method under that operating system.</span></span>

## <a name="examples"></a><span data-ttu-id="d2c0c-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="d2c0c-113">Examples</span></span>

<span data-ttu-id="d2c0c-114">L'esempio seguente mostra **RefreshMenu** in uso.</span><span class="sxs-lookup"><span data-stu-id="d2c0c-114">The following example shows **RefreshMenu** in use.</span></span> <span data-ttu-id="d2c0c-115">Viene illustrato l'utilizzo corretto per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d2c0c-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="d2c0c-116">Jscript:</span><span class="sxs-lookup"><span data-stu-id="d2c0c-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.RefreshMenu();
    }
</script>
```



<span data-ttu-id="d2c0c-117">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="d2c0c-117">VBScript:</span></span>


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



<span data-ttu-id="d2c0c-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="d2c0c-118">Visual Basic:</span></span>


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.RefreshMenu

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="d2c0c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2c0c-119">Requirements</span></span>



| <span data-ttu-id="d2c0c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2c0c-120">Requirement</span></span> | <span data-ttu-id="d2c0c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d2c0c-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2c0c-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2c0c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d2c0c-123">Solo app desktop di Windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d2c0c-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d2c0c-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2c0c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d2c0c-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d2c0c-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d2c0c-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d2c0c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2c0c-127"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="d2c0c-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d2c0c-128">Idl</span><span class="sxs-lookup"><span data-stu-id="d2c0c-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d2c0c-129"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="d2c0c-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d2c0c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d2c0c-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2c0c-131"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="d2c0c-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




