---
description: Crea e restituisce un oggetto ShellWindows. Questo oggetto rappresenta una raccolta di tutte le finestre aperte che appartengono alla Shell.
title: Metodo Shell. Windows (shldisp. h)
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
ms.openlocfilehash: a865109f926253215e5ad39227cfe3d480e9ccc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968338"
---
# <a name="shellwindows-method"></a><span data-ttu-id="e7d22-104">Shell. Windows (metodo)</span><span class="sxs-lookup"><span data-stu-id="e7d22-104">Shell.Windows method</span></span>

<span data-ttu-id="e7d22-105">Crea e restituisce un oggetto [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="e7d22-105">Creates and returns a [**ShellWindows**](shellwindows.md) object.</span></span> <span data-ttu-id="e7d22-106">Questo oggetto rappresenta una raccolta di tutte le finestre aperte che appartengono alla Shell.</span><span class="sxs-lookup"><span data-stu-id="e7d22-106">This object represents a collection of all of the open windows that belong to the Shell.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7d22-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7d22-107">Syntax</span></span>


```JScript
retVal = Shell.Windows()
```


```VB

Shell.Windows() As IDispatch
```





## <a name="parameters"></a><span data-ttu-id="e7d22-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7d22-108">Parameters</span></span>

<span data-ttu-id="e7d22-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e7d22-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e7d22-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e7d22-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="e7d22-111">JScript</span><span class="sxs-lookup"><span data-stu-id="e7d22-111">JScript</span></span>

<span data-ttu-id="e7d22-112">Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="e7d22-112">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="e7d22-113">Riferimento all'oggetto [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="e7d22-113">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="e7d22-114">VB</span><span class="sxs-lookup"><span data-stu-id="e7d22-114">VB</span></span>

<span data-ttu-id="e7d22-115">Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="e7d22-115">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="e7d22-116">Riferimento all'oggetto [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="e7d22-116">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="e7d22-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="e7d22-117">Examples</span></span>

<span data-ttu-id="e7d22-118">Nell'esempio seguente viene utilizzato **Windows** per recuperare l'oggetto [**ShellWindows**](shellwindows.md) e viene visualizzato un conteggio del numero di elementi in esso contenuti.</span><span class="sxs-lookup"><span data-stu-id="e7d22-118">The following example uses **Windows** to retrieve the [**ShellWindows**](shellwindows.md) object and display a count of the number of items that it contains.</span></span> <span data-ttu-id="e7d22-119">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e7d22-119">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="e7d22-120">JScript</span><span class="sxs-lookup"><span data-stu-id="e7d22-120">JScript:</span></span>


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



<span data-ttu-id="e7d22-121">VBScript</span><span class="sxs-lookup"><span data-stu-id="e7d22-121">VBScript:</span></span>


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



<span data-ttu-id="e7d22-122">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="e7d22-122">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="e7d22-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7d22-123">Requirements</span></span>



| <span data-ttu-id="e7d22-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7d22-124">Requirement</span></span> | <span data-ttu-id="e7d22-125">Valore</span><span class="sxs-lookup"><span data-stu-id="e7d22-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7d22-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7d22-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e7d22-127">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e7d22-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e7d22-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7d22-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e7d22-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e7d22-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e7d22-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7d22-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7d22-131"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7d22-131"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e7d22-132">IDL</span><span class="sxs-lookup"><span data-stu-id="e7d22-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e7d22-133"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e7d22-133"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e7d22-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e7d22-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7d22-135"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="e7d22-135"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
