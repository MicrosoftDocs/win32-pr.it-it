---
description: 'Consente di visualizzare la finestra di dialogo Trova: tutti i file. Questo equivale a fare clic sul menu Start e quindi scegliere Cerca.'
ms.assetid: 6F588D5E-5B6E-4000-BAD5-B557FB975FCA
title: Metodo IShellDispatch. FindFiles (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FindFiles
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9a9ea407d0ceccfe7706ed481aa80bcda9405ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879790"
---
# <a name="ishelldispatchfindfiles-method"></a><span data-ttu-id="dcbdf-104">IShellDispatch. FindFiles, metodo</span><span class="sxs-lookup"><span data-stu-id="dcbdf-104">IShellDispatch.FindFiles method</span></span>

<span data-ttu-id="dcbdf-105">Consente di visualizzare la finestra di dialogo **trova: tutti i file** .</span><span class="sxs-lookup"><span data-stu-id="dcbdf-105">Displays the **Find: All Files** dialog box.</span></span> <span data-ttu-id="dcbdf-106">Questo equivale a fare clic sul menu **Start** e quindi scegliere **Cerca**.</span><span class="sxs-lookup"><span data-stu-id="dcbdf-106">This is the same as clicking the **Start** menu and then selecting **Search**.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcbdf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dcbdf-107">Syntax</span></span>


```JScript
IShellDispatch.FindFiles()
```


```VB

IShellDispatch.FindFiles()
```





## <a name="parameters"></a><span data-ttu-id="dcbdf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dcbdf-108">Parameters</span></span>

<span data-ttu-id="dcbdf-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="dcbdf-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dcbdf-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dcbdf-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="dcbdf-111">JScript</span><span class="sxs-lookup"><span data-stu-id="dcbdf-111">JScript</span></span>

<span data-ttu-id="dcbdf-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="dcbdf-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="dcbdf-113">VB</span><span class="sxs-lookup"><span data-stu-id="dcbdf-113">VB</span></span>

<span data-ttu-id="dcbdf-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="dcbdf-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcbdf-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="dcbdf-115">Remarks</span></span>

<span data-ttu-id="dcbdf-116">Questo metodo viene implementato e accessibile tramite il metodo [**Shell. FindFiles**](shell-findfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="dcbdf-116">This method is implemented and accessed through the [**Shell.FindFiles**](shell-findfiles.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="dcbdf-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="dcbdf-117">Examples</span></span>

<span data-ttu-id="dcbdf-118">Negli esempi seguenti viene illustrato l'utilizzo di **FindFiles** in JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="dcbdf-118">The following examples show the use of **FindFiles** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="dcbdf-119">JScript</span><span class="sxs-lookup"><span data-stu-id="dcbdf-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindFilesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindFiles();
    }
</script>
```



<span data-ttu-id="dcbdf-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="dcbdf-120">VBScript:</span></span>


```VB
<script language="VBScript">
   function fnShellFindFilesVB()
       dim objShell
       
       set objShell = CreateObject("shell.application")
       objshell.FindFiles

       set objShell = nothing
   end function
</script>
```



<span data-ttu-id="dcbdf-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="dcbdf-121">Visual Basic:</span></span>


```VB
Private Sub fnShellFindFilesVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindFiles

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="dcbdf-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dcbdf-122">Requirements</span></span>



| <span data-ttu-id="dcbdf-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcbdf-123">Requirement</span></span> | <span data-ttu-id="dcbdf-124">Valore</span><span class="sxs-lookup"><span data-stu-id="dcbdf-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcbdf-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dcbdf-125">Minimum supported client</span></span><br/> | <span data-ttu-id="dcbdf-126">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="dcbdf-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="dcbdf-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dcbdf-127">Minimum supported server</span></span><br/> | <span data-ttu-id="dcbdf-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dcbdf-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dcbdf-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dcbdf-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcbdf-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcbdf-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="dcbdf-131">IDL</span><span class="sxs-lookup"><span data-stu-id="dcbdf-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dcbdf-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dcbdf-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="dcbdf-133">DLL</span><span class="sxs-lookup"><span data-stu-id="dcbdf-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcbdf-134"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="dcbdf-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




