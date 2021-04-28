---
description: 'Metodo IShellDispatch.Windows: crea e restituisce un oggetto ShellWindows. Questo oggetto rappresenta una raccolta di tutte le finestre aperte che appartengono alla shell.'
ms.assetid: 788E2106-3534-4e22-801F-677FD02BDFE0
title: Metodo IShellDispatch.Windows (Shldisp.h)
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
ms.openlocfilehash: 16991d6a251909e8f3b277894a96e6ad08a7f9a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117169"
---
# <a name="ishelldispatchwindows-method"></a><span data-ttu-id="19c1b-104">Metodo IShellDispatch.Windows</span><span class="sxs-lookup"><span data-stu-id="19c1b-104">IShellDispatch.Windows method</span></span>

<span data-ttu-id="19c1b-105">Crea e restituisce un [**oggetto ShellWindows.**](shellwindows.md)</span><span class="sxs-lookup"><span data-stu-id="19c1b-105">Creates and returns a [**ShellWindows**](shellwindows.md) object.</span></span> <span data-ttu-id="19c1b-106">Questo oggetto rappresenta una raccolta di tutte le finestre aperte che appartengono alla shell.</span><span class="sxs-lookup"><span data-stu-id="19c1b-106">This object represents a collection of all of the open windows that belong to the Shell.</span></span>

## <a name="syntax"></a><span data-ttu-id="19c1b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19c1b-107">Syntax</span></span>


```JScript
retVal = IShellDispatch.Windows()
```


```VB

IShellDispatch.Windows() As IDispatch
```





## <a name="parameters"></a><span data-ttu-id="19c1b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="19c1b-108">Parameters</span></span>

<span data-ttu-id="19c1b-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="19c1b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="19c1b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="19c1b-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="19c1b-111">JScript</span><span class="sxs-lookup"><span data-stu-id="19c1b-111">JScript</span></span>

<span data-ttu-id="19c1b-112">Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="19c1b-112">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="19c1b-113">Riferimento all'oggetto [**ShellWindows.**](shellwindows.md)</span><span class="sxs-lookup"><span data-stu-id="19c1b-113">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="19c1b-114">VB</span><span class="sxs-lookup"><span data-stu-id="19c1b-114">VB</span></span>

<span data-ttu-id="19c1b-115">Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="19c1b-115">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="19c1b-116">Riferimento all'oggetto [**ShellWindows.**](shellwindows.md)</span><span class="sxs-lookup"><span data-stu-id="19c1b-116">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="19c1b-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="19c1b-117">Remarks</span></span>

<span data-ttu-id="19c1b-118">Questo metodo viene implementato e accessibile tramite il [**metodo Shell.Windows.**](shell-windows.md)</span><span class="sxs-lookup"><span data-stu-id="19c1b-118">This method is implemented and accessed through the [**Shell.Windows**](shell-windows.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="19c1b-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="19c1b-119">Examples</span></span>

<span data-ttu-id="19c1b-120">Gli esempi seguenti **usano Windows** per recuperare [**l'oggetto ShellWindows**](shellwindows.md) e visualizzare un conteggio del numero di elementi in esso contenuti.</span><span class="sxs-lookup"><span data-stu-id="19c1b-120">The following examples use **Windows** to retrieve the [**ShellWindows**](shellwindows.md) object and display a count of the number of items that it contains.</span></span> <span data-ttu-id="19c1b-121">L'utilizzo viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="19c1b-121">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="19c1b-122">Jscript:</span><span class="sxs-lookup"><span data-stu-id="19c1b-122">JScript:</span></span>


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



<span data-ttu-id="19c1b-123">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="19c1b-123">VBScript:</span></span>


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



<span data-ttu-id="19c1b-124">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="19c1b-124">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="19c1b-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19c1b-125">Requirements</span></span>



| <span data-ttu-id="19c1b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="19c1b-126">Requirement</span></span> | <span data-ttu-id="19c1b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="19c1b-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19c1b-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19c1b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="19c1b-129">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="19c1b-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="19c1b-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19c1b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="19c1b-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="19c1b-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="19c1b-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="19c1b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="19c1b-133"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="19c1b-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="19c1b-134">Idl</span><span class="sxs-lookup"><span data-stu-id="19c1b-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="19c1b-135"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="19c1b-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="19c1b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="19c1b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19c1b-137"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="19c1b-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
