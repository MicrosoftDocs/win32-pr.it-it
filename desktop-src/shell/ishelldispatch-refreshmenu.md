---
description: Aggiorna il contenuto del menu Start. Utilizzato solo con i sistemi precedenti a Windows XP.
ms.assetid: D36FA5A0-AF03-4627-86E0-869BF1440958
title: Metodo IShellDispatch. RefreshMenu (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.RefreshMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 98728ef48ffb9ef4383cf9ba567606758b7a015c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978095"
---
# <a name="ishelldispatchrefreshmenu-method"></a><span data-ttu-id="df272-104">IShellDispatch. RefreshMenu, metodo</span><span class="sxs-lookup"><span data-stu-id="df272-104">IShellDispatch.RefreshMenu method</span></span>

<span data-ttu-id="df272-105">Aggiorna il contenuto del menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="df272-105">Refreshes the contents of the **Start** menu.</span></span> <span data-ttu-id="df272-106">Utilizzato solo con i sistemi precedenti a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="df272-106">Used only with systems preceding Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="df272-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df272-107">Syntax</span></span>


```JScript
IShellDispatch.RefreshMenu()
```


```VB

IShellDispatch.RefreshMenu()
```





## <a name="parameters"></a><span data-ttu-id="df272-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="df272-108">Parameters</span></span>

<span data-ttu-id="df272-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="df272-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="df272-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df272-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="df272-111">JScript</span><span class="sxs-lookup"><span data-stu-id="df272-111">JScript</span></span>

<span data-ttu-id="df272-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="df272-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="df272-113">VB</span><span class="sxs-lookup"><span data-stu-id="df272-113">VB</span></span>

<span data-ttu-id="df272-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="df272-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="df272-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="df272-115">Remarks</span></span>

<span data-ttu-id="df272-116">Questo metodo viene implementato e accessibile tramite il metodo [**Shell. TrayProperties**](shell-trayproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="df272-116">This method is implemented and accessed through the [**Shell.TrayProperties**](shell-trayproperties.md) method.</span></span>

<span data-ttu-id="df272-117">La funzionalità fornita da **RefreshMenu** viene gestita automaticamente in Windows XP o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="df272-117">The functionality that **RefreshMenu** provides is handled automatically under Windows XP or later.</span></span> <span data-ttu-id="df272-118">Non chiamare questo metodo in Windows XP o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="df272-118">Do not call this method on Windows XP or later.</span></span>

## <a name="examples"></a><span data-ttu-id="df272-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="df272-119">Examples</span></span>

<span data-ttu-id="df272-120">Negli esempi seguenti viene illustrato l'utilizzo di **RefreshMenu** in JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="df272-120">The following examples show the use of **RefreshMenu** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="df272-121">JScript</span><span class="sxs-lookup"><span data-stu-id="df272-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.RefreshMenu();
    }
</script>
```



<span data-ttu-id="df272-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="df272-122">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellRefreshMenuVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.RefreshMenu

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="df272-123">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="df272-123">Visual Basic:</span></span>


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.RefreshMenu

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="df272-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df272-124">Requirements</span></span>



| <span data-ttu-id="df272-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="df272-125">Requirement</span></span> | <span data-ttu-id="df272-126">Valore</span><span class="sxs-lookup"><span data-stu-id="df272-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df272-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df272-127">Minimum supported client</span></span><br/> | <span data-ttu-id="df272-128">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="df272-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="df272-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df272-129">Minimum supported server</span></span><br/> | <span data-ttu-id="df272-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="df272-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="df272-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df272-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="df272-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="df272-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="df272-133">IDL</span><span class="sxs-lookup"><span data-stu-id="df272-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="df272-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="df272-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="df272-135">DLL</span><span class="sxs-lookup"><span data-stu-id="df272-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df272-136"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="df272-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




