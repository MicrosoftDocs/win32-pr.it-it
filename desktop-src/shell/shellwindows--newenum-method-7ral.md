---
description: Crea e restituisce un nuovo oggetto ShellWindows che è una copia di questo oggetto ShellWindows.
title: ShellWindows._NewEnum metodo (Exdisp.h)
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
ms.openlocfilehash: 944da80196db12d0bfa5d64767c5e6c2e8ff733e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841252"
---
# <a name="shellwindows_newenum-method"></a><span data-ttu-id="94dac-103">ShellWindows. \_ Metodo NewEnum</span><span class="sxs-lookup"><span data-stu-id="94dac-103">ShellWindows.\_NewEnum method</span></span>

<span data-ttu-id="94dac-104">Crea e restituisce un nuovo [**oggetto ShellWindows**](shellwindows.md) che è una copia di questo **oggetto ShellWindows.**</span><span class="sxs-lookup"><span data-stu-id="94dac-104">Creates and returns a new [**ShellWindows**](shellwindows.md) object that is a copy of this **ShellWindows** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="94dac-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="94dac-105">Syntax</span></span>


```JScript
retVal = ShellWindows._NewEnum()
```



## <a name="parameters"></a><span data-ttu-id="94dac-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="94dac-106">Parameters</span></span>

<span data-ttu-id="94dac-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="94dac-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="94dac-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="94dac-108">Return value</span></span>

<span data-ttu-id="94dac-109">Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span><span class="sxs-lookup"><span data-stu-id="94dac-109">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span></span>

<span data-ttu-id="94dac-110">Riferimento all'oggetto alla [**copia dell'oggetto ShellWindows.**](shellwindows.md)</span><span class="sxs-lookup"><span data-stu-id="94dac-110">An object reference to the [**ShellWindows**](shellwindows.md) object copy.</span></span>

## <a name="examples"></a><span data-ttu-id="94dac-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="94dac-111">Examples</span></span>

<span data-ttu-id="94dac-112">Nell'esempio seguente viene **\_ illustrato NewEnum** in uso.</span><span class="sxs-lookup"><span data-stu-id="94dac-112">The following example shows **\_NewEnum** in use.</span></span> <span data-ttu-id="94dac-113">L'utilizzo corretto viene visualizzato per VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="94dac-113">Proper usage is shown for VBScript and Visual Basic.</span></span> <span data-ttu-id="94dac-114">Questo metodo non può essere usato con JScript.</span><span class="sxs-lookup"><span data-stu-id="94dac-114">This method cannot be used with JScript.</span></span>

<span data-ttu-id="94dac-115">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="94dac-115">VBScript:</span></span>


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



<span data-ttu-id="94dac-116">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="94dac-116">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="94dac-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94dac-117">Requirements</span></span>



| <span data-ttu-id="94dac-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="94dac-118">Requirement</span></span> | <span data-ttu-id="94dac-119">Valore</span><span class="sxs-lookup"><span data-stu-id="94dac-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94dac-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94dac-120">Minimum supported client</span></span><br/> | <span data-ttu-id="94dac-121">Solo app desktop di Windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="94dac-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="94dac-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94dac-122">Minimum supported server</span></span><br/> | <span data-ttu-id="94dac-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="94dac-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="94dac-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="94dac-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="94dac-125"><dt>Exdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="94dac-125"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="94dac-126">DLL</span><span class="sxs-lookup"><span data-stu-id="94dac-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94dac-127"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="94dac-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
