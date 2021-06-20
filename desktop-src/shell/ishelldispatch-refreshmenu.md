---
description: Informazioni sul metodo IShellDispatch.RefreshMenu, che aggiorna il contenuto del menu Start. Utilizzato solo con sistemi che precedono Windows XP.
ms.assetid: D36FA5A0-AF03-4627-86E0-869BF1440958
title: Metodo IShellDispatch.RefreshMenu (Shldisp.h)
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
ms.openlocfilehash: d9e1a3c326cfa79c7b754cc8a364e649cf2c9931
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404674"
---
# <a name="ishelldispatchrefreshmenu-method"></a><span data-ttu-id="e4529-104">Metodo IShellDispatch.RefreshMenu</span><span class="sxs-lookup"><span data-stu-id="e4529-104">IShellDispatch.RefreshMenu method</span></span>

<span data-ttu-id="e4529-105">Aggiorna il contenuto del menu **Start.**</span><span class="sxs-lookup"><span data-stu-id="e4529-105">Refreshes the contents of the **Start** menu.</span></span> <span data-ttu-id="e4529-106">Utilizzato solo con sistemi che precedono Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e4529-106">Used only with systems preceding Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4529-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4529-107">Syntax</span></span>


```JScript
IShellDispatch.RefreshMenu()
```


```VB

IShellDispatch.RefreshMenu()
```





## <a name="parameters"></a><span data-ttu-id="e4529-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4529-108">Parameters</span></span>

<span data-ttu-id="e4529-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e4529-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e4529-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4529-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="e4529-111">JScript</span><span class="sxs-lookup"><span data-stu-id="e4529-111">JScript</span></span>

<span data-ttu-id="e4529-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e4529-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="e4529-113">VB</span><span class="sxs-lookup"><span data-stu-id="e4529-113">VB</span></span>

<span data-ttu-id="e4529-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e4529-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4529-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4529-115">Remarks</span></span>

<span data-ttu-id="e4529-116">Questo metodo viene implementato e accessibile tramite il [**metodo Shell.TrayProperties.**](shell-trayproperties.md)</span><span class="sxs-lookup"><span data-stu-id="e4529-116">This method is implemented and accessed through the [**Shell.TrayProperties**](shell-trayproperties.md) method.</span></span>

<span data-ttu-id="e4529-117">La funzionalità fornita **da RefreshMenu** viene gestita automaticamente in Windows XP o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="e4529-117">The functionality that **RefreshMenu** provides is handled automatically under Windows XP or later.</span></span> <span data-ttu-id="e4529-118">Non chiamare questo metodo in Windows XP o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="e4529-118">Do not call this method on Windows XP or later.</span></span>

## <a name="examples"></a><span data-ttu-id="e4529-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="e4529-119">Examples</span></span>

<span data-ttu-id="e4529-120">Gli esempi seguenti illustrano l'uso **di RefreshMenu** in JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e4529-120">The following examples show the use of **RefreshMenu** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="e4529-121">Jscript:</span><span class="sxs-lookup"><span data-stu-id="e4529-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.RefreshMenu();
    }
</script>
```



<span data-ttu-id="e4529-122">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="e4529-122">VBScript:</span></span>


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



<span data-ttu-id="e4529-123">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="e4529-123">Visual Basic:</span></span>


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.RefreshMenu

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="e4529-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4529-124">Requirements</span></span>



| <span data-ttu-id="e4529-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4529-125">Requirement</span></span> | <span data-ttu-id="e4529-126">Valore</span><span class="sxs-lookup"><span data-stu-id="e4529-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4529-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4529-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e4529-128">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="e4529-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e4529-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4529-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e4529-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e4529-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e4529-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4529-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4529-132"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="e4529-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e4529-133">Idl</span><span class="sxs-lookup"><span data-stu-id="e4529-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e4529-134"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="e4529-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e4529-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e4529-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4529-136"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="e4529-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




