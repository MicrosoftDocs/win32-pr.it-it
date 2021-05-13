---
description: 'Metodo Shell.Windows: crea e restituisce un oggetto ShellWindows. Questo oggetto rappresenta una raccolta di tutte le finestre aperte che appartengono alla shell.'
title: Metodo Shell.Windows (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Windows
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ffa6311c-8bbe-45c4-9b06-069779d2306d
ms.openlocfilehash: bbe8ed55865322fc7436959fd80b478baa3c0b40
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842612"
---
# <a name="shellwindows-method"></a><span data-ttu-id="58b3b-104">Metodo Shell.Windows</span><span class="sxs-lookup"><span data-stu-id="58b3b-104">Shell.Windows method</span></span>

<span data-ttu-id="58b3b-105">Crea e restituisce un [**oggetto ShellWindows.**](shellwindows.md)</span><span class="sxs-lookup"><span data-stu-id="58b3b-105">Creates and returns a [**ShellWindows**](shellwindows.md) object.</span></span> <span data-ttu-id="58b3b-106">Questo oggetto rappresenta una raccolta di tutte le finestre aperte che appartengono alla shell.</span><span class="sxs-lookup"><span data-stu-id="58b3b-106">This object represents a collection of all of the open windows that belong to the Shell.</span></span>

## <a name="syntax"></a><span data-ttu-id="58b3b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58b3b-107">Syntax</span></span>


```JScript
retVal = Shell.Windows()
```


```VB

Shell.Windows() As IDispatch
```





## <a name="parameters"></a><span data-ttu-id="58b3b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="58b3b-108">Parameters</span></span>

<span data-ttu-id="58b3b-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="58b3b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="58b3b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58b3b-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="58b3b-111">JScript</span><span class="sxs-lookup"><span data-stu-id="58b3b-111">JScript</span></span>

<span data-ttu-id="58b3b-112">Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="58b3b-112">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="58b3b-113">Riferimento all'oggetto [**ShellWindows.**](shellwindows.md)</span><span class="sxs-lookup"><span data-stu-id="58b3b-113">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="58b3b-114">VB</span><span class="sxs-lookup"><span data-stu-id="58b3b-114">VB</span></span>

<span data-ttu-id="58b3b-115">Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="58b3b-115">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="58b3b-116">Riferimento all'oggetto [**ShellWindows.**](shellwindows.md)</span><span class="sxs-lookup"><span data-stu-id="58b3b-116">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="58b3b-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="58b3b-117">Examples</span></span>

<span data-ttu-id="58b3b-118">L'esempio seguente **usa Windows** per recuperare [**l'oggetto ShellWindows**](shellwindows.md) e visualizzare un conteggio del numero di elementi in esso contenuti.</span><span class="sxs-lookup"><span data-stu-id="58b3b-118">The following example uses **Windows** to retrieve the [**ShellWindows**](shellwindows.md) object and display a count of the number of items that it contains.</span></span> <span data-ttu-id="58b3b-119">Viene illustrato l'utilizzo corretto per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="58b3b-119">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="58b3b-120">Jscript:</span><span class="sxs-lookup"><span data-stu-id="58b3b-120">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objShell.Windows();

        if (objShellWindows != null)
        {
            var Shell = new ActiveXObject("WScript.Shell");
            Shell.Popup(objShellWindows.Count);
        }
    }
</script>
```



<span data-ttu-id="58b3b-121">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="58b3b-121">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsVBS()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objShell.Windows

        if (not objShellWindows is nothing) then
            WScript.Echo objShellWindows.Count
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="58b3b-122">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="58b3b-122">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objShell.Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="58b3b-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58b3b-123">Requirements</span></span>



| <span data-ttu-id="58b3b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="58b3b-124">Requirement</span></span> | <span data-ttu-id="58b3b-125">Valore</span><span class="sxs-lookup"><span data-stu-id="58b3b-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58b3b-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58b3b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="58b3b-127">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="58b3b-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="58b3b-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58b3b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="58b3b-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="58b3b-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="58b3b-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58b3b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="58b3b-131"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="58b3b-131"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="58b3b-132">Idl</span><span class="sxs-lookup"><span data-stu-id="58b3b-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="58b3b-133"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="58b3b-133"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="58b3b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="58b3b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58b3b-135"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="58b3b-135"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
