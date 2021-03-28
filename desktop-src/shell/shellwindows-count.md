---
description: Contiene il numero di elementi nella raccolta.
ms.assetid: 0113cc32-2197-4004-99a1-89fe10828e5f
title: Proprietà ShellWindows. Count (Exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows.Count
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a8d5b9e605650ba7d3cb6036e8abfac58c0b8597
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980714"
---
# <a name="shellwindowscount-property"></a><span data-ttu-id="6f5c3-103">Proprietà ShellWindows. Count</span><span class="sxs-lookup"><span data-stu-id="6f5c3-103">ShellWindows.Count property</span></span>

<span data-ttu-id="6f5c3-104">Contiene il numero di elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="6f5c3-104">Contains the number of items in the collection.</span></span>

<span data-ttu-id="6f5c3-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6f5c3-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f5c3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f5c3-106">Syntax</span></span>


```JScript
iCount = ShellWindows.Count
```



## <a name="property-value"></a><span data-ttu-id="6f5c3-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="6f5c3-107">Property value</span></span>

<span data-ttu-id="6f5c3-108">**Intero** contenente un valore per la proprietà **count** .</span><span class="sxs-lookup"><span data-stu-id="6f5c3-108">An **Integer** that contains a value for the **Count** property.</span></span>

## <a name="examples"></a><span data-ttu-id="6f5c3-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="6f5c3-109">Examples</span></span>

<span data-ttu-id="6f5c3-110">Nell'esempio seguente viene illustrato il **conteggio** in uso.</span><span class="sxs-lookup"><span data-stu-id="6f5c3-110">The following example shows **Count** in use.</span></span> <span data-ttu-id="6f5c3-111">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6f5c3-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="6f5c3-112">JScript</span><span class="sxs-lookup"><span data-stu-id="6f5c3-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellWindowsCountJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Shell_Windows();
        if (objShellWindows != null)
        {
            var nCount;
            
            nCount = objShellWindows.Count;
            alert(nCount);
        }
    }
</script>
```



<span data-ttu-id="6f5c3-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="6f5c3-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsCountVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Shell_Windows

        if (not objShellWindows is nothing) then
            dim nCount
            nCount = objShellWindows.Count

            alert(nCount)
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="6f5c3-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="6f5c3-114">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsCountVB()
    Dim objShell         As Shell
    Dim objShellWindows  As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Shell_Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="6f5c3-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f5c3-115">Requirements</span></span>



| <span data-ttu-id="6f5c3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f5c3-116">Requirement</span></span> | <span data-ttu-id="6f5c3-117">Valore</span><span class="sxs-lookup"><span data-stu-id="6f5c3-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f5c3-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f5c3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6f5c3-119">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6f5c3-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6f5c3-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f5c3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6f5c3-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6f5c3-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6f5c3-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f5c3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f5c3-123"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f5c3-123"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="6f5c3-124">DLL</span><span class="sxs-lookup"><span data-stu-id="6f5c3-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f5c3-125"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="6f5c3-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




