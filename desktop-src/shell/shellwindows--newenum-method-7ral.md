---
description: Crea e restituisce un nuovo oggetto ShellWindows che è una copia di questo oggetto ShellWindows.
title: Metodo ShellWindows._NewEnum (Exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows._NewEnum
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 85e84c13-62aa-4502-b642-ca55273a800d
ms.openlocfilehash: ded5ae2c337e80359c012fb63a37aa13cc43b5fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233562"
---
# <a name="shellwindows_newenum-method"></a><span data-ttu-id="2e606-103">ShellWindows. \_ Metodo NewEnum</span><span class="sxs-lookup"><span data-stu-id="2e606-103">ShellWindows.\_NewEnum method</span></span>

<span data-ttu-id="2e606-104">Crea e restituisce un nuovo oggetto [**ShellWindows**](shellwindows.md) che è una copia di questo oggetto **ShellWindows** .</span><span class="sxs-lookup"><span data-stu-id="2e606-104">Creates and returns a new [**ShellWindows**](shellwindows.md) object that is a copy of this **ShellWindows** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e606-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e606-105">Syntax</span></span>


```JScript
retVal = ShellWindows._NewEnum()
```



## <a name="parameters"></a><span data-ttu-id="2e606-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e606-106">Parameters</span></span>

<span data-ttu-id="2e606-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="2e606-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2e606-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e606-108">Return value</span></span>

<span data-ttu-id="2e606-109">Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span><span class="sxs-lookup"><span data-stu-id="2e606-109">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span></span>

<span data-ttu-id="2e606-110">Riferimento a un oggetto alla copia dell'oggetto [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="2e606-110">An object reference to the [**ShellWindows**](shellwindows.md) object copy.</span></span>

## <a name="examples"></a><span data-ttu-id="2e606-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="2e606-111">Examples</span></span>

<span data-ttu-id="2e606-112">Nell'esempio seguente viene illustrato **\_ NewEnum** in uso.</span><span class="sxs-lookup"><span data-stu-id="2e606-112">The following example shows **\_NewEnum** in use.</span></span> <span data-ttu-id="2e606-113">L'utilizzo corretto viene visualizzato per VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2e606-113">Proper usage is shown for VBScript and Visual Basic.</span></span> <span data-ttu-id="2e606-114">Questo metodo non può essere utilizzato con JScript.</span><span class="sxs-lookup"><span data-stu-id="2e606-114">This method cannot be used with JScript.</span></span>

<span data-ttu-id="2e606-115">VBScript</span><span class="sxs-lookup"><span data-stu-id="2e606-115">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsNewEnumVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Shell_Windows

        if (not objShellWindows is nothing) then
            dim objEnumItems
            
            for each objEnumItems in objShellWindows
                alert(objEnumItems.Type)
            next
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="2e606-116">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="2e606-116">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsNewEnumVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Shell_Windows

    If (Not objShellWindows Is Nothing) Then
        Dim vEnumItem As Variant
        
        For Each vEnumItem In objShellWindows
            Debug.Print vEnumItem.Type
        Next vEnumItem
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="2e606-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e606-117">Requirements</span></span>



| <span data-ttu-id="2e606-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e606-118">Requirement</span></span> | <span data-ttu-id="2e606-119">Valore</span><span class="sxs-lookup"><span data-stu-id="2e606-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e606-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e606-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2e606-121">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2e606-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2e606-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e606-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2e606-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2e606-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2e606-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2e606-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e606-125"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e606-125"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="2e606-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2e606-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e606-127"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="2e606-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
