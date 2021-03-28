---
description: Crea e restituisce un oggetto ShellWindows. Questo oggetto rappresenta una raccolta di tutte le finestre aperte che appartengono alla Shell.
ms.assetid: 788E2106-3534-4e22-801F-677FD02BDFE0
title: Metodo IShellDispatch. Windows (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Windows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: cb5f84caebf38deb27c7fb60565167793fead561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753079"
---
# <a name="ishelldispatchwindows-method"></a><span data-ttu-id="c1d87-104">Metodo IShellDispatch. Windows</span><span class="sxs-lookup"><span data-stu-id="c1d87-104">IShellDispatch.Windows method</span></span>

<span data-ttu-id="c1d87-105">Crea e restituisce un oggetto [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="c1d87-105">Creates and returns a [**ShellWindows**](shellwindows.md) object.</span></span> <span data-ttu-id="c1d87-106">Questo oggetto rappresenta una raccolta di tutte le finestre aperte che appartengono alla Shell.</span><span class="sxs-lookup"><span data-stu-id="c1d87-106">This object represents a collection of all of the open windows that belong to the Shell.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1d87-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1d87-107">Syntax</span></span>


```JScript
retVal = IShellDispatch.Windows()
```


```VB

IShellDispatch.Windows() As IDispatch
```





## <a name="parameters"></a><span data-ttu-id="c1d87-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c1d87-108">Parameters</span></span>

<span data-ttu-id="c1d87-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c1d87-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c1d87-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c1d87-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="c1d87-111">JScript</span><span class="sxs-lookup"><span data-stu-id="c1d87-111">JScript</span></span>

<span data-ttu-id="c1d87-112">Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="c1d87-112">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="c1d87-113">Riferimento all'oggetto [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="c1d87-113">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="c1d87-114">VB</span><span class="sxs-lookup"><span data-stu-id="c1d87-114">VB</span></span>

<span data-ttu-id="c1d87-115">Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="c1d87-115">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="c1d87-116">Riferimento all'oggetto [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="c1d87-116">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1d87-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1d87-117">Remarks</span></span>

<span data-ttu-id="c1d87-118">Questo metodo viene implementato e accessibile tramite il metodo [**Shell. Windows**](shell-windows.md) .</span><span class="sxs-lookup"><span data-stu-id="c1d87-118">This method is implemented and accessed through the [**Shell.Windows**](shell-windows.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="c1d87-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="c1d87-119">Examples</span></span>

<span data-ttu-id="c1d87-120">Negli esempi seguenti viene utilizzato **Windows** per recuperare l'oggetto [**ShellWindows**](shellwindows.md) e viene visualizzato un conteggio del numero di elementi in esso contenuti.</span><span class="sxs-lookup"><span data-stu-id="c1d87-120">The following examples use **Windows** to retrieve the [**ShellWindows**](shellwindows.md) object and display a count of the number of items that it contains.</span></span> <span data-ttu-id="c1d87-121">L'utilizzo viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c1d87-121">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c1d87-122">JScript</span><span class="sxs-lookup"><span data-stu-id="c1d87-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Windows();

        if (objShellWindows != null)
        {
            alert(objShellWindows.Count);
        }
    }
</script>
```



<span data-ttu-id="c1d87-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="c1d87-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Windows

        if (not objShellWindows is nothing) then
            alert(objShellWindows.Count)
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="c1d87-124">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="c1d87-124">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c1d87-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1d87-125">Requirements</span></span>



| <span data-ttu-id="c1d87-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1d87-126">Requirement</span></span> | <span data-ttu-id="c1d87-127">Valore</span><span class="sxs-lookup"><span data-stu-id="c1d87-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1d87-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1d87-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c1d87-129">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c1d87-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c1d87-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1d87-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c1d87-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c1d87-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c1d87-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c1d87-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1d87-133"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1d87-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c1d87-134">IDL</span><span class="sxs-lookup"><span data-stu-id="c1d87-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c1d87-135"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c1d87-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c1d87-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c1d87-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1d87-137"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="c1d87-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
