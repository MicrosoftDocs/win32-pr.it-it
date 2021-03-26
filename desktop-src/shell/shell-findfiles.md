---
description: "Consente di visualizzare la finestra di dialogo Trova: tutti i file. Questa operazione equivale a fare clic sul menu Start e quindi selezionare Cerca (o l'equivalente in sistemi precedenti a Windows XP)."
ms.assetid: cccdd3ea-b52a-4fbe-b4c5-1efc1dd6d770
title: Metodo Shell. FindFiles (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindFiles
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f3e6551dc41fd8d6a040ada8000f0b46e81a5dd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233203"
---
# <a name="shellfindfiles-method"></a><span data-ttu-id="bcbe3-104">Shell. FindFiles, metodo</span><span class="sxs-lookup"><span data-stu-id="bcbe3-104">Shell.FindFiles method</span></span>

<span data-ttu-id="bcbe3-105">Consente di visualizzare la finestra di dialogo **trova: tutti i file** .</span><span class="sxs-lookup"><span data-stu-id="bcbe3-105">Displays the **Find: All Files** dialog box.</span></span> <span data-ttu-id="bcbe3-106">Questa operazione equivale a fare clic sul menu **Start** e quindi selezionare **Cerca** (o l'equivalente in sistemi precedenti a Windows XP).</span><span class="sxs-lookup"><span data-stu-id="bcbe3-106">This is the same as clicking the **Start** menu and then selecting **Search** (or its equivalent under systems earlier than Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcbe3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bcbe3-107">Syntax</span></span>


```JScript
Shell.FindFiles()
```


```VB

Shell.FindFiles()
```





## <a name="parameters"></a><span data-ttu-id="bcbe3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bcbe3-108">Parameters</span></span>

<span data-ttu-id="bcbe3-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="bcbe3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bcbe3-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bcbe3-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="bcbe3-111">JScript</span><span class="sxs-lookup"><span data-stu-id="bcbe3-111">JScript</span></span>

<span data-ttu-id="bcbe3-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="bcbe3-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="bcbe3-113">VB</span><span class="sxs-lookup"><span data-stu-id="bcbe3-113">VB</span></span>

<span data-ttu-id="bcbe3-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="bcbe3-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="bcbe3-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="bcbe3-115">Examples</span></span>

<span data-ttu-id="bcbe3-116">Nell'esempio seguente viene illustrato **FindFiles** in uso.</span><span class="sxs-lookup"><span data-stu-id="bcbe3-116">The following example shows **FindFiles** in use.</span></span> <span data-ttu-id="bcbe3-117">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="bcbe3-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="bcbe3-118">JScript</span><span class="sxs-lookup"><span data-stu-id="bcbe3-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindFilesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Shell_FindFiles();
    }
</script>
```



<span data-ttu-id="bcbe3-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="bcbe3-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFindFilesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.FindFiles

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="bcbe3-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="bcbe3-120">Visual Basic:</span></span>


```VB
Private Sub fnShellFindFilesVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindFiles

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="bcbe3-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bcbe3-121">Requirements</span></span>



| <span data-ttu-id="bcbe3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcbe3-122">Requirement</span></span> | <span data-ttu-id="bcbe3-123">Valore</span><span class="sxs-lookup"><span data-stu-id="bcbe3-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcbe3-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bcbe3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bcbe3-125">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bcbe3-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bcbe3-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bcbe3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bcbe3-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bcbe3-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bcbe3-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bcbe3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcbe3-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcbe3-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="bcbe3-130">IDL</span><span class="sxs-lookup"><span data-stu-id="bcbe3-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bcbe3-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bcbe3-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="bcbe3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="bcbe3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcbe3-133"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="bcbe3-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




